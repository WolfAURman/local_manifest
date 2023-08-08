# All local manifest
## Repository with my local manifests for android build

Everything listed as "archive" in the branches no longer makes sense.

List of all active branches:

> Daisy: 
- [CrDroid 9.x](https://github.com/WolfAURman/local_manifest/tree/CrDroid9.x-daisy_msm8953) ***
- [CrDroid 8.x](https://github.com/WolfAURman/local_manifest/tree/CrDroid8.x-daisy_msm8953) **
- [CrDroid 7.x](https://github.com/WolfAURman/local_manifest/tree/CrDroid7.x-daisy_msm8953) *
- [LOS 18.1](https://github.com/WolfAURman/local_manifest/tree/los18.1-daisy_msm8953)

> Lava:
- [CrDroid 9.x](https://github.com/WolfAURman/local_manifest/tree/CrDroid9.x-mt6768-S_V)
- [CrDroid 8.x](https://github.com/WolfAURman/local_manifest/tree/CrDroid8.x-mt6768-S_V) S vendor | [CrDroid 8.x](https://github.com/WolfAURman/local_manifest/blob/crdroid8.x-mt6768PHQ_archive/local_manifest.xml) R vendor
- [CrDroid 7.x](https://github.com/WolfAURman/local_manifest/tree/crdroid7.x-mt6768PHQ-NewKernel)
- [LOS 20.0](https://github.com/WolfAURman/local_manifest/tree/los20.0-mt6768-S_V)
- [LOS 19.1](https://github.com/WolfAURman/local_manifest/tree/los19.1-mt6768-S_V) S vendor | [LOS 19.1](https://github.com/WolfAURman/local_manifest/blob/los19.1-mt6768PHQ_archive/local_manifest.xml) R vendor
- [LOS 18.1](https://github.com/WolfAURman/local_manifest/tree/los18.1-mt6768PHQ-NewKernel)

> Onclite
- [CrDroid 9.x](https://github.com/WolfAURman/local_manifest/tree/CrDroid9.x-onclite_msm8953) ***
- [CrDroid 8.x](https://github.com/WolfAURman/local_manifest/tree/CrDroid8.x-onclite_msm8953) **
- [CrDroid 7.x](https://github.com/WolfAURman/local_manifest/tree/los18.1-onclite) *
- [LOS 18.1](https://github.com/WolfAURman/local_manifest/tree/los18.1-onclite)

> Ginkgo
- [CrDroid 9.x](https://github.com/WolfAURman/local_manifest/tree/CrDroid9.x-ginkgo_sm6125)

> Jason
- [CrDroid 8.x](https://github.com/WolfAURman/local_manifest/blob/CrDroid8.x-jason_sdm660/local_manifest.xml)

> Sakura:
- [CrDroid 9.x](https://github.com/WolfAURman/local_manifest/tree/CrDroid9.x-sakura_msm8953) ****

##

```*``` - When creating these ROMs, use these commands. With stock blobs 8996 from crDroid 7.x version, the screen does not start, but when using from Lineage 18.1, the launch is successful:
```bash
rm -rf hardware/qcom-caf/msm8996/display && git clone https://github.com/LineageOS/android_hardware_qcom_display -b lineage-18.1-caf-msm8996 hardware/qcom-caf/msm8996/display
rm -rf hardware/qcom-caf/msm8996/audio && git clone https://github.com/LineageOS/android_hardware_qcom_audio -b lineage-18.1-caf-msm8996 hardware/qcom-caf/msm8996/audio
rm -rf hardware/qcom-caf/msm8996/media && git clone https://github.com/LineageOS/android_hardware_qcom_media -b lineage-18.1-caf-msm8996 hardware/qcom-caf/msm8996/media
```

Or one line:
```bash
rm -rf hardware/qcom-caf/msm8996/display && git clone https://github.com/LineageOS/android_hardware_qcom_display -b lineage-18.1-caf-msm8996 hardware/qcom-caf/msm8996/display && rm -rf hardware/qcom-caf/msm8996/audio && git clone https://github.com/LineageOS/android_hardware_qcom_audio -b lineage-18.1-caf-msm8996 hardware/qcom-caf/msm8996/audio && rm -rf hardware/qcom-caf/msm8996/media && git clone https://github.com/LineageOS/android_hardware_qcom_media -b lineage-18.1-caf-msm8996 hardware/qcom-caf/msm8996/media
```

If you don't need these repositories anymore:
```bash
rm -rf hardware/qcom-caf/msm8996/display && rm -rf hardware/qcom-caf/msm8996/audio && rm -rf hardware/qcom-caf/msm8996/media
```

##

```**``` - To create these ROMs, you need to clone this repository that is not present in CrDroid:
```bash
git clone https://github.com/LineageOS/android_hardware_xiaomi -b lineage-19.1 hardware/xiaomi
```

##

```***``` - To create these ROMs, you need to clone this repository that is not present in CrDroid:
```bash
git clone https://github.com/LineageOS/android_hardware_xiaomi -b lineage-20 hardware/xiaomi
```

##

```****``` - To create this ROM you will need to replace the repository:
```bash
rm -rf device/qcom/sepolicy-legacy-um && git clone https://github.com/Dev-msm8953/platform_device_qcom_sepolicy-legacy-um device/qcom/sepolicy-legacy-um
```

## Clone branch:

<details><summary>Daisy:</summary>

> crDroid:

crDroid 9
```bash
rm -rf .repo/local_manifests && curl -o .repo/local_manifests/local_manifest.xml https://raw.githubusercontent.com/WolfAURman/local_manifest/CrDroid9.x-daisy_msm8953/local_manifest.xml --create-dirs
```

crDroid 8
```bash
rm -rf .repo/local_manifests && curl -o .repo/local_manifests/local_manifest.xml https://raw.githubusercontent.com/WolfAURman/local_manifest/CrDroid8.x-daisy_msm8953/local_manifest.xml --create-dirs
```

crDroid 7
```bash
rm -rf .repo/local_manifests && curl -o .repo/local_manifests/local_manifest.xml https://raw.githubusercontent.com/WolfAURman/local_manifest/CrDroid7.x-daisy_msm8953/local_manifest.xml --create-dirs
```
> LineageOS:

LineageOS 18.1
```bash
rm -rf .repo/local_manifests && curl -o .repo/local_manifests/local_manifest.xml https://raw.githubusercontent.com/WolfAURman/local_manifest/los18.1-daisy_msm8953/local_manifest.xml --create-dirs
```
</details>

<details><summary>Lava:</summary>

>crDroid:

crDroid 9
```bash
rm -rf .repo/local_manifests && curl -o .repo/local_manifests/local_manifest.xml https://raw.githubusercontent.com/WolfAURman/local_manifest/CrDroid9.x-mt6768-S_V/local_manifest.xml --create-dirs
```

crDroid 8 S vendor
```bash
rm -rf .repo/local_manifests && curl -o .repo/local_manifests/local_manifest.xml https://raw.githubusercontent.com/WolfAURman/local_manifest/CrDroid8.x-mt6768-S_V/local_manifest.xml --create-dirs
```

crDroid 8 R vendor
```bash
rm -rf .repo/local_manifests && curl -o .repo/local_manifests/local_manifest.xml https://raw.githubusercontent.com/WolfAURman/local_manifest/crdroid8.x-mt6768PHQ_archive/local_manifest.xml --create-dirs
```

crDroid 7
```bash
rm -rf .repo/local_manifests && curl -o .repo/local_manifests/local_manifest.xml https://raw.githubusercontent.com/WolfAURman/local_manifest/crdroid7.x-mt6768PHQ-NewKernel/local_manifest.xml --create-dirs
```

> LineageOS:

LineageOS 20
```bash
rm -rf .repo/local_manifests && curl -o .repo/local_manifests/local_manifest.xml https://raw.githubusercontent.com/WolfAURman/local_manifest/los20.0-mt6768-S_V/local_manifest.xml --create-dirs
```

LineageOS 19.1 S vendor
```bash
rm -rf .repo/local_manifests && curl -o .repo/local_manifests/local_manifest.xml https://raw.githubusercontent.com/WolfAURman/local_manifest/los19.1-mt6768-S_V/local_manifest.xml --create-dirs
```

LineageOS 19.1 R vendor
```bash
rm -rf .repo/local_manifests && curl -o .repo/local_manifests/local_manifest.xml https://raw.githubusercontent.com/WolfAURman/local_manifest/los19.1-mt6768PHQ_archive/local_manifest.xml --create-dirs
```

LineageOS 18.1
```bash
rm -rf .repo/local_manifests && curl -o .repo/local_manifests/local_manifest.xml https://raw.githubusercontent.com/WolfAURman/local_manifest/los18.1-mt6768PHQ-NewKernel/local_manifest.xml --create-dirs
```
</details>

<details><summary>Onclite:</summary>

>crDroid:

crDroid 9
```bash
rm -rf .repo/local_manifests && curl -o .repo/local_manifests/local_manifest.xml https://raw.githubusercontent.com/WolfAURman/local_manifest/CrDroid9.x-onclite_msm8953/local_manifest.xml --create-dirs
```

crDroid 8
```bash
rm -rf .repo/local_manifests && curl -o .repo/local_manifests/local_manifest.xml https://raw.githubusercontent.com/WolfAURman/local_manifest/CrDroid8.x-onclite_msm8953/local_manifest.xml --create-dirs
```

crDroid 7
```bash
rm -rf .repo/local_manifests && curl -o .repo/local_manifests/local_manifest.xml https://raw.githubusercontent.com/WolfAURman/local_manifest/los18.1-onclite/local_manifest.xml --create-dirs
```

> LineageOS:

LineageOS 18.1
```bash
rm -rf .repo/local_manifests && curl -o .repo/local_manifests/local_manifest.xml https://raw.githubusercontent.com/WolfAURman/local_manifest/los18.1-onclite/local_manifest.xml --create-dirs
```
</details>

## Synchronizing repositories:

```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```