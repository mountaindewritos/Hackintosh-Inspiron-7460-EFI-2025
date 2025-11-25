**Dell Inspiron 7460 Sonoma, Sequioa and Tahoe (Pending OCLP new version) EFI with Unsupported BCM Wifi cards**

_For Sequioa installations and later, choose the Tahoe EFI as it has a Broadcom legacy card patchfix. For Sonoma 14.3.1 and below choose the Sonoma EFI (v1.2.0)._

***For Sequioa and Tahoe Build***

This was made from the ground up with the help of OC-Simplify since the previous EFI builds had a ton of kexts for compatibility making it a bit bloated. In this EFI build the DSDT, kext patches are only few resulting to a much faster, reliable and stable boot.
You have to add other kexts yourselves to suit your macOS experience. Wait for the newer OCLP release as 2.4.0 detects Tahoe as Unsupported OS.

<img width="2048" height="1536" alt="image" src="https://github.com/user-attachments/assets/4751cefa-22c2-424b-9b8b-377a8d1f4b96" />


***For SONOMA Builds***

I already created CSR-ACTIVE-CONFIG codes for you to patch root easily on OCLP (SIP Disable), MinKernel Values for Wi-FI Kexts as well as Blocking com.apple.iokit.skywalkfamily on OCConfigurator.

Special Thanks to HowieHye who laid the ground work for the DSDT patches for Dell Inspiron 7460 but it's only for Ventura RC. I already included his patches to this build.

https://github.com/HowieHye/Dell-7460-Hackintosh-OC

***Instructions:***
1. Download hackintool (https://hackintool.com/) and install
2. You have to allow hackintool to macos ***Settings > Privacy & Security*** for you to open.
3. Open Hackintool and mount your EFI partition
4. Delete the existing EFI Folder and Replace it with the EFI that you downloaded

   (In case you are on Multiboot DELETE EFI/OC FOLDER AND REPLACE IT WITH THE OC FOLDER FROM THE DOWNLOADED EFI)
5. Download OpenCore Auxiliary tools (https://github.com/ic005k/OCAuxiliaryTools) and do the same as on step 2.
6. Open OpenCore Auxiliary Tools and go to ***File > Open*** config.plist located on EFI drive that you mounted earlier
7. On the Sidebar click PI from there you have to look for ***SystemProductName*** and click ***_Generate_***.
6. Save your config.plist and Restart your PC
7. Open OpenCore Legacy Patcher (I also proveded this on Applications.zip), Click Post-Install Root Patch and then Start Root Patching
   
![Screenshot 2024-03-18 at 1 06 36 PM](https://github.com/ervinavales/Hackintosh-Inspiron-7460-Sonoma/assets/66302821/6abf1d08-80d1-4d9e-8308-82312da7766b)

8. Reset NVRAM once on boot
9. You should have a working Wi-Fi after reboot

![Screenshot 2024-03-18 at 1 10 16 PM](https://github.com/ervinavales/Hackintosh-Inspiron-7460-Sonoma/assets/66302821/419b6357-aa18-428d-99a3-7b5a7ef08857)

For Intel Wi-Fi/BT cards download airportitwlm kext file and paste it on EFI/OC/Kexts
Download link: https://github.com/OpenIntelWireless/itlwm

**Permanent Issues for this build**
1. DRM doesn't work for Prime Video, Apple TV due to GPU incompatible with the OS specification 
2. Touchpad kext is a bit buggy (Disabled it for now)
3. Palm Rejection doesn't work for Sonoma EFI but on Sequioa it is fixed.
   
~~AirDrop doesn't work on BCM~~ (Fixed on v1.2.0 EFI)

![Screenshot 2024-03-20 at 12 09 18 AM](https://github.com/ervinavales/Hackintosh-Inspiron-7460-Sonoma/assets/66302821/a6cdfa34-54bd-468e-99a6-e9b37530e1f6)

~~Bluetooth doesn't work on BCM~~ (Fixed on v1.2.0 EFI)

![Screenshot 2024-03-20 at 12 09 53 AM](https://github.com/ervinavales/Hackintosh-Inspiron-7460-Sonoma/assets/66302821/007f68af-b614-49db-ac24-787b47ecdc0e)

