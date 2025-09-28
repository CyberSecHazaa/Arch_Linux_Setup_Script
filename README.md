# Summary
---
If you're a Arch user, you may be well aware that playing around with Arch would most definitely break it, in some cases. That sort of goes for any distro but over the years of using different Linux distros, I found that with Arch it's not the easiest to rollback. In case of a Arch Linux breakage, I've created a "Setup" script that install all the software, tools and packages that I use so I can get back on my feet as soon as possible. 

# Concept Goals 
---
Making this script, I had simple goals in mind which includes:
- This script needs to look readable 
- This script needs to look understandable and somewhat simple
- Includes a ASCII art
- A title using Figlet
- Have fun making it and watching it run


# **The Script & Annotations:**
----
**The ASCII Art:**





**ASCII art from: emojicombos**









**Annotations:** This is sort of a welcome screen to the script, very common way of showing a loading code of the script,  which usually includes title, some sort of a logo, a prompt for something(s). There's a lot of echos, letting the user know almost exactly what's happening, in case people that may have Arch, don't know how scripting works. 





**Annotations:** After so, It updates the system in case the user didn't. Then it lists what packages and softwares that will be installed, it ONLY lists them, it doesn't install them just yet, in my case, those are the packages and tools that I use on a regular basis. A different user may have different packages and tools that they would like on their machine and it's simple as pretty much going into the script and deleting any of the stuff they don't want and adding the stuff they want.





**Annotations:** Then it actually does install those tools and softwares. This is much efficient then doing "sudo pacman -S packagename" many times, which in this case it may be 19 times.








**Annotations:** It's the same deal here, however this time it's with YAY from the AUR packages instead of Pacman. 


