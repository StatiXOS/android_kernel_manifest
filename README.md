[<center><img src="https://raw.githubusercontent.com/sourajitk/STX-Logo/main/stx-2021-kernel.png" height="50%" width="50%;" /></center>](https://github.com/StatiXOS)

## Repo Init ##

```bash
repo init -u https://github.com/StatiXOS/android_kernel_manifest.git -b android-msm-xiaomi-4.19-android11
```

## Sync Source ##

```bash
repo sync --force-sync --no-clone-bundle --current-branch --no-tags -j$(nproc --all)
```

## Build ##

Rename `DEVICE_NAME` with the appropriate device codename

For Clang builds
```bash
BUILD_CONFIG=build.config.xiaomi.${DEVICE_NAME} BUILD_KERNEL=1 build/build.sh
```
Clang Extras:
* Pass `LTO=full|thin` to build with full clang LTO or thinLTO respectively.

For GCC builds
```bash
BUILD_CONFIG=build.config.xiaomi.${DEVICE_NAME} COMPILER=gcc BUILD_KERNEL=1 build/build.sh
```

GCC Extras:
* Pass `GCC_LTO=1` to build with full GCC LTO.

Example:

For alioth with GCC LTO
```bash
BUILD_CONFIG=build.config.xiaomi.alioth COMPILER=gcc GCC_LTO=1 BUILD_KERNEL=1 build/build.sh
```

### Submitting Patches ###

Please refer to this for submitting patches: https://github.com/StatiXOS/android_manifest#submitting-patches
