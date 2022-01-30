# Windows Tips

Hello everyone, this readme aims to share with you the tools I use on a daily basis on W10 to improve the user experience:

## Tool n°1 : PowerToys

------

<img src="Ressources/PowerToysLogo.png" alt="PowerToysLogo" style="zoom:67%;" />

[PowerToys](https://docs.microsoft.com/en-us/windows/powertoys/) s an open source application that uses keyboard shortcuts to launch windows add-ons that integrate seamlessly with the W10 environment and enhance the user experience.

For example, here is the "PowerRun" bar which allows quick access to applications, visual studio code workspaces, windows services, with just alt + space shortcut: 

<img src="Ressources/PowerRunExemple.png" alt="image-20210901193126519" style="zoom:67%;" />

Here is the link to the github where you can discover the many other tools of PowerToys:

https://github.com/microsoft/PowerToys



## Tool n°2 : Search Deflector (seems to not working anymore :cry:) 

------

<img src="Ressources/SearchDeflectorLogo.png" alt="image-20210901194026093" style="zoom:67%;" />

[Search Deflector](https://github.com/spikespaz/search-deflector) is a tool developed by [Jacob Birkett](https://github.com/spikespaz) that allows you to **divert** the **internet queries** made by **cortana** or the **W10 search bar** to your **favorite web browser** armed with your **favorite search engine.**

Link :

https://github.com/spikespaz/search-deflector



## Tool n°3 : Windows Terminal

------

Windows Terminal is a new terminal that gather all Windows Terminal (cmd, powershell,...) in just an app. It offers many possibility of personalization.

![](Ressources\WTerminal.png)

Link : https://github.com/microsoft/terminal



## Tool n°4 : WSL 2

------

WSL2 (Windows Subsystem for Linux) is a compatibility layer for running Linux binary executables natively on W10 & W11. This tool rely on a real Linux kernel through a subset of Hyper-V features. 

This tool combined with Windows Terminal is really powerful :muscle:

![](Ressources\WSL2.png)

Link : https://docs.microsoft.com/en-us/windows/wsl/install



## Tool n°5 : VcXsrv

------

VcXsrv is an app that launch a server X in localhost to provide GUI for WSL2. That means yo can launch firefox and linux-based app with GUI when it is possible.

How to do that ?
Firstly by [modifying your WSL2 Linux .bashrc](https://github.com/Upsylonbare/Notices/tree/master/Linux%20Tips#basrc) and add this to line at the end of the file (not forget to source it):

```bash
export DISPLAY=$(cat /etc/resolv.conf | grep nameserver | awk '{print $2; exit;}'):0.0
export LIBGL_ALWAYS_INDIRECT=1
```

Then download and install VcXsrv :

https://sourceforge.net/projects/vcxsrv/

Then launch it and setup it like that 

![](C:\Users\clego\OneDrive\Documents\Web\Notices\Windows Tips\Ressources\VcXsrv.png)

At the end of the configuration, hit the save configuration button and save it in your startup folder to start your server X each time your computer start.

To do it, firstly save the conf file on your desktop

Hit `Win+R` and type `shell:startup` this open a Windows Explorer tab in which you can paste your conf file.



