# Cinnamenu-metro

## 🌟 Features
- Metro style applet
- App groups
- App group priority
- Added context menu "Properties" and "Open Desktop File".

## 📸 Preview
![Menu](docs/menu.png)


## 🚀 How to Install

1. Extract the folder `Cinnamenu-metro@json` into your local applets directory:
   ```bash
   ~/.local/share/cinnamon/applets/
   ```
2. Restart cinnamon. Press `Alt + F2`, type `r`, and press `Enter` to reload the desktop environment.
3. **Add to Panel:**  
   Right-click your panel, select **Applets**, find **Cinnamenu-metro**, and add it.\
   ![Add Applet](docs/add-applet.png)

## 📂 How to Create Your Own Groups

Instead of forcing you to manually manage a complex JSON file every time a new app is installed, this applet reads your groups natively from your application launchers.

1. **Edit the Launcher:**  
   Open your desired `.desktop` file and add the `CinnamenuCategory` field inside the `[Desktop Entry]` section. The value will be the exact name of the group.
   Additionally you can add `CinnamenuPriority` field to specify the order of the apps in the group. The lower the number, the higher the priority. If not specified, the app will be placed at the end of the group.:
   ```ini
   [Desktop Entry]
   Name=Antigravity
   CinnamenuCategory=Work
   CinnamenuPriority=1
   ```

2. **💡 Pro Tip (Avoid losing your groups):**  
   To prevent system updates from overwriting your custom groups in `/usr/share/applications/`, copy your modified `.desktop` files to your user space:
   ```bash
   ~/.local/share/applications/
   ```
   The operating system will always prioritize your local versions over the system-wide ones.

---

## ⚠️ Known Limitations
- Groups are fixed to a maximum of 2 groups per row.


## ⚖️ Credits & License

* **Credits:** This applet is a modified version of the classic [Cinnamenu](https://github.com/fredcw/Cinnamenu) applet by **fredcw**.
* **License:** This project is licensed under the terms of the **GNU General Public License v3.0 (GPL-3.0)**.