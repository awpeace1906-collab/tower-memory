# Tower's memory: notes for Claude

- This private repo is the agent's memory: the owner's people, divisions, calendars, rules and notes. The app's code lives in github.com/awpeace1906-collab/chief-of-staff (the core) and reads this repo; the layout is specified there in `docs/memory.md`.
- Personal information belongs here and never in the core. After changing anything here, run `python ../chief-of-staff/tools/check_core.py --memory .` if the core is checked out beside it.
- `assistant.id` (`tower`) never changes. To rename the agent, change only `assistant.name` (with the old name added to `formerNames`), and rename this repo to `<new name>-memory`; the app's Settings or `cos rename <name>` do both locally.
- When the owner states a new rule or preference, add it to `memory.json` (the matching rules list, or `standingAgreements`) on a branch with a PR.
- Never store passwords, keys or tokens here; say where they are kept instead. Never copy clinical or patient details.
