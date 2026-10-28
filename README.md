# OrangeFox Recovery Manifests for Samsung Galaxy M20 (`m20lte`)

This repository contains the manifest and local manifest definitions for syncing and building **OrangeFox Recovery** (`fox_12.1`) for Samsung Galaxy M20 (`m20lte`).

## Included Repositories

- **Device Tree**: [`txorav/device_samsung_m20lte`](https://github.com/txorav/device_samsung_m20lte) (Branch `fox_12.1`)
- **Kernel Tree**: [`txorav/kernel_samsung_m20lte`](https://github.com/txorav/kernel_samsung_m20lte) (Branch `lineage-17.1`)
- **Samsung DT mkbootimg**: [`LineageOS/android_system_tools_mkbootimg`](https://github.com/LineageOS/android_system_tools_mkbootimg) (Branch `lineage-19.1`)

## Usage

### 1. Using as Local Manifest with OrangeFox Sync
```bash
mkdir -p .repo/local_manifests
curl -fsSL https://raw.githubusercontent.com/txorav/orangefox_manifest/fox_12.1/m20lte.xml -o .repo/local_manifests/m20lte.xml
repo sync
```

### 2. Building OrangeFox
```bash
source build/envsetup.sh
lunch twrp_m20lte-eng
mka recoveryimage
```
