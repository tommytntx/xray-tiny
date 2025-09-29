# Xray for ARMv5 (armel) — UPX Compressed Build

This repository provides **precompiled Xray binaries** for legacy ARMv5 (armel) devices.  
The binaries are statically built with Go, stripped of debug symbols, and compressed with [UPX](https://upx.github.io/) to minimize size.  
They are intended for constrained environments where storage space is limited (e.g., 128 MB flash).

---

## Features
- **Architecture**: `linux/arm/v5` (soft-float / armel)
- **Protocols supported**:  
  - VLESS (with REALITY, Vision flow)  
  - VMess  
  - Trojan  
  - Socks, HTTP, Dokodemo-door  
  - DNS (DoH/DoT/DoQ)  
- **Compression**: UPX-packed binary to reduce disk footprint
- **Usage**: standalone binary or inside a minimal Docker container

---

## Downloads
You can find the latest binaries in the [Releases](https://github.com/tommytntx/xray-tiny/releases) section.

Example (direct link to release asset):

```bash
curl -L -o xray \
  https://github.com/tommytntx/xray-tiny/releases/download/25.9.11-upx-armv5/xray
chmod +x xray
./xray -version
