# b4q (SM-F721N Galaxy Z Flip 4) — F721NKSS8IZE2

## Firmware Identity

```
model: SM-F721N
region: S (KOR)
AP/PDA: F721NKSS8IZE2
display build: BP2A.250605.031.A3.F721NKSS8IZE2
fingerprint: samsung/b4qksx/b4q:16/BP2A.250605.031.A3/F721NKSS8IZE2:user/release-keys
kernel release: 5.10.236-android12-9-31998796-abF721NKSS8IZE2
```

## Kernel Image (extracted 2026-09-04)

- **Kernel SHA-256:** `911D0A87F4CEDABDD6C578675CDE4C8285943AD471CB6499590324AF963D48C3`
- **Kernel size:** 41,421,312 bytes (39.5 MB)
- **ARM64 Image text_offset:** 0x0 (standard ARM64 layout)
- **ARM64 Image flags:** 0x293ff20
- **BTF:** Not present in kernel image (no BTF blob found)
- **Symbols:** All derived from `vmlinux-to-elf` (112,071 symbols)

## Offsets Summary (relative to KIMAGE_TEXT_BASE 0xffffffc008000000)

| Symbol | Offset | Absolute Address |
|---|---|---|
| `init_task` | +0x0258c000 | 0xffffffc00a58c000 |
| `root_task_group` | +0x0278a040 | 0xffffffc00a78a040 |
| `selinux_state` | +0x028bba68 | 0xffffffc00a8bba68 |
| `kmalloc_caches` | +0x020baa20 | 0xffffffc00a0baa20 |
| `system_unbound_wq` | +0x02579e08 | 0xffffffc00a579e08 |
| `call_usermodehelper_exec_work` | +0x001086b4 | 0xffffffc0081086b4 |
| `ashmem_misc.fops` | +0x026db7a8 | 0xffffffc00a6db7a8 |
| `ashmem_fops` | +0x02078838 | 0xffffffc00a078838 |
| `ashmem_ioctl` | +0x01115d58 | 0xffffffc009115d58 |
| `ashmem_compat_ioctl` | +0x01116824 | 0xffffffc009116824 |
| `ashmem_mmap` | +0x0111687c | 0xffffffc00911687c |
| `ashmem_open` | +0x01116aac | 0xffffffc009116aac |
| `ashmem_release` | +0x01116b44 | 0xffffffc009116b44 |
| `ashmem_show_fdinfo` | +0x01116c60 | 0xffffffc009116c60 |
| `ashmem_llseek` | +0x01115bb8 | 0xffffffc009115bb8 |
| `configfs_read_file` | +0x006040d8 | 0xffffffc0086040d8 |
| `configfs_write_bin_file` | +0x00604a68 | 0xffffffc008604a68 |
| `generic_file_splice_read` | +0x0053866c | 0xffffffc00853866c |
| `noop_llseek` | +0x004c3694 | 0xffffffc0084c3694 |
| `nfulnl_logger` | +0x02581340 | 0xffffffc00a581340 |
| `loggers` | +0x02581268 | 0xffffffc00a581268 |
| `random_table` | +0x0269b4c8 | 0xffffffc00a69b4c8 |
| `sysctl_bootid` | +0x0295bac5 | 0xffffffc00a95bac5 |
| `anon_pipe_buf_ops` | +0x01efbba8 | 0xffffffc009efbba8 |
| `"nfnetlink_log"` string | +0x01dc7d90 | 0xffffffc009dc7d90 |

## Porting Status: COMPLETE (offsets derived)

All critical offsets extracted from `vmlinux-to-elf` of the exact firmware kernel image.

## TODO

1. Build exploit with `make TARGET=b4q-F721NKSS8IZE2 release`
2. Build KernelSU module for KMI `android12-5.10` (see kernelsu/README.md)
3. Generate P0 fingerprint table from target kernel (PORTING.md §5)
4. Derive `SLIDE_TRACEFS_EVENT_ID` and `SLIDE_TRACEFS_WORKER_CALLER_OFF` from trace events
5. Verify `SLIDE_RANDOM_TABLE_BOOT_ID_DATA_PTR_OFF` (offset within random_table[] for boot_id entry)
6. Verify on hardware — test full chain + re-verification

## References

- [PORTING.md](../../docs/PORTING.md) — Full porting procedure
- [vmlinux.nm](../../../../vmlinux.nm) — Full symbol table from extracted kernel
