# Theodia Remote MP3 Playlists

This repository distributes `.playlist.zip` packages for Theodia playlists that use publicly available remote MP3 audio instead of TTS.

## Contents

| Package | Description | Source |
| ------- | ----------- | ------ |
| `the-pilgrims-progress.playlist.zip` | **The Pilgrim's Progress (Audio)** — the complete book by John Bunyan, read by MaryAnn for LibriVox. | [LibriVox](https://librivox.org/the-pilgrims-progress-by-john-bunyan-2/) / [Internet Archive](https://archive.org/details/pilgrimsprogress_1407_librivox) |

## Installing

Open **Theodia → Settings → Manage Resources → Playlists → Install from GitHub** and select this repository (`theodia.playlist.remote-mp3`).

## Packaging

1. Clone this repository to `/Volumes/external/theodia.playlist.remote-mp3`.
2. Add playlist source directories under `assets/data/playlists_dev/<playlist-name>/` containing one `.playlist.json` file and any referenced local MP3s.
3. From the main Theodia source repo, run:
   ```bash
   THEODIA_PLAYLISTS_CLONE=/Volumes/external/theodia.playlist.remote-mp3 npx tsx scripts/package-playlists.ts <playlist-name>
   ```
4. Commit and push the resulting `.playlist.zip` and updated `README.md`.
