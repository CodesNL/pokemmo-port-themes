# PokéMMO Custom Themes (Portmaster Edition)

Welcome to the official repository for custom **PokéMMO themes** built specifically for the **PokéMMO port running via [Portmaster](https://github.com/PortMaster/PortMaster)**.

Whether you're looking to personalize your in-game UI or create your own theme, this repo provides ready-to-use themes and a base to build from.

---

## 📁 Installation
(This theme/instalation is only for the custom animation login screen I will be working on full theme support in the future)
1. **Install PokéMMO via the PokeMMO GitHub page**  
   Follow the instructions at the [PokéMMO port](https://github.com/lowlevel-1989/pokemmo-port) to set up PokéMMO.

2. **Download or Clone this Repository**
   ```bash
   git clone https://github.com/yourusername/pokemmo-themes-portmaster.git

3. Copy the Theme Folder to PokéMMO's Port Theme Directory
The typical path is: ~\ports\pokemmo\data\themes

4. Now only copy these's files (anim,login-animation.xml,theme.xml) from the Default Theme Folder to: ~\ports\pokemmo\data\mods\console_mod\console

5. Now go to ~\ports\pokemmo\config\main.properties
open main.properties.txt and change the line client.ui.theme=console to client.ui.theme=default
save and exit.

Now you should have a custom login animation 
<img width="3024" height="4032" alt="image" src="https://github.com/user-attachments/assets/8728a76c-b397-4bf6-bf99-799ecfec45bb" />


## Creating Your Own Theme/Login Animation

*For the custom login theme follow these steps. 

1. Convert the video you want for you login animation to PNG: https://ezgif.com/video-to-png
Important to use ezfig.com, since the code is based on the file naming, if not you can always edit the xml file yourself.
Make sure the video you convert to PNG is the same size as your device, for the RG35XXSP it's 640x480.

3. Go to your Theme folder Default, and place the images in the folder 'anim' depending on how many images you have, you would need to edit both theme.xml and login-animation.xml
(Don't forget you need to do this for both the Data/Theme folder and the Mod Console folder)

4. Make sure to have this one line in both the Theme.xml files 
<img width="606" height="693" alt="image" src="https://github.com/user-attachments/assets/e5984cd8-2177-4c08-9a52-c9cf95b2c03e" />

5. In the login-animation.xml make sure the code goes to the amount of images you have, so in this instance 145 images.
<images file="anim/ezgif-frame-145.png" filter="nearest">
<area name="bg-f00145" xywh="*"/>
<img width="1362" height="958" alt="image" src="https://github.com/user-attachments/assets/19ecc460-5919-40a8-943b-fc470e0edbe7" />

6. Do the same for the duration code.
<frame ref="bg-f00145" duration="50"/>
<img width="1030" height="944" alt="image" src="https://github.com/user-attachments/assets/7fd9f5f8-d8f7-4d15-b404-cf5a21c45c17" />


## Custom Themes
As for custom theme's you can try to copy the Theme folder to ~\ports\pokemmo\data\themes and ~\ports\pokemmo\data\mods\console_mod\console.
I haven't tested full theme's yet, I will be working on it.


## 🙌 Credits

- **PokéMMO** – All game assets, client, and content belong to the developers at [https://pokemmo.eu](https://pokemmo.eu). This project is not affiliated with or endorsed by PokéMMO.
- **Portmaster** – Thanks to the [Portmaster](https://github.com/PortMaster/PortMaster) project for making it possible to run PokéMMO on various platforms.
- **PokéMMO GitHub Port** – Special thanks to the community-maintained [PokéMMO port](https://github.com/lowlevel-1989/pokemmo-port) for enabling compatibility through Portmaster.





