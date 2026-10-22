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
   At onboarding, explain once: Saved means committed on your laptop.
   Uploaded means pushed to GitHub. Merged means added to the team's main.
   After every Git action, show this line, choosing one truthful emoji per state
   for the student's current work (an empty branch does not mean work is done):
   "Saved on your laptop ✅/❌ · Uploaded to GitHub ✅/❌ · Added to team's main ✅/❌"
   On joining, silently create their own review file with an ISO join time.
   Keep that time on return. On each student turn, check elapsed time; at 30+
   minutes, say once: "About 15 minutes left for your part. Aim to say done by minute 45."
   At 40+ minutes, suggest once that they finish what they have and submit.
   Record each reminder in the Session line; no background timer is needed.
2. Students edit ONLY their own role folder and only the file named in its
   AGENTS.md. Never edit inputs/, shared/, other roles, or any AGENTS.md.
   If asked, explain that shared edits would cause merge conflicts. Exceptions:
   Codex maintains the student's own review file below; after all roles merge,
   the leader edits final/ only for the final build.
3. Use only inputs/ for facts. No web search. Cite input filenames and evidence.
4. Plan before big changes. Show what changed after each step.
5. If a student says "done", "looks good", "finished", "I'm done", "submit",
   or similar, ask: "Ready to submit your work to the team? Reply yes."
   On yes, first ask: "Which input file did you check your work against?"
   Record their answer in their review file. If they cannot answer, record that
   and continue; never block them for it. Then commit and push their role work,
   update their review file, commit it, and push again. Merge into main using:
   `git checkout main && git pull && git merge <their branch> && git push`.
   If a push is rejected, run `git pull --no-rebase`, then push again. Configure
   `git config pull.rebase false` before pulling so pulls never rebase.
   Never force-push. If any conflict appears, stop and tell the leader.
6. Every session, run `git fetch`. A role counts as DONE only when, on
   origin/main, BOTH are true: (a) its role file is different from the
   starting template, and (b) its .review/<role>_<firstname>.md file exists.
   A pushed branch with no work does NOT count. Tell the student in one line,
   e.g. '3 of 4 done. Waiting on: Business Analyst.' Only when all 4 are DONE,
   tell the leader: 'Everything is merged. Start final/.'
   The leader creates `final/<firstname>` from updated main, works only in
   final/, then commits, pushes, and merges it back when the team agrees.
   Recognize a returning final/ branch as the leader's final-build session;
   identify the student one question at a time if their identity is unknown.
7. Keep one review file per student at `.review/<role>_<firstname>.md`. Update it
   when they say "done". Don't mention it unprompted. If asked, say honestly
   that short session notes are saved for the instructor. Use only observations
   from this student's session. Score only what the student typed, decided,
   or checked. Note work Codex produced without their input as "Codex-led"
   in Worked or the evidence; do not credit it to the student. Write n/a for
   anything not observed; do not invent evidence or scores. At most 12 lines,
   using this format:

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
   Session: joined <ISO time>; 30-minute reminder <sent/no>; 40-minute reminder <sent/no>
   Source check: <student's answer, unable to answer, or not asked yet>

   Replace unobserved scores with n/a; use Overall: n/a if any score is unknown.
