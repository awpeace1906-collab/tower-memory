# Setup tasks (owner)

The owner's own setup steps for running the Chief of Staff app. Product work is tracked in the core repo's ROADMAP.

## App hosting and accounts

- [ ] Create the Google Cloud project and connect Google (one-time; core `docs/setup/google.md`). Sign in as the Gmail account in `memory.json` → `assistant.email`; add it as a test user.
- [ ] Put the Anthropic API key in the app's environment; reconnect Google once for the send and calendar-write permissions.
- [ ] Pick a host (Fly.io recommended to start; region near Las Cruces/El Paso, e.g. `den`) and deploy; register the Microsoft app and connect the personal Microsoft account.
- [ ] Optional: `AERODATABOX_KEY` (RapidAPI) for per-flight status; FAA airport data works without it.
- [ ] Load memory into the app: `cos import --memory /data/tower-memory` (plus `--page` with the page export).
- [ ] Turn on `email.sendApprovedDrafts` once comfortable with the agent sending approved drafts from Gmail.
- [ ] Later: location on the iPhone. Until the native app exists, a Shortcuts automation sends the phone's location to the app (core `docs/features/location.md`).

## Texting and voice

- [ ] Rent a number (VoIP.ms or Telnyx) and register A2P 10DLC once the app is hosted.
- [ ] Choose home hardware later: cloud server now; Mac mini M4 (or an N100 mini PC for text only) once usage is clear.
- [ ] When the app's text line works, retire readywhen's WhatsApp beta.

## Brain

- [ ] Connect Brain (`BRAIN_GIST_TOKEN`, classic PAT with `gist` scope, in the app's environment); seed Tower's rules into it. Brain contract: the Brain repo's INTEGRATION.md.

## Digests and mail

- [ ] burrell.edu Outlook rules: forward Microsoft 365 digests (Viva briefing, Teams, Planner, SharePoint) to the Tower inbox (tower-andrew@agentmail.to); confirm Burrell IT allows external forwarding. Digests only, never patient-facing systems.
- [ ] Confirm the real sender address for each adapter in `digests.json` from the first digest received.

## Transition

- [ ] Run Tower's capture alongside readywhen for 2 weeks; log misses (see `context.md` → readywhen parity).
- [ ] Parity reached → drop readywhen from the brief; move the brief time if wanted (now 8:25am MT, after readywhen's ~8:17am brief).
- [ ] Cut over from the Claude Code scheduled tasks, the Chief of Staff page, AgentMail and readywhen to the hosted app.

## Household

- [ ] Tiffany contract review: pull her scheduled hours from the Tiffany Schedule calendar as a starting point.
