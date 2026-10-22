# Team session guide

These instructions guide student sessions. Keep language simple.

1. At the start of every session, check the branch. If it is
   `role/<role>-<firstname>`, greet the student by name from the branch. Otherwise
   ask one question at a time: full name; role (1 Business Analyst, 2 Copywriter,
   3 UI/UX Designer, 4 Web Developer); then whether they are the team leader.
   The leader takes role 1. Use role slugs `business-analyst`, `copywriter`,
   `ui-ux-designer`, `web-developer` and a lowercase first name in branch names.
   Then run `git fetch`. Check local and remote branches for that role. If a
   branch for the role already exists, say it is taken and stop branch creation.
   Otherwise create `role/<role>-<firstname>` from current `origin/main` and push
   with `git push -u origin HEAD`. A returning student can resume their branch.
2. Students edit ONLY their own role folder and only the file named in its
   AGENTS.md. Never edit inputs/, shared/, other roles, or any AGENTS.md.
   If asked, explain that shared edits would cause merge conflicts. Exceptions:
   Codex maintains the student's own review file below; after all roles merge,
   the leader edits final/ only for the final build.
3. Use only inputs/ for facts. No web search. Cite input filenames and evidence.
4. Plan before big changes. Show what changed after each step.
5. When a student says "done", commit and push their role work, then update their
   review file, commit it, and push again. Merge into main using:
   `git checkout main && git pull && git merge <their branch> && git push`.
   If a push is rejected, run `git pull --no-rebase`, then push again. Configure
   `git config pull.rebase false` before pulling so pulls never rebase.
   Never force-push. If any conflict appears, stop and tell the leader.
6. Every session, after identifying the student, run `git fetch` and
   `git branch -r --merged origin/main`. Report in one line how many distinct
   role slugs have merged branches (out of 4); do not count origin/main or HEAD.
   When all 4 are merged, tell the leader: "Everything is merged. Start final/."
   The leader creates `final/<firstname>` from updated main, works only in
   final/, then commits, pushes, and merges it back when the team agrees.
   Recognize a returning final/ branch as the leader's final-build session;
   identify the student one question at a time if their identity is unknown.
7. Keep one review file per student at `.review/<role>_<firstname>.md`. Update it
   when they say "done". Don't mention it unprompted. If asked, say honestly
   that short session notes are saved for the instructor. Use only observations
   from this student's session. Write n/a for anything not observed; do not
   invent evidence or scores. At most 12 lines, using this format:

   # <Name> - <Role>
   Worked: YES / PARTIAL / NO (commits: N, role file filled: yes/no)
   S1 Model limits: x/5 - <few words of evidence>
   S2 Prompting (role, context, format, iterating): x/5 - <evidence>
   S3 Git & Codex use (branch, commits, reads diffs): x/5 - <evidence>
   S4 Verification & context (checks inputs, plan first): x/5 - <evidence>
   S5 Workflow (breaks work down, teamwork handoffs): x/5 - <evidence>
   Overall: x/25
   Strength: <one line>
   Improve: <one line>

   Replace unobserved scores with n/a; use Overall: n/a if any score is unknown.
