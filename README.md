# Theodia Remote MP3 Playlists

This repository distributes `.playlist.zip` packages for Theodia playlists that use publicly available remote MP3 audio instead of TTS.

## Catalog

See `index.json` for the machine-readable package catalog.

| Package | Description | Source |
| ------- | ----------- | ------ |
| `The-Pilgrims-Progress-Audio.playlist.zip` | **The Pilgrim's Progress (Audio)** — the complete book by John Bunyan, read by MaryAnn for LibriVox. | [LibriVox](https://librivox.org/the-pilgrims-progress-by-john-bunyan-2/) / [Internet Archive](https://archive.org/details/pilgrimsprogress_1407_librivox) |

## Installing

Open **Theodia → Settings → Manage Resources → Playlists → Install from GitHub** and select this repository (`theodia.playlist.remote-mp3`).

## Packaging

1. Clone this repository to `/Volumes/external/theodia.playlist.remote-mp3`.
2. Add playlist source directories under `assets/data/playlists_dev/<Playlist-Name>/` containing one `.playlist.json` file and any referenced local MP3s.
3. From the main Theodia source repo, run:
   ```bash
   THEODIA_PLAYLISTS_CLONE=/Volumes/external/theodia.playlist.remote-mp3 npx tsx scripts/package-playlists.ts <Playlist-Name>
   ```
4. Update `index.json` and `README.md`.
5. Commit and push the resulting `.playlist.zip`, `index.json`, and `README.md`.

## File naming

Package file names follow [`notes/github-repo-naming-standards.md`](https://github.com/ecodiallc/theodia/blob/main/notes/github-repo-naming-standards.md):

- Sentence-case each word.
- Separate words with dashes (`-`).
- Keep the extension lowercase (`.playlist.zip`).
