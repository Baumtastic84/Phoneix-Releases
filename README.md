# Phoneix Releases

Public binary distribution for **Phoneix**.

This repository contains release assets only. Phoneix source code, development branches, pull requests, and the release-signing process live separately in the private development repository.

## What is published here

Phoneix releases may include:

- Phoneix Forge for Windows
- Phoneix Nest packages for `win-x64`, `linux-x64`, and `linux-arm64`
- signed Nest package manifests
- Windows Nest Setup
- the offline Windows deployment kit
- signed Raspberry Pi appliance images and manifests

## Release channels

- `vX.Y.Z-beta.N` — beta/prerelease builds
- `vX.Y.Z-dev.N` — developer/prerelease builds
- `vX.Y.Z` — stable builds

## Update trust

This repository is public so normal Phoneix installations can download releases without a GitHub account or access token.

Public hosting is **not** the update trust boundary. Phoneix verifies signed release manifests with the public key embedded in the software and verifies the downloaded archive/image hashes before installation. A file uploaded here without a valid Phoneix release signature is rejected by current clients.

The private release-signing key is not stored in this repository and must never be committed or uploaded here.

## Historical releases

Older prerelease assets may predate the current signed-release contract and are retained only for development history. Current v1-Beta clients intentionally require the newer signed manifest format.
