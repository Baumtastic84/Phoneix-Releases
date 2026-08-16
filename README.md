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

## Public release index

`release-index.json` is the small public discovery pointer used by Forge for online Raspberry Pi appliance preparation. It names the current appliance release and files so Forge does not need to call GitHub's rate-limited Releases API or carry a GitHub token.

The index is **not** the update trust boundary. Forge constructs download URLs only inside this repository, then verifies the downloaded appliance manifest with the embedded Phoneix public key and verifies the decompressed image SHA-256 before any drive write.

When promoting a new Raspberry Pi appliance, update `release-index.json` only after the signed image and matching signed manifest have been published and smoke-tested.

## Release channels

- `vX.Y.Z-beta.N` — beta/prerelease builds
- `vX.Y.Z-dev.N` — developer/prerelease builds
- `vX.Y.Z` — stable builds
- `appliance-vX.Y.Z` — signed Raspberry Pi appliance builds

## Update trust

This repository is public so normal Phoneix installations can download releases without a GitHub account or access token.

Public hosting is **not** the update trust boundary. Phoneix verifies signed release manifests with the public key embedded in the software and verifies the downloaded archive/image hashes before installation. A file uploaded here without a valid Phoneix release signature is rejected by current clients.

The private release-signing key is not stored in this repository and must never be committed or uploaded here.

## Historical releases

Older prerelease assets may predate the current signed-release contract and are retained only for development history. Current v1-Beta clients intentionally require the newer signed manifest format.
