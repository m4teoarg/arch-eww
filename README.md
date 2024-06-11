Archlinux awesome eww
![Deja una estrella. Comparte.](https://github.com/m4teoarg/arch-eww/blob/eww/images/a.png)
 1. Install dependencies and enable services

      + Dependencies

      - **Arch Linux** (and all Arch-based distributions)

            *Assuming your AUR helper is* `yay`

            ```shell
            yay -Sy awesome-git picom-git rofi todo-bin acpi acpid \
            wireless_tools jq inotify-tools polkit-gnome xdotool xclip maim \
            brightnessctl alsa-utils alsa-tools lm_sensors \
            mpd mpc mpdris2 ncmpcpp playerctl --needed 
            ```

      + Services

         ```shell
         # For automatically launching mpd on login
         systemctl --user enable mpd.service
         systemctl --user start mpd.service

         # For charger plug/unplug events (if you have a battery)
         sudo systemctl enable acpid.service
         sudo systemctl start acpid.service
         ```
