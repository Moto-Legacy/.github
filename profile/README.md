# Moto Legacy

Current Android on old Motorola phones.

We bring LineageOS releases to Motorola devices that were left behind years
ago, keeping their original kernels running and patching Android to cope with
what those kernels lack.

## Devices

| Device | Codename | SoC | Kernel | LineageOS | Status |
| --- | --- | --- | --- | --- | --- |
| Moto G (2013) | `falcon` | MSM8226 | 3.4 | 23.2 (Android 16) | Boots to the setup wizard and Settings, adb (root) |
| Moto G LTE (2013) | `peregrine` | MSM8226 | 3.4 | 23.2 (Android 16) | Same tree as falcon; retrofit dynamic partitions not tested on a device yet |

Not daily driver material yet: the UI is slow and the radio, camera and compass
still don't work.

## Repositories

| Repository | What |
| --- | --- |
| [`local_manifests`](https://github.com/Moto-Legacy/local_manifests) | Local manifests for each LineageOS release |
| [`patches`](https://github.com/Moto-Legacy/patches) | Platform and kernel patches for Linux 3.4 kernels (no eBPF, none of the syscalls Android 16 takes for granted) |
| [`android_device_motorola_msm8226-common`](https://github.com/Moto-Legacy/android_device_motorola_msm8226-common) | Common MSM8226 device tree |
| [`android_device_motorola_falcon`](https://github.com/Moto-Legacy/android_device_motorola_falcon) | Moto G (2013) device tree |
| [`android_device_motorola_peregrine`](https://github.com/Moto-Legacy/android_device_motorola_peregrine) | Moto G LTE device tree |
| [`android_kernel_motorola_msm8226`](https://github.com/Moto-Legacy/android_kernel_motorola_msm8226) | Linux 3.4 kernel for MSM8226 Motorola devices |
| [`proprietary_vendor_motorola`](https://github.com/Moto-Legacy/proprietary_vendor_motorola) | Proprietary files |
| [`twrp-super`](https://github.com/Moto-Legacy/twrp-super) | Makes the official TWRP find the retrofit `super` partition, to install the ROMs |

## Building

Start with [`patches`](https://github.com/Moto-Legacy/patches#readme): it has
the full build guide (sync, patching and building).

## Credits

These ports stand on the work of many people, credited in each repository:
the [legacy_support_patches](https://github.com/Ultra-Legacy-Hippeastrum/legacy_support_patches)
maintainers, the TrebleDroid BPF-less work picked from
[MisterZtr/LineageOS_gsi](https://github.com/MisterZtr/LineageOS_gsi), the
original device and kernel maintainers, and the LineageOS project.

Motorola is a trademark of Motorola Mobility LLC. This project is not
affiliated with or endorsed by Motorola.
