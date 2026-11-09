# Mindcraft MVP v0.1

A working offline-first iPhone-installable Progressive Web App with 30 daily quests, 5 skill tracks (including Ne), XP, levels, achievements, journal, pending AI review status, and IndexedDB autosave.

## Run locally

Serve the folder over HTTP: `python3 -m http.server 8080` then open `http://localhost:8080`. A service worker requires HTTPS (or localhost). To install on iPhone, deploy this folder to an HTTPS host such as GitHub Pages, Netlify, or Cloudflare Pages, open the URL in Safari, choose Share > Add to Home Screen, and launch it once online to cache assets.

## What is NOT implemented

- Firebase sign-in, cloud synchronization, encrypted cloud backups, recovery key management
- AI review, mastery assessment, weekly AI growth reports
- Weekly boss challenges / sophisticated game types (current missions use multiple-choice and writing)

The UI explicitly marks cloud and AI as not connected. The manual JSON export is unencrypted. Never treat the local copy as an off-device backup. Use Export Backup and store it safely until cloud sync is implemented.

## Security notes for next phase

A robust encrypted cloud design requires client-side AES-GCM with a random data encryption key, password/recovery-key wrapping, safe rotation and recovery UX, and authenticated sync. AI review needs separate explicit consent to send selected plaintext to a trusted server-side endpoint, where API keys are kept off-device. Never put service secrets in browser code. Multi-device conflict resolution and reliable retry queues also need implementation.

## Note on learning science

MBTI function labels are conceptual prompts, not clinically validated cognitive metrics. XP measures activity, not proven skill growth.
