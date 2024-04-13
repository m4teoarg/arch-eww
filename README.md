Archlinux awesome eww
 1. Install dependencies and enable services

      + Dependencies

      - **Arch Linux** (and all Arch-based distributions)

            *Assuming your AUR helper is* `yay`

            ```shell
            yay -Sy awesome-git picom-git alacritty rofi todo-bin acpi acpid \
            wireless_tools jq inotify-tools polkit-gnome xdotool xclip maim \
            brightnessctl alsa-utils alsa-tools pulseaudio lm_sensors \
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
