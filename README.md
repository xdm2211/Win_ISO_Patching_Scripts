### Win_ISO_Patching_Scripts

[English Readme](https://github.com/adavak/Win_ISO_Patching_Scripts/blob/master/README.md)

[中文说明](https://github.com/adavak/Win_ISO_Patching_Scripts/blob/master/README_cn.md)

<a href="https://github.com/adavak/Win_ISO_Patching_Scripts/releases/latest"><img src="https://img.shields.io/github/v/release/adavak/Win_ISO_Patching_Scripts"></a>
<a href="https://github.com/adavak/Win_ISO_Patching_Scripts/releases/latest"><img src="https://img.shields.io/github/release-date-pre/adavak/Win_ISO_Patching_Scripts"></a>

##### Usage: Put the Windows image (ISO format) in the root directory of the folder. Run Start.cmd to start downloading the latest patches and start creating an ISO with the integrated patches. The download address of the patch file is from Microsoft.


###### Supported Windows versions:

|Name|Internal version (last updated: November 13, 2024)|
|---|---|
|**Windows 10 Enterprise LTSB 2016, Windows Server 2016**|**Build 14393.7515**|
|**Windows 10 Enterprise LTSC 2019, Windows Server 2019**|**Build 17763.6532**|
|**Windows 10 22H2, Windows 10 Enterprise LTSC 2021**|**Build 1904x.5131**|
|**Windows Server 2022**|**Build 20348.2849**|
|**Windows 11 21H2**|**Build 22000.3260 (2024-10, EOL)**|
|**Windows 11 23H2**|**Build 22631.4460**|
|**Windows 11 24H2, Windows 11 Enterprise LTSC 2024, Windows Server 2025**|**Build 26100.2314**|

###### Some settings (located in the W10UI.ini file in the root directory of the folder):
|Value|Description|
|---|---|
|**Net35 = 1**|If you do not want to integrate .NET 3.5, change it to 0.|
|**wim2esd = 1**|If you do not want to generate an install.esd file to reduce space usage. This process consumes a lot of time and computer resources, and the image size is reduced by about 25%. Change it to 0.|
|**AutoStart = 1**|For multi-version images, the script will download and integrate all the images by default and start automatically. If you need to select a specific version in the image, such as only generating an integrated update image for the Professional edition, change it to 0. After the script is run, press 8 to select the version. You can select multiple versions. After selecting, press 0 to start.|
|**ltscfix = 1**|Repair the library files for LTSC 2021 & 2024 (this option will be removed after the official patch is released). If you do not want to repair, change it to 0.|
|**netfx481 = 1**|Support for .NET Framework 4.8.1. If you do not want to install it, change it to 0.|
|**nosuggapp = 0**|If you want to disable the installation of third-party apps after a new installation of Windows, change it to 1.|
|**nosuggtip = 0**|If you want to disable the useless suggestion tips and functions in Windows, change it to 1.|
|**norestorage = 0**|If you want to disable the space usage of the reserved storage, change it to 1.|
|**nogamebar = 0**|If you want to disable the Game Bar, change it to 1.|

###### Thanks:
|Tool|Source|
|---|---|
|**7-zip**|[7-zip.org](https://www.7-zip.org)|
|**wimlib**|[wimlib.net](https://wimlib.net)|
|**aria2**|[aria2](https://github.com/aria2/aria2)|
|**oscdimg**|[Microsoft](https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/oscdimg-command-line-options)|
|**PSFExtractor**|[PSFExtractor](https://github.com/Secant1006/PSFExtractor)|
|**W10UI**|[BatUtil](https://github.com/abbodi1406/BatUtil)|
