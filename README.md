[<center><img src="https://raw.githubusercontent.com/sourajitk/STX-Logo/main/stx-2021-kernel.png" height="50%" width="50%;" /></center>](https://github.com/StatiXOS)

## Repo Init ##
```bash
repo init -u https://github.com/StatiXOS/android_kernel_manifest.git -b android-msm-sake-5.4-android11-lts
```
## Sync Source ##
```bash
repo sync --force-sync --no-clone-bundle --current-branch --no-tags -j$(nproc --all)
```
## Build ##
For GCC builds (recommended)
```bash
BUILD_CONFIG=private/asus-msm-5.4/build.config.sake BUILD_KERNEL=1 BUILD_DT=1 build/build.sh
```
### Submitting Patches ###

Please refer to this for submitting patches: https://github.com/StatiXOS/android_manifest#submitting-patches
