# Summary

If you're a Arch user, you may be well aware that playing around with Arch would most definitely break it, in some cases. That sort of goes for any distro but over the years of using different Linux distros, I found that with Arch it's not the easiest to rollback. In case of a Arch Linux breakage, I've created a "Setup" script that install all the software, tools and packages that I use so I can get back on my feet as soon as possible. 

# Concept Goals 

Making this script, I had simple goals in mind which includes:
- This script needs to look readable 
- This script needs to look understandable and somewhat simple
- Includes a ASCII art
- A title using Figlet
- Have fun making it and watching it run


# **The Script & Annotations:**

**The ASCII Art:**

<img width="318" height="593" alt="image" src="https://github.com/user-attachments/assets/0d96fae8-3672-4b9d-9d2f-f1b8e30abb9e" />


**ASCII art from: emojicombos**

<img width="735" height="1103" alt="image" src="https://github.com/user-attachments/assets/088a7b82-b6d8-45c4-9f61-d12ef1ad9690" />

**Annotations:** This is sort of a welcome screen to the script, very common way of showing a loading code of the script,  which usually includes title, some sort of a logo, a prompt for something(s). There's a lot of echos, letting the user know almost exactly what's happening, in case people that may have Arch, don't know how scripting works. 

<img width="584" height="720" alt="image" src="https://github.com/user-attachments/assets/5f13c5c9-0a3a-4a1b-8318-48a31d09c6bc" />

**Annotations:** After so, It updates the system in case the user didn't. Then it lists what packages and softwares that will be installed, it ONLY lists them, it doesn't install them just yet, in my case, those are the packages and tools that I use on a regular basis. A different user may have different packages and tools that they would like on their machine and it's simple as pretty much going into the script and deleting any of the stuff they don't want and adding the stuff they want.

<img width="737" height="622" alt="image" src="https://github.com/user-attachments/assets/b7ede292-66aa-41b9-83de-7014ee3e373b" />

**Annotations:** Then it actually does install those tools and softwares. This is much efficient then doing "sudo pacman -S packagename" many times, which in this case it may be 19 times.

<img width="584" height="601" alt="image" src="https://github.com/user-attachments/assets/486ec924-5246-41da-ad93-26b1077939bb" />

**Annotations:** It's the same deal here, however this time it's with YAY from the AUR packages instead of Pacman. 

<img width="773" height="299" alt="image" src="https://github.com/user-attachments/assets/cc94b06a-a20b-4215-a739-ad9aa43d2575" />


**Annotations:** This is more of personal preference. I like when my terminal loads up, it displays neofetch or fastfetch. I also like to use Fish shell, which speeds up my terminal workflow. 

<img width="685" height="509" alt="image" src="https://github.com/user-attachments/assets/ef4e5d75-e05c-4c7d-9e10-1fafd3ea0c03" />


**Annotations:** Lastly, it tells the user that the installation was successful, which it should be most of the time since it's working with any proprietary tools. It's kind of straightforward yet efficient way to install your favorite softwares and tools. Then it launches up your Kitty terminal and shows fastfetch, so the user can get a glimpse how their system looks like.

**Conclusion:** I had a lot of fun making this script, it was one of my first one I did without much internet, video help and it helped me learn a lot about scripting in general and I look forward to advancing my scripting skills. 

If you want the script for yourself to copy and paste (I will also include a full download link to it), here you ago!

**Full Raw Script:**

#!/bin/bash


set -e
echo -e "\0331m WELCOME TO\0330m" 
echo -e "\0330;31m

\0330m"  
echo -e "\0331;34m Arch Set-UP\0330m"
sleep 2

echo -e "\0331;33m Set-Up requires Password To Initiate...\0330m"
sleep 1
echo -e "\0331;33m May need password more then once...\0330m"


echo -e "\0331m Are you sure to start? (y/n) \0330m"
read -r response 

response=(echo "response" | tr ':upper:' ':lower:')

if [[ "$response" == "y" || "$response" == "yes" ]]; then 
	echo -e "\0331m Starting Arch Set-Up Script...\0330m"
fi
sleep 1



echo "--------------------------"
echo -e "\0331m Updating System...\0330m"
echo "--------------------------"
sudo pacman -Syu --noconfirm
sleep 1




echo "----------------------------------------"
echo -e "\0331m 
Installing the following Pacman Softwares:
btop
htop
nvtop
nvidia
nvidia-utils
lib32-nvidia-utils 
fastfetch
neovim
figlet
fish
kitty
alacritty
tmux
blender
gimp
obs-studio
audacity
handbrake
virtualbox

\0330m"

echo "----------------------------------------"

sleep 5


pacpackages=(
btop
htop
nvtop
nvidia
nvidia-utils
lib32-nvidia-utils 
fastfetch
neovim
figlet
fish
kitty
alacritty
tmux
blender
gimp
obs-studio
audacity
handbrake
virtualbox
)

for ppackage in ${pacpackages@}; do
	sudo pacman -S --noconfirm ${pacpackages}
done 






echo "----------------------------------------"
echo -e "\0331m 
Installing the following Pacman Softwares:
spotify
steam
obsidian
pureref
lutris

\0330m"

echo "----------------------------------------"

yaypacckages=(
	spotify
	steam
	obsidian
	pureref
	lutris
	



for ypackage in ${yaypackages@} do;



if grep -q "fish" ~/.bashrc; then 
	echo -e "\0331m Adding Fish to ~/.bashrc...\0330m"
	echo -e "\n# Enabling Fish with Kitty" >> ~/.bashrc
	echo "fastfetch" >> ~/.bashrc
fi


if ! grep -q "fastfetch" ~/.bashrc; then 
	echo -e "\0331m Adding Fastfetch to ~/.bashrc...\0330m"
	echo -e "\n# Display System Info with Fastfetch" >> ~/.bashrc
	echo "fastfetch" >> ~/.bashrc
fi


echo "--------------------------"
echo -e "\0331;32m Installations Sucessful\0330m"
echo "--------------------------"

echo "--------------------------"
echo -e "\0331;32m WELCOME, $USER\0330m" 
echo "--------------------------"



echo "--------------------------"
echo -e "\0331;32m Extra Info
kitten theme (To switch theme of kitty)
set -U fish_greeting "" (To disable greeting in Fish\0330m"
echo "-------------------------"



Launch a kitty Terminal with Neofetch
kitty &	


