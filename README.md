# tower-memory

Tower's memory: everything personal that the Chief of Staff app reads. Private; never copy any of it into the app's repo.

- `memory.json`: the agent (`assistant.id` is permanent; `assistant.name` is the alias), the owner and people, divisions and calendars, standing agreements, rules, cadence.
- `digests.json`: where digests arrive and how each source is read.
- `notes/`: personal context the agent uses (rotations, travel, setup tasks).

The folder and repo are named `<alias>-memory`. Renaming the agent (`cos rename <new>` or the app's Settings) moves this to `<new>-memory`; the id stays, so it is the same agent. On GitHub, rename the repo to match (GitHub redirects the old name).

The layout is specified in the app's `docs/memory.md`.
