# Intel I219-V Ethernet driver installation for Windows Server

## System requirements
* Windows Server 2012
* Windows Server 2012 R2
* Windows Server 2016
* Windows Server 2019
* Windows Server 2022

## Driver version
* Update: 26.4 (2021-07-22)
* SHA1: 90694EA1D4DB9CDDE243CB28B4BC42759D60A07B

## modifications
* Deleted all files except the I219-V driver files.
* Modified *.inf files for installation in Windows Server

## Supported operating systems by each directory
* NDIS63: Windows Server 2012
* NDIS64: Windows Server 2012 R2
* NDIS65: Windows Server 2016
* NDIS68: Windows Server 2019, Windows Server 2022

## Instructions
1. Run `ENABLE_TESTMODE.cmd` to reboot as test signing mode.
2. Open `devmgmt.msc`.
3. Select the Ethernet Controller in Other devices.
4. Click the Driver update button.
5. Find the driver manually.
6. Choose directly from the list of available drivers.
7. Select the `NDIS*/e1d*x64.inf` file in the directory for current Windows Server version
8. Select `Intel(R) Ethernet Connection (2) I219-V` from the driver list
9. Continue and finish installation even if an unsigned driver installation warning appears.
10. Run `DISABLE_TESTMODE.cmd` to reboot as standard signing mode.