# Install Windows 11 as Guest OS on VMware Workstation

Purpose of this repository is to provide one way (of the many available in the Internet) to install Windows 11 as Guest OS on VMware Workstation, where either or both of the host machine's resources and/or the VMware version do ***NOT support Windows 11 Requirements***.
There are many guides which use script and/or binary tool which you need to download and execute.
However, from security perspective this MAY NOT be a good option since you MAY NOT trust those scripts and/or binary tools.
This repository provides a step by step procedure without needing external script or external binary tool.
All you need is the original installation `.iso` file from Microsoft.

The procedure on this repository were tested with the following components:
- [ ] Host: Windows 10 Home (version 22H2)
- [ ] Virtualization Technology: VMware Workstation Pro (version 15.5.7)
- [ ] Guest OS: Windows 11 Pro (version 22H2)
Note that both Microsoft and VMware keep updating their software, so when the versions you use differ, understandably you may stumble on error(s) not stated in this repository.

Download the Windows 11 `.iso` file from Microsoft's [Download Windows 11](https://www.microsoft.com/software-download/windows11) page.
The `.iso` file used for this repository is the one stated on the table below:
| Language | SHA256 hash values for the `.iso` files |
| --- | --- |
| English International 64-bit | F115CD6B31734BC091BC94B964D5AD43984285BF229503481E2F7EF94AB7140E |



[Installing Windows 11 as a Guest OS on VMware Workstation](https://kb.vmware.com/s/article/86207)

- [ ] While installing Windows 11, if your computer does not meet the hardware requirements, you will see a message stating, "This PC can't run Windows 11." Windows 11 setup blocked due to missing hardware requirements.
- [ ] When you see the above message, press `shift`+`F10` (Or `shift`+`fn`+`F10`) on your keyboard at the same time to launch a command prompt. At the command prompt, type `regedit` and press `enter` to launch the Windows Registry Editor.
- [ ] When the Registry Editor opens, navigate to: `HKEY_LOCAL_MACHINE\SYSTEM\Setup`, Right-click on the `Setup` key and select `New` > `Key`.
- [ ] When prompted to name the key, Type `LabConfig` and press `enter`.
- [ ] Now right-click on the `LabConfig` key and select `New` > `DWORD (32-bit)` value and create a value named `BypassTPMCheck`, and set its data to `1`.
- [ ] Now right-click on the `LabConfig` key and select `New` > `DWORD (32-bit)` value and create a value named `BypassSecureBootCheck`, and set its data to `1`.
- [ ] Now right-click on the `LabConfig` key and select `New` > `DWORD (32-bit)` value and create a value named `BypassRAMCheck`, and set its data to `1`.
- [ ] Now right-click on the `LabConfig` key and select `New` > `DWORD (32-bit)` value and create a value named `BypassStorageCheck`, and set its data to `1`.
- [ ] Now right-click on the `LabConfig` key and select `New` > `DWORD (32-bit)` value and create a value named `BypassCPUCheck`, and set its data to `1`.












- [ ] Once you configure the above keys and their respective values under the `LabConfig` key, close the Registry Editor, and then type `exit` in the Command Prompt followed by `enter` to close the window. You will now be back at the message stating that the PC can't run Windows 11. Click on the back button in the Windows Setup dialog, as shown below. Press the back button in Windows setup.
- [ ] You will now be back at the screen prompting you to select the version of Windows 11 you wish to install. You can now continue with the setup, and the hardware requirements will be bypassed, allowing you to install Windows 11.


- [ ] Blah, blah . . . press `shift`+`F10` (Or `shift`+`fn`+`F10`) on your keyboard at the same time to launch a command prompt. At the command prompt, type `oobe\bypassnro` and press `enter`. the guest os will reboot/restart









