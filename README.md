# wasm-builds

Prebuilt machines for browser-based wasm computers. Each release asset is one machine: a restore snapshot plus a content-addressed disk store, ready to unpack next to a static site that loads them.

| Machine | Desktop | Guest RAM | Asset |
|---|---|---|---|
| Alpine Desktop | JWM, xterm, NetSurf, Thunar | 256 MB | `alpine-desktop.tar` |
| Debian Desktop (trixie, i386) | JWM, xterm, NetSurf, Thunar | 256 MB | `debian-desktop.tar` |
| Kali Desktop (kali-rolling, i386) | JWM, NetSurf, nmap, sqlmap, john and more | 256 MB | `kali-desktop.tar` |
| Alpine Desktop Plus | Alpine desktop plus Firefox ESR (full JavaScript; slow cold start) | 768 MB | `alpine-desktop-plus.tar` (v2) |
| Arch Linux 32 Desktop | IceWM, xterm, dillo, Thunar | 256 MB | `wasmarch-desktop.tar` (v2) |
| Alpine + Node (i386) | Headless, node/npm/python preinstalled | 256 MB | `alpine-node.tar` (v3) |
| Debian 13 (i386) | Headless (trixie) | 256 MB | `debian-i386.tar` (v4) |
| Ubuntu 24.04 (i386, unofficial) | Headless | 256 MB | `ubuntu-2404-i386.tar` (v4) |
| Kali Linux (i386, real kali-rolling userland) | Headless, nmap/sqlmap/john/hydra and more | 384 MB | `kali-i386.tar` (v5) |
| Alpine Linux 3.21 (x86_64, musl, QEMU) | Headless, node/npm/python preinstalled, real 64-bit CPU via `qemu-system-x86_64` | 256 MB | `alpine64-qemu.tar` (v3) |
| Alpine Linux 3.21 (riscv64, musl, QEMU) | Headless, node/npm/python preinstalled | 256 MB | `riscv64-alpine-qemu.tar` (v3) |
| Arch Linux 32 (headless) | wasmport's own lean archlinux32 derivative, no base/kernel/firmware bloat | 256 MB | `wasmarch.tar` (v4) |

### Kali addons (apply to `kali-i386` or `kali-desktop`)

Static flat apt repos — `apt-get update && apt-get install <package>` once the repo's on your PATH, or `kali-get --offline=<host> <package>`. Install-and-version-check only; nothing in these bundles was run against any target.

| Addon | Adds | Size | Asset |
|---|---|---|---|
| exploitdb | `exploitdb` | 30.5 MB | `kali-addon-exploitdb.tar` (v3) |
| hashcat | `hashcat` | 118.9 MB | `kali-addon-hashcat.tar` (v3) |
| metasploit | `metasploit-framework` | 473.3 MB | `kali-addon-metasploit.tar` (v5) |
| web | `whatweb`, `wpscan` | 12.9 MB | `kali-addon-web.tar` (v3) |
| wireless | `aircrack-ng`, `wifite` | 2.7 MB | `kali-addon-wireless.tar` (v3) |
| wordlists | `wordlists` | 55.4 MB | `kali-addon-wordlists.tar` (v3) |

Verify with `sha256sum -c SHA256SUMS`. Kali tools are for labs and CTFs on systems you own or are allowed to test.
Machines are built from free software only and contain no commercial games, firmware or media.
