# Silicium UEFI for Xiaomi Mi 8 (dipper)

Fork of [Project Silicium](https://github.com/Project-Silicium/Mu-Silicium) tailored specifically for **Xiaomi Mi 8 (dipper)** running Snapdragon 845 (SDM845), with direct support for booting HakiOS / XNU.

## Features

- Lightweight: all non-dipper platforms and bloated submodules stripped out
- Pre-configured memory map and ACPI tables for Xiaomi Mi 8
- Supports building `Mu-dipper.img` (fastboot bootable UEFI image)
- Includes BootShim with XNU loader compatibility

## Building

```bash
# Setup environment
./setup_env.sh

# Build UEFI for Xiaomi Mi 8
.venv/bin/python3 build_uefi.py -d dipper
```

Output binary: `Mu-dipper.img`

## Booting

Boot the generated UEFI image on your phone via fastboot:

```bash
fastboot boot Mu-dipper.img
```
