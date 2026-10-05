# wasm-builds

Prebuilt machines for browser-based wasm computers. Each release asset is one machine: a restore snapshot plus a content-addressed disk store, ready to unpack next to a static site that loads them.

| Machine | Desktop | Guest RAM | Asset |
|---|---|---|---|
| Alpine Desktop | JWM, xterm, NetSurf, Thunar | 256 MB | `alpine-desktop.tar` |
| Debian Desktop (trixie, i386) | JWM, xterm, NetSurf, Thunar | 256 MB | `debian-desktop.tar` |
| Kali Desktop (kali-rolling, i386) | JWM, NetSurf, nmap, sqlmap, john and more | 256 MB | `kali-desktop.tar` |
| Alpine Desktop Plus | Alpine desktop plus Firefox ESR (full JavaScript; slow cold start) | 768 MB | `alpine-desktop-plus.tar` (v2) |
| Arch Linux 32 Desktop | IceWM, xterm, dillo, Thunar | 256 MB | `wasmarch-desktop.tar` (v2) |

Verify with `sha256sum -c SHA256SUMS`. Kali tools are for labs and CTFs on systems you own or are allowed to test.
Machines are built from free software only and contain no commercial games, firmware or media.
