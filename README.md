# My Team Fortress 2 config

This repository contains my custom TF2 files and instructions for applying the configuration on Linux desktop.

## Instructions

1. [Clean up your TF2 installation](https://docs.mastercomfig.com/latest/setup/clean_up/).
   * The config assumes default settings and changes them only where necessary.

2. Change working directory to the custom folder.

    ```bash
    cd ~/.steam/steam/steamapps/common/Team\ Fortress\ 2/tf/custom
    ```

3. Clone this repository.

4. Download [mastercomfig by mastercoms](https://mastercomfig.com/) Low preset with Null-Canceling Movement, OpenGL and No Tutorial addons.

5. Download [junior's loadouts script](https://github.com/jooonior/tf2-loadouts-script).

6. Move the downloaded vpk files to the custom folder.

    ```bash
    mv ~/Downloads/*.vpk .
    ```

7. Clone [Eniere's Improved default HUD](http://eniere.github.io).

    ```bash
    git clone https://github.com/Eniere/idhud.git
    ```

8. [Enable Server Control Panel](https://wiki.teamfortress.com/wiki/User:Eniere/Improved_Default_HUD#How_to_enable_Server_Control_Panel) by modifying `mainmenuoverride.res`.

    ```bash
    nano idhud/resource/ui/mainmenuoverride.res
    ```

   * Optional: [Change Medic UI layout](https://wiki.teamfortress.com/wiki/User:Eniere/Improved_Default_HUD#How_to_change_Medic_UI_layout) by modifying `hudmediccharge.res`.

        ```bash
        nano idhud/resource/ui/hudmediccharge.res
        ```

9. Move custom HUD files (modified `idhud` files) to replace `idhud` files.

    ```bash
    mv tf2-config/resource/ui/huddamageaccount.res idhud/resource/ui/huddamageaccount.res
    mv tf2-config/advanced/resource/ui/mainmenuoverride_scp.res idhud/advanced/resource/ui/mainmenuoverride_scp.res
    ```

10. Install `idhud` fonts and `lucon.ttf` (Lucida Console) font.

    ```bash
    sudo mv idhud/resource/fonts/* /usr/share/fonts
    sudo mv ~/lucon.ttf /usr/share/fonts
    ```

11. Optional: Install [GameMode](https://github.com/FeralInteractive/gamemode) and/or [libstrangle](https://gitlab.com/torkel104/libstrangle).

12. Set Launch Options for TF2 (options marked with `[]` are optional).

    ```txt
    [gamemoderun] [strangle 143.86 %command%] -novid -nojoy -nosteamcontroller -nohltv -particles 1 -precachefontchars -noquicktime -console -nostartupsound -no_texture_stream
    ```

## Maps

Maps to download.

* [tr_walkway_fix](https://gamebanana.com/mods/74813)
* [tr_rocket_shooting2](https://gamebanana.com/mods/74806)
* [tr_newbots](https://gamebanana.com/mods/74803)
