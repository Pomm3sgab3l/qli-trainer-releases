# qli-trainer-releases

Public download mirror for the **QLI pool trainer** worker binaries. This repository holds
**release assets only**. The source is maintained in a separate private repository.

## Current epoch: 235

**[Release ep235](https://github.com/Pomm3sgab3l/qli-trainer-releases/releases/tag/ep235)**: all platforms in one release.

Each epoch has exactly one release, tagged `ep<EPOCH>`. Direct links follow
`https://github.com/Pomm3sgab3l/qli-trainer-releases/releases/download/ep<EPOCH>/<file>`.

| File | Platform | Client run name |
|---|---|---|
| `win-cuda-pps-pom-<ver>.exe` | NVIDIA GPU, Windows x64 | `qli-worker-CUDA.exe` |
| `linux-amd-pps-pom-<ver>` | AMD GPU, Linux x64 (ROCm 6.x) | `qli-worker-AMD` |
| `qli-worker-ARM64-<ver>` | Android arm64-v8a | `qli-worker-ARM64` |
| `qli-worker-ARMV7-<ver>` | Android armeabi-v7a (Android 5.0+) | `qli-worker-ARMV7` |
| `*-SS-<ver>` | as above, with SessionSync (fail-closed pubkey whitelist) | as above + `-SS` |

`<ver>` is `<epoch>.<build>`, for example `235.0`. Only the newest build of each file is kept.
Releases up to epoch 234 use the older per-platform tags.

## Verify before use

Every file ships with a `.sha256`. Download both, then:

```bash
sha256sum -c qli-worker-ARM64-235.0.sha256
```

Only run a binary whose checksum matches.
