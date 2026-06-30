# Mood Collab — distribution

Public, **releases-only** mirror of the **Mood Collab** Obsidian plugin. The
source lives in a private repository; this repo exists so the team can install
and auto-update the plugin via **BRAT** without needing any GitHub access to the
source.

It contains only the **built** plugin (`manifest.json`, `versions.json`,
`main.js`, `styles.css`) — no source, no server secrets. The plugin is useless
without valid credentials to the team's collab server, so publishing the build
here exposes nothing sensitive.

## Install (BRAT)

1. Install the **BRAT** community plugin in Obsidian.
2. In BRAT: **Add beta plugin** → `MoodStudios/moodstudios-collab-dist`.
3. Enable **Mood Collab**, then log in with your team credentials.

No GitHub account or token is required — this repo is public.

## Updating

This repo is published automatically from the private source repo on each
version tag. BRAT picks up new versions on its own; you don't need to do
anything after the first install.
