[<center><img src="https://raw.githubusercontent.com/sourajitk/STX-Logo/main/stx-2021-kernel.png" height="50%" width="50%;" /></center>](https://github.com/StatiXOS)

## Repo Init ##
```bash
repo init -u https://github.com/StatiXOS/android_kernel_manifest.git -b android-msm-davinci-5.10-android12
```
## Sync Source ##
```bash
repo sync --force-sync --no-clone-bundle --current-branch --no-tags -j$(nproc --all)
```
## Building Kernel ##
```bash
BUILD_KERNEL=1 ./build_ai2202.sh
```
### Submitting Patches ###
Please refer to this for submitting patches: https://github.com/StatiXOS/android_manifest#submitting-patches
