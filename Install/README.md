# Windows_11_VM

















[Download Windows 11](https://www.microsoft.com/software-download/windows11)

| Language | Hash values for the ISO files |
| --- | --- |
|English International 64-bit | F115CD6B31734BC091BC94B964D5AD43984285BF229503481E2F7EF94AB7140E |



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









