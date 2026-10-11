# qli-trainer-releases

Public download mirror for the **QLI pool trainer** worker binaries.

This repository contains **release assets only** — no source code. The trainer
source is maintained in a separate private repository. Binaries are published
here per epoch so operators can download them over a public link.

## Download

Grab the asset for your architecture and epoch from the
[Releases](https://github.com/Pomm3sgab3l/qli-trainer-releases/releases) page.

Asset naming: `qli-worker-<TARGET>-ep<EPOCH>` (+ a matching `.sha256`).

| TARGET | Device | Notes |
|---|---|---|
| `ANDROID` | Android arm64-v8a | 64-bit phones/tablets |
| `ANDROID32` | Android armeabi-v7a | old/low-end 32-bit tablets (Android 5.0+) |
| `*-SS` | as above, with SessionSync | fetches + enforces the pool's dynamic authorised-pubkey whitelist (fail-closed) |

## Verify before use

Every asset ships with a `.sha256`. After downloading both:

```bash
sha256sum -c qli-worker-ANDROID32-SS-ep234.sha256
```

Only run a binary whose checksum matches.