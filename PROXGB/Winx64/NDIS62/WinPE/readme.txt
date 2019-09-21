Setting up Intel(R) 10GbE Network Connection Drivers for Micorsoft* Windows* PE
===============================================================================
To set up network drivers for Microsoft* Windows* PE, you must import files from
the Intel(R) Network Connections Software CD to the Windows PE image. Follow the
directions for your operating system.
 
32-bit Microsoft Windows PE V3
==============================
1. Create a temporary directory (for example, c:\temp\winpe).
 
2. Copy all files from the PROXGB\Win32\NDIS62\WinPE directory to the temporary
   directory.
 
3. Extract the driver inf file (for example: ixe6232.inf) from
   PROXGB\Win32\NDIS62\WinPE\*.zip to the temporary directory.
 
4. Use the /Add-Driver option of the DISM.exe tool to import the drivers into
   the image. For example, use the following command:
 
   dism /image:C:\mounted_winpe /Add-Driver /driver:c:\temp\winpe\ixe6232.inf
 
The syntax for the dism.exe tool is as follow:
 
   dism /image:<%WINPEDIR%> /Add-Driver /driver:<path>
 
     /image:<%WINPEDIR%> specifies the path to the directory where you have
     mounted your Windows PE image.
     /Add-Driver specifices the action dism should take.
     /driver:<path> specifies the path to the driver inf file.
 
Please see your Microsoft Windows PE documentation or the Microsoft website for
more information on using dism.exe
 
x64 Microsoft Windows PE V3
===========================
1. Create a temporary directory (for example, c:\temp\winpe).
 
2. Copy all files from the PROXGB\Winx64\NDIS62 directory to the temporary
   directory. Do NOT copy the ixe62x64.inf file to this directory.
 
3. Extract the driver inf file (for example: ixe62x64.inf)from 
   PROXGB\Winx64\NDIS62\WinPE\*.zip to the temporary directory.
 
4. Use the /Add-Driver option of the DISM.exe tool to import the drives into
   the image. For example, use the following command:
 
   dism /image:C:\mounted_winpe /Add-Driver /driver:c:\temp\winpe\ixe62x64.inf
 
The syntax for the dism.exe tool is as follow:
 
   dism /image:<%WINPEDIR%> /Add-Driver /driver:<path>
 
     /image:<%WINPEDIR%> specifies the path to the directory where you have
     mounted your Windows PE image.
     /Add-Driver specifices the action dism should take.
     /driver:<path> specifies the path to the driver inf file.
 
Please see your Microsoft Windows PE documentation or the Microsoft website
for more information on using dism.exe
 
Legal / Disclaimers
===================
Copyright (C) 2009-2015, Intel Corporation. All rights reserved.
 
Intel Corporation assumes no responsibility for errors or omissions in this
document. Nor does Intel make any commitment to update the information
contained herein.
 
Intel and the Intel logo are trademarks of Intel Corporation or its
subsidiaries in the U.S. and/or other countries.
 
*Other names and brands may be claimed as the property of others.
