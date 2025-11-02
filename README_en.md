Japanese version is here: [README.md](README.md)

# Global-Shutter MIPI High-Speed Camera (PYTHON300 + Spartan-7)

## Overview

This repository provides the KiCad design data for the global-shutter MIPI high-speed camera introduced [here](https://rtc-lab.com/products/rtcl-cam-p3s7-mipi/).

This is a compact, R&D-oriented camera module built with the onsemi [PYTHON300 image sensor](https://www.onsemi.com/products/sensors/image-sensors/python300) and the AMD (Xilinx) [Spartan-7 FPGA](https://www.amd.com/en/products/adaptive-socs-and-fpgas/fpga/spartan-7.html).


Although the sensor is VGA-class on the datasheet and rated for up to 815 fps, we have achieved 1000 fps capture at 320×320 when connected to a [KV260](https://www.amd.com/en/products/system-on-modules/kria/k26/kv260-vision-starter-kit.html) or [Zybo Z7](https://digilent.com/shop/zybo-z7-zynq-7000-arm-fpga-soc-development-board/).

Sample videos and more details are also introduced [here](https://rtc-lab.com/products/rtcl-cam-p3s7-mipi/).


## Schematics

Schematics are available below:

- [Image sensor daughterboard](sensor_python300/sensor_python300.pdf)
- [FPGA baseboard](mipi_spartan7/mipi_spartan7.pdf)

![Camera Photo](docs/images/camera_photo.png)

## Board Sales

We sell manufactured boards on [BOOTH](https://rtc-lab.booth.pm/).

- [Monochrome version](https://rtc-lab.booth.pm/items/7427869)
- [Color version](https://rtc-lab.booth.pm/items/7428802)

## Related Software

Currently, there is a project that sends data to the KV260 using a custom specification.

- [Spartan-7 Design](https://github.com/ryuz/rtcl-designs/tree/main/projects/rtcl_p3s7_mipi/rtcl_p3s7_mipi)
- [KV260 Design](https://github.com/ryuz/rtcl-designs/tree/main/projects/kv260/kv260_rtcl_p3s7_hs)
- [ZYBO Design](https://github.com/ryuz/rtcl-designs/tree/main/projects/zybo_z7/zybo_z7_rtcl_p3s7_hs)

## Repository Structure

| Directory        | Description                                                |
|:-----------------|:-----------------------------------------------------------|
| mipi_spartan7    | Project for the baseboard carrying the Spartan-7 FPGA      |
| sensor_python300 | Project for the daughterboard carrying the PYTHON300 sensor |
| sensor_mipi      | Combined panelized project for manufacturing base and daughter boards |

## Disclaimer

These design files are provided for prototyping and research/development experiments. The author assumes no responsibility or liability for any damages arising from their use.

## License

This work is licensed under the [Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)](https://creativecommons.org/licenses/by-nc/4.0/).

You may freely use the design for hobby or research purposes, as long as you do not sell or distribute the manufactured boards without permission.

If you wish to manufacture and sell this design commercially, please contact the author to arrange a separate license agreement. You can reach us via the [contact form](https://rtc-lab.com/contact/).

## Author

Ryuji Fuchikami  
[Real-Time Computing Laboratory](https://rtc-lab.com/)
