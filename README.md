# armbian-onecloud
[![build](https://img.shields.io/github/actions/workflow/status/hzyitc/armbian-onecloud/ci.yml)](https://github.com/hzyitc/armbian-onecloud/actions/workflows/ci.yml) [![downloads](https://img.shields.io/github/downloads/hzyitc/armbian-onecloud/total)](https://github.com/hzyitc/armbian-onecloud/releases) [![downloads@latest](https://img.shields.io/github/downloads/hzyitc/armbian-onecloud/latest/total)](https://github.com/hzyitc/armbian-onecloud/releases/latest)

[README](README.md)[中文文档](README_zh.md)

**All modifications have been submitted to [the official repository](https://github.com/armbian/build) and you can directly use the official repository for compilation.**

This project is modified based on ['hzyitc/armbian-onecloud'](https://github.com/hzyitc/armbian-onecloud) online, thank you to ['hzyit'](https://github.com/hzyitc).

## First-time login

`onecloud`

`root`

`1234`

## Build parameters

### `BOARD`=`onecloud`

### `BRANCH`=`current`

| BRANCH    | KERNEL VERSION | eMMC | HDMI | VPU |
| :-:       | :-:            | :-:  | :-:  | :-: |
| `current` | `v6.12`        ||||

>
>
>

## Boot from `u-boot` 

### Boot from `USB`

```
setenv bootdev "usb 0"
usb start
fatload ${bootdev} 0x20800000 boot.scr && autoscr 0x20800000
```

### Boot from `eMMC`

```
setenv bootdev "mmc 1"
fatload ${bootdev} 0x20800000 boot.scr && autoscr 0x20800000
```

## GPIO

`SoC``GPIO`

`dts``patch/kernel/archive/meson-6.12/onecloud-0001-add-dts.patch`

`dts``V1.0 board`

## Related link

[`armbian/build`](https://github.com/armbian/build)

[`xdarklight/linux@meson-mx-integration-5.18-20220417`](https://github.com/xdarklight/linux/tree/meson-mx-integration-5.18-20220417)`HDMI`

[`S805_Datasheet V0.8 20150126.pdf`](https://dn.odroid.com/S805/Datasheet/S805_Datasheet%20V0.8%2020150126.pdf)





