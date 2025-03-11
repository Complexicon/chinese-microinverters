# Knowledge about the TSUN MS2000(800) Microinverter

- DTU on a seperate board -> HiFlying HF-LPX70 Series
- DTU communicates over UART with the DSP to get information about the individual MPPTs
- DTU firmware is based on the off-the-shelf sdk from hi-flying (which is based on [bl_iot_sdk](https://github.com/bouffalolab/bl_iot_sdk))
- TSUN modified the firmware to include the solarman protocol
- alot of functions related to solarman have the prefix "yz_" and there are some mentions to "yingzhen technology"
- according to [ventureradar](https://www.ventureradar.com/organisation/Wuxi%20Yingzhen%20Technology%20Co_[dot]_,%20Ltd_[dot]_/4cd6169f-7944-450d-8572-bf434c9dd34e) wuxi yingzhen is IGEN Tech which in turn is the main operator or solarmanpv.com - which makes sense
- the upgrade.bin file has a header of "HF-LPx70x1 Image" and the main payload 256 bytes after that is compressed with lzma ([closely related](https://github.com/dasrecht/deye-firmware))
- the main chip of the DTU is most likely a BL602 Risc-V Chip based on the SiFive E24 Core
- the DTU has BLE but is unused?

some known web endpoints in the stock firmware
![image](https://github.com/user-attachments/assets/eca5b65e-689e-430e-a0da-103795c77fab)
![image](https://github.com/user-attachments/assets/f102fabb-b0c7-4bf2-9d3e-ed752e6ce92b)
