# Galaxy Z Flip 4 (SM-F721N) — F721NKSS8IZE2

## Device Info

- **Model:** SM-F721N
- **Codename:** b4q
- **Region:** S (KOR)
- **Display:** BP2A.250605.031.A3.F721NKSS8IZE2
- **Fingerprint:** samsung/b4qksx/b4q:16/BP2A.250605.031.A3/F721NKSS8IZE2:user/release-keys
- **Kernel:** 5.10.236-android12-9-31998796-abF721NKSS8IZE2
- **SoC:** Snapdragon 8 Gen 1 (SM8450)
- **Android:** 16 (API 36)
- **ABI:** arm64-v8a

## Kernel Image (extracted from firmware)

- **Kernel SHA-256:** `911D0A87F4CEDABDD6C578675CDE4C8285943AD471CB6499590324AF963D48C3`
- **Kernel size:** 41,421,312 bytes (39.5 MB)
- **Boot.img SHA-256:** `58780806438B7268286A8EC7AB40936E499BFD0F9E94F159C4B65645E798BA71`
- **text_offset:** 0x0 (standard ARM64)

## Artifacts

| File | SHA-256 | Size | Notes |
|---|---|---|---|
| `cve-2026-43499-app.so` | `05eb726d38820767778c86f9e43294beefb6f352e596c196ad9019f1e062a5cc` | 104,128 B | Exploit payload (APP_PAYLOAD build) |
| `android12-5.10_kernelsu-b4q-F721NKSS8IZE2-kdp.ko` | `23ca2a7c3f9bb36133003348ae15099e7bc4dcae02c96604988359ffa6107d6d` | 361,280 B | KernelSU module (KMI: android12-5.10, vermagic: 5.10.226-android12-9-31117096) |
| `ksud-b4q-F721NKSS8IZE2-kdp` | `727eecc25bb03d4fef3301de137ec13391da51bca5e701c842033cd270b781ba` | 6,649,032 B | KernelSU late-load binary (KMI: android12-5.10) |

## Build Notes

- Kernel version: 5.10.236 (KMI: android12-5.10)
- No BTF in kernel image — all offsets derived from vmlinux-to-elf
- 112,071 symbols extracted via llvm-nm
- Snapdragon 8 Gen 1 (SM8450) — same SoC family as Z Fold4 (q4q/S22U)
- Offsets derived from exact firmware kernel, not copied from other devices

## Hardware Test Record

- Device verified: TODO
- Status: Payload built, needs hardware verification
