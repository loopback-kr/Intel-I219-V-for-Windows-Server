## Intel Ethernet Connection I219-V driver installation for Windows Server

### System requirements
* Windows Server 2012
* Windows Server 2012 R2
* Windows Server 2016
* Windows Server 2019
* Windows Server 2022
* Windows Server 2025

### Driver version
* Update: 26.4 (2021-07-22)
* SHA1: 90694EA1D4DB9CDDE243CB28B4BC42759D60A07B
* Update: 30.0 (2025-01-21)
* SHA1: 1F1DA97C4D9ADF41251361F3907EF94C5FB42E9F

### Modifications
* Deleted all files except the I219-V driver files.
* Modified `e1d.inf` files based on server version.

### Supported operating systems by each directory
* PRO1000/Winx64/NDIS63: Windows Server 2012 (v26.4)
* PRO1000/Winx64/NDIS64: Windows Server 2012 R2 (v26.4)
* PRO1000/Winx64/NDIS65: Windows Server 2016 (v30.0)
* PRO1000/Winx64/NDIS68: Windows Server 2019 (v30.0)
* PRO1000/Winx64/WS2022: Windows Server 2022 (v30.0)
* PRO1000/Winx64/WS2025: Windows Server 2025 (v30.0)

### Instructions
1. Run `ENABLE_TESTMODE.cmd` to reboot as test signing mode.
2. Open `devmgmt.msc`.
3. Select the Ethernet Controller in Other devices.
4. Click the Driver update button.
5. Find the driver manually.
6. Choose directly from the list of available drivers.
7. Select the `NDIS*/e1d*x64.inf` or `NDIS*/e1d.inf` file in the directory for current Windows Server version.
8. Select `Intel(R) Ethernet Connection (2) I219-V` from the driver list.
9. Continue and finish installation even if an unsigned driver installation warning appears.
10. Run `DISABLE_TESTMODE.cmd` to reboot as standard signing mode.