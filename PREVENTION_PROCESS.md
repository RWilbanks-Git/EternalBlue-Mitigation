### DRAFT

To start, I determined that I needed to research the EternalBlue exploit to give myself a better idea on where my focus should be. From the sources I found (mentioned in SOURCES.mb), I learned that I needed to focus on disabling SMB1, installing the MS17-010 patch (or just making sure it is installed), and doing an overall check on the firewall (to be safe). 

I started by attempting to install the MS17-010 patch, though I am unsure whether it ever successfully downloaded before the attempted attack (there was no response in Command Prompt when running the command to get the patch, and there was no response when I tried to check if it was successfully added). With this in mind, I believe that SMB1's disabling had a larger role in preventing the attack.

As mentioned beforehand, I disabled SMB1 by using "reg add HKLM\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters /v SMB1 /t REG_DWORD /d 0 /f". After this command, I restarted the server. Later on, SMB1 gave signs of still being enabled when I ran "reg query HKLM\SYSTEM\CurrentControlSet\Services\mrxsmb10 /v Start". I believe this, and some issues with patching had to do with restarting errors on my own behalf (a few times, restarting made me lose most of my progress, leading me to start over). These issues were able to be fixed after another restart and other commands in Command Prompt (I am unsure of the exact ones due to restarting errors making me unsure of where I left off from the last attempt). 

Overall, the EternalBlue exploit was able to be defended against by disabling SMB1 and possibly by installing the MS17-010 patch. Though it might have not been the sole factor in preventing this attack, it is still important to make sure that this patch is installed. I will look into this and any other patches we may be lacking. I will also look into the availability of dasShare and both WinRM on Workstation-Desk and Domain-Controller for MSP, as there seems to be an issue with these.

Thank you for your time.
