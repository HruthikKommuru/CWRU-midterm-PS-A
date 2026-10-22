# Client Brief Build

Maria runs a small bakery, Maria's Bakery. She sent a messy voice note, a logo,
a flyer, and photos. She wants a website.

Your mission: turn her request into a one-page website she would be happy with.
Visitors will use phones. Make the page mobile-first.

Hidden problems are in the inputs. Finding them is part of your score.
Use only files in inputs/. Prove your answer is right.

## Inputs

- `inputs/client_transcript.md`: Maria's voice note.
- `inputs/flyer.png`: her flyer.
- `inputs/logo.png`: her logo.
- `inputs/photos/`: five captioned placeholder images.

## Roles

| Role | Your file | Your job |
| --- | --- | --- |
| 1. Business Analyst (LEADER) | `roles/01_business_analyst/requirements.md` | List wants, contradictions, and questions. |
| 2. Copywriter | `roles/02_copywriter/copy.md` | Write headline, menu and prices, hours, about, and contact. |
| 3. UI/UX Designer | `roles/03_ui_ux_designer/styles.css` | Choose colors, fonts, and layout. Use text 16px+ and buttons 44px+. |
| 4. Web Developer | `roles/04_web_developer/index.html` | Build the page with temporary text and link the designer's CSS. |

## Rules

1. Each person edits only their own role file. Keep inputs, shared files, other
   roles, and all AGENTS.md files unchanged.
2. Read `shared/page_structure.md`. Designer and Developer use its exact section
   IDs and class names, so both can work at the same time.
3. Use only the inputs for facts. No web search. Point to evidence for decisions.
4. Plan before big changes. Check the result and explain what changed.
5. Work on your own branch. Tell Codex "done" when ready to commit, push, and merge.
   Never force-push. Stop for the leader if there is a merge conflict.
6. After all four roles merge, the leader creates the final work on a new branch
   from main, edits only `final/`, and merges when the team agrees.

## Timeline (90 minutes)

Before the clock (if you can): fork, clone, open Codex.

- 0-5 read the brief and join your role
- 5-45 do your role (say "done" by minute 45)
- 45-55 everyone merges
- 55-80 leader builds final/, team reviews
- 80-90 rehearse the 5-minute talk

## Final hand-in

The leader builds `final/index.html` and `final/styles.css`, with working images,
plus `final/questions_for_maria.md` and `final/presentation_outline.md` for a
5-minute presentation. The leader swaps temporary page text for the final copy.
Check the page on a phone-sized screen, test links and images, and explain any
assumptions that still need Maria's answer. See `final/README.md` for the checklist.
