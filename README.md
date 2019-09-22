# MacOSR
A MacOS Replica, built on KDE Plasma, using Latte and a litany of other tools, including references to bootloader, splashscreen, and local stylings.

![Original](https://cdn.discordapp.com/attachments/369445684103086081/625201742983856128/Screenshot_20190922_012722.png)

[**Alternate Version**](https://cdn.discordapp.com/attachments/369445684103086081/625201745106305035/Screenshot_20190922_012816.png)

Note: There will be other versions and themes installed as well, to better help you pick a version that you prefer. The icons in the image **may** be supplied over GitHub, if they're okay with it, but it's quite a large filesize, approaching 5GB. If it becomes hosted offsite, I'll link the compiled folder here.

## Prerequisites / Requirements
Tested with:<br>
`KDE Plasma (Latest)`<br>
`Kubuntu 19.04 / Ubuntu 19.04`<br>
`An Internet Connection`<br>

## Included
#### Resources
* Apple Fonts
* Apple Logo (White)
* Notification Logo (White)
* UMenu App Launcher
* Sidebar App Launcher
#### KDE Themes
* Modified Aex Dark Theme (Not Recommended due to UI / UX inconsistency)
* McMojave
* Mojave-CT
#### Icon Packs
* Mojave-CT
* McMojave Circle
* Mac OSXOne 8 (Not Recommended - Broken)
#### SDDM
* McMojave
#### Color Packs
* KvantumAlt
* Kvantum
* McMojave
* McMojave Light
#### Window Managers
* Kvantum
#### Window Decorations
* Modified Cupertino
* Mojave Dark Aurorae

# Installation / Manual Installation
For the automatic installation, for those that know that their dependencies are correct, or just want to ride the lightning, go to the installed folder, right click > Actions (in the context menu) > Open Terminal / Konsole Here. Afterwards, you're going to run: `sudo ./install.sh`<br>
<br>
First, we need to verify that out starting materials are correct. If you're extremely new to linux, you need to make sure that you're running on Ubuntu, or an Ubuntu / Debian derivative. If you don't know what distro you installed, first of all- what? moving past that, let's check our desktop environment:<br>
<br>
KDE Plasma Verification: `plasmashell --version`<br>
*If this comes back with anything other than a version number or integer, you should probably reinstall your desktop environment, in this case being KDE Plasma.*<br>


## F.A.Q.
Will you be maintaining theses resources individually?<br>
**A:** No, that's on the individual creators.

Will you update this with newer versions as they're released?<br>
**A:** Possibly, but it would have to be something that the creators and I would work together on.

Will you compile the icon packs into one central icon pack, to fix the broken ones?<br>
**A:** Most likely, no. However, if a lot of interest is expressed, then maybe, but I'd prefer to have permission from the authors. I will however show how to fix broken icons in the trouble shooting section here.

Will you convert this documentation to GitBooks for easier reading?<br>
**A:** Yes, absolutely. However, I wanted to get a preliminary version done on GitHub prior. I may create a wiki here, if one is needed.

Will you update this internally?<br>
**A:** Yes, any custom modifications I make to the apps, programs, or desktops, will be added here, unless it's added in another separate repository, in which case it'll be referenced / added here.

Have you already modified anything?<br>
**A:** Some things, yes. Not enough to constitute any major changes. For the most part, it's just been UI / UX for the sake of continuity.

Are you worred about Apple requesting a take-down?<br>
**A:** I suppose a small bit, as is anyone that makes a replica. However, given that this isn't for sale, I don't consider it to be infringing to any of their properties (despite the logo included), and I'm fairly confident it could pass the factors in a balancing test. Which, even if it doesn't, I'll move the project to another location, out of the country (United States) if necessary.

I just started using Linux, can I use this?<br>
**A:** Absolutely, I'm planning to make the installer as simple as possible to allow new users to try to bridge the UI/UX gap between MacOS and Linux, drawing more users.

Are you going to include a wine installer to get a stable version that supports apps like the Adobe Suite, Safari, Microsoft Office, etc?<br>
**A:** That's hilarious...maybe..

Putting in all of this work, why not just make your own distro?<br>
**A:** Because making a distro is a lot more complex than formulating a front-end, even considering those Ubuntu derivatives like Mint, Deepin, Elementary, etc. Plus, using these resources to make a distro has a much higher probability of pissing someone off.

## Troubleshooting
My windows have large borders around them now, what happened?<br>
**A:** This is a known problem with Nvidia's drivers. Unfortunately, I have yet to find out exactly what causes it. A temporary workaround / solution is to purge the drivers with: `sudo apt-get purge nvidia*` (Yes, you will still be able to view your desktop).

Refind isn't letting my use high resolution options, why?<br>
**A:** For those with AMD Cards, it may be a matter of just disabling CSM in your BIOS and ensuring you're running in UEFI / EFI mode only. For some manufactures, this means enabling a certain setting akin to "Windows 8 / 8.1 / 10 Mode / Compatibility Mode, in addition to disabling legacy support in your bootloader. For those with Nvidia cards, Nvidia, without going into detail, has a certain interaction with KVM that can cause problems. Purging the drivers helps this as well, but you may still need to disable CSM and the above settings.

My desktop isn't loading on boot?<br>
**A:** This is a bit of a more uncommon problem, but when using Refind while Proxying Grub2 (the way this installation works for compatibility purposes), it can increase boot time, even though Grub2 runs silently / passively. Most of the time, it's trial and error. This usually resolves itself afer a couple of minutes; KDE catches up, for lack of a better term. (Yes, it's normal for latte to launch before the plasma desktop, in some cases (at least pertaining to this installation, it's still an anomaly normally)).
