# All local manifest
## Repository with my local manifests for android build

Everything listed as "archive" in the branches no longer makes sense.

List of all active branches:

> Daisy: 
- [CrDroid 8.x](https://github.com/WolfAURman/local_manifest/tree/CrDroid8.x-daisy_msm8953)
- [CrDroid 7.x](https://github.com/WolfAURman/local_manifest/tree/CrDroid7.x-daisy_msm8953) *
- [LOS 18.1](https://github.com/WolfAURman/local_manifest/tree/los18.1-daisy_msm8953)

> Lava:
- [CrDroid 9.x](https://github.com/WolfAURman/local_manifest/tree/CrDroid9.x-mt6768-S_V)
- [CrDroid 8.x](https://github.com/WolfAURman/local_manifest/tree/CrDroid8.x-mt6768-S_V)
- [CrDroid 7.x](https://github.com/WolfAURman/local_manifest/tree/crdroid7.x-mt6768PHQ-NewKernel)
- [LOS 20.0](https://github.com/WolfAURman/local_manifest/tree/los20.0-mt6768-S_V)
- [LOS 19.1](https://github.com/WolfAURman/local_manifest/tree/los19.1-mt6768-S_V)
- [LOS 18.1](https://github.com/WolfAURman/local_manifest/tree/los18.1-mt6768PHQ-NewKernel)

> Onclite
- [CrDroid 8.x](https://github.com/WolfAURman/local_manifest/tree/CrDroid8.x-onclite_msm8953)
- [CrDroid 7.x](https://github.com/WolfAURman/local_manifest/tree/los18.1-onclite) *
- [LOS 18.1](https://github.com/WolfAURman/local_manifest/tree/los18.1-onclite)

> Ginkgo
- [CrDroid 9.x](https://github.com/WolfAURman/local_manifest/tree/CrDroid9.x-ginkgo_sm6125)

##

```*``` - When creating these ROMs, use these commands. With stock blobs 8996 from crDroid 7.x version, the screen does not start, but when using from Lineage 18.1, the launch is successful:
```bash
rm -rf hardware/qcom-caf/msm8996/display && git clone https://github.com/LineageOS/android_hardware_qcom_display -b lineage-18.1-caf-msm8996 hardware/qcom-caf/msm8996/display
rm -rf hardware/qcom-caf/msm8996/audio && git clone https://github.com/LineageOS/android_hardware_qcom_audio -b lineage-18.1-caf-msm8996 hardware/qcom-caf/msm8996/audio
rm -rf hardware/qcom-caf/msm8996/media && git clone https://github.com/LineageOS/android_hardware_qcom_media -b lineage-18.1-caf-msm8996 hardware/qcom-caf/msm8996/media
```