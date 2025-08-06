# PokéMMO Custom Themes (Portmaster Edition)

Welcome to the official repository for **custom PokéMMO themes**, specifically built for the **PokéMMO port running via [Portmaster](https://github.com/PortMaster/PortMaster)**.

Whether you want to personalize your in-game UI or create your own custom login animation, this repo provides ready-to-use assets and a foundation to build upon.

---

## 📁 Installation Guide

> ⚠️ **Note:** This setup currently supports **custom login screen animations only**. Full theme support is in development.

### 1. Install PokéMMO via GitHub  
Follow the instructions on the official [PokéMMO port](https://github.com/lowlevel-1989/pokemmo-port) to install the game.

### 2. Clone or Download This Repository
```bash
git clone https://github.com/yourusername/pokemmo-themes-portmaster.git
```

### 3. Copy Theme Files
- Copy the `Default` theme folder to:  
  `~/ports/pokemmo/data/themes`

### 4. Apply the Login Animation Files
- From the `Default` folder, copy these files:
  - `anim`
  - `login-animation.xml`
  - `theme.xml`

  To:  
  `~/ports/pokemmo/data/mods/console_mod/console`

### 5. Update Config
- Open the file:  
  `~/ports/pokemmo/config/main.properties`
- Change this line:
  ```
  client.ui.theme=console
  ```
  To:
  ```
  client.ui.theme=default
  ```
- Save and close the file.

You should now see your custom login animation when launching the game!

![Login Animation Preview](https://github.com/user-attachments/assets/8728a76c-b397-4bf6-bf99-799ecfec45bb)

---

## Creating Your Own Login Animation

Follow these steps to create a custom login animation using your own video or GIF.

### 1. Convert Video to Frames
- Go to [ezgif.com](https://ezgif.com/video-to-png)
- Upload your video or GIF.
- Convert it to PNG frames.
- Download the result as a `.zip` file.

> ⚠️ **Important:**  
> Use **ezgif.com** specifically, as the XML animation relies on its naming format.  
> Using another tool may require renaming files or editing the XML manually.

### 2. Ensure Correct Resolution
- The animation should match your device's resolution.  
  For the **RG35XXSP**, use **640x480**.

### 3. Add Frames to Your Theme
- Extract the PNG frames into the `anim/` folder inside your theme (both in `data/themes` and `mods/console_mod/console`).
- Update both `theme.xml` and `login-animation.xml` to reflect your image count.

### 4. Add This Line to Both `theme.xml` Files
Make sure this line is included in both copies of `theme.xml`:

![XML Theme Line](https://github.com/user-attachments/assets/e5984cd8-2177-4c08-9a52-c9cf95b2c03e)

### 5. Update `login-animation.xml`

For example, if you have 145 images, add this to the XML:
```xml
<images file="anim/ezgif-frame-145.png" filter="nearest">
  <area name="bg-f00145" xywh="*"/>
</images>
```
![XML Image Example](https://github.com/user-attachments/assets/19ecc460-5919-40a8-943b-fc470e0edbe7)

Also, update the frame duration section accordingly:
```xml
<frame ref="bg-f00145" duration="50"/>
```
![Frame Duration Example](https://github.com/user-attachments/assets/7fd9f5f8-d8f7-4d15-b404-cf5a21c45c17)

---

## Custom Theme Support (WIP)

Full UI theming is currently **experimental**.

You can try placing your custom `Theme` folder in both:
- `~/ports/pokemmo/data/themes`
- `~/ports/pokemmo/data/mods/console_mod/console`

This may allow some customization, but full support is not guaranteed yet. Stay tuned for future updates.

---

## Credits

- **PokéMMO** – All game assets, client files, and intellectual property belong to [pokemmo.eu](https://pokemmo.eu).
- **Portmaster** – Huge thanks to the [Portmaster](https://github.com/PortMaster/PortMaster) team for enabling PokéMMO on various platforms.
- **PokéMMO GitHub Port** – Special thanks to the [community-maintained port](https://github.com/lowlevel-1989/pokemmo-port) for making this project possible.
