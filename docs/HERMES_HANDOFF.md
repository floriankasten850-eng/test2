# Hermes Handoff Note

**Audience:** Hermes / DeepSeek agent  
**Purpose:** Shared context from the ChatGPT collaborator  
**Status:** Voice setup is in progress; end-to-end success is not yet verified.

## Immediate task: finish voice input and output

The user wants a practical, personal-JARVIS-style assistant: natural voice interaction, useful memory, proactive task completion, computer/file/code assistance, and eventual coordination of models through an OmniRouter/OpenCode setup.

### Known local setup

- Windows + PowerShell.
- Hermes Agent reported version: v0.22.4 (stable build dated 2026-09-24).
- Workspace: `C:\Users\Flori\HermesWorkspace`.
- Config: `%LOCALAPPDATA%\hermes\config.yaml`.
- Hermes home: `%LOCALAPPDATA%\hermes`.
- Inference: custom AI/ML API provider, model `deepseek/deepseek-v4.1-flash`, base URL `https://api.aimlapi.com/v1`.
- `tts.provider` reads as `edge`.
- Earlier, `hermes config get stt.provider` returned `Config key not set: stt.provider`.
- `/voice status` initially reported audio capture OK but STT provider MISSING; voice mode and TTS were OFF.
- The `hermes tools` CLI tool-toggle menu has no STT provider entry. Do not send the user back there to look for one.
- A diagnostic was attempted that recorded four seconds from the default microphone and loaded `faster-whisper` `base` on CPU for English transcription. A Windows notification/voice said “Hermes is online,” but neither successful transcription nor a complete spoken-response round trip has been conclusively confirmed.

## First actions

1. Inspect the actual current machine state and recent Hermes logs/results before changing anything. Determine whether installation/diagnostic processes are still running and whether Whisper is installed in the correct Hermes-managed environment.
2. Verify the exact configuration schema and dependency-management method for the installed version. Use its installed help/source or version-matched documentation; do not assume current docs match v0.22.4.
3. Configure the supported local STT provider and install only the required dependencies using Hermes' supported mechanism. Prefer local/free speech recognition; avoid extra paid API calls.
4. Test microphone capture, actual transcription, `/voice on`, and spoken output. Then test German input/output if supported.
5. Report verified results and remaining blockers. Exit code zero alone is not sufficient proof that voice works.

## How to work with the user

- Keep instructions short and practical, usually one clear step at a time.
- The user is not asking to read long help dumps. Inspect targeted files/logs and extract relevant details yourself.
- Do not repeatedly direct the user into the same menu or ask them to paste large outputs.
- Do not invent config keys, commands, or test results.
- Back up config before meaningful edits. Never expose API keys or other secrets.
- Routine, reversible work can proceed autonomously. Ask first before destructive/security-sensitive changes, significant costs, external communications, or consequential actions.
- Use concise, direct language with occasional dry humor. Explain meaningful changes and distinguish verified facts from assumptions.

## Shared-repository collaboration

This repository is the shared source of truth for the user's multi-agent work. Read `AGENTS.md` and `docs/PROTOCOL.md` before contributing. Keep changes scoped, avoid conflicts with other agents, verify changes, and report files/checks/results. Coordinate ownership before editing shared files.

## After voice works

Propose the next small, high-value step toward the personal assistant goal: reliable memory and task follow-through first, then carefully scoped integrations with OmniRouter/OpenCode and other models. Prioritize reliability, observability, and user control over broad autonomy.