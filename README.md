## Repo Init ##
```bash
repo init -u https://github.com/DarknessKiller/android_kernel_manifest.git -b overdose-oneplus-5.4
```
## Sync Source ##
```bash
repo sync --force-sync --no-clone-bundle --current-branch --no-tags -j$(nproc --all)
```
## Build ##
For Clang builds
```bash
BUILD_CONFIG=kernel/msm-5.4/build.config.msm.lahaina VARIANT=qgki LTO=thin BUILD_KERNEL=1 build/build.sh
```

For GCC builds
```bash
BUILD_CONFIG=kernel/msm-5.4/build.config.msm.lahaina VARIANT=qgki COMPILER=gcc BUILD_KERNEL=1 build/build.sh
```
### Submitting Patches ###

Please refer to this for submitting patches: https://github.com/StatiXOS/android_manifest#submitting-patches
