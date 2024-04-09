# archvillainette-dotfiles-pub
 Here is my release of public dotfiles for open use. See /r/unixporn post here: https://www.reddit.com/r/unixporn/comments/1by7879/bspwm_experimenting_with_pywal/
 * OS: Arch Linux
 * WM: bspwm
 * Color Scheme: Automatically generated by wallpaper.
 * Bar: polybar
 * Editor: vscode
 * Launcher: rofi
 * Notifications: dunst
 * Files: thunar
 * Icons: Papirus

# Dependencies
 The following will be needed to make these dotfiles work correctly:
 * bspwm
 * sxhkd
 * picom
 * pywal (16 colors fork is HIGHLY recommended, things may break otherwise)
 * imagemagick (needed for generating some components of the theme)
 * feh (does the actual wallpaper work for the pywal scripts to allow theming and wallpaper configuration to be seperate)
 * Rofi
 * xorg-xrdb (Probably already included with your distro)
 * Papirus icons
 * Iosevka Nerd Font
 * Dunst
 * A GTK-based file manager, like Thunar. Ranger would also work fine if you prefer it.
 * Maim (for screenshots)
 * xclip (probably already included but make sure)

# Optional Dependencies
 * pywalfox (if you use Firefox)
 * vscode pywal theme (if you use VSCode. Install it through extensions)
 * themix-full (If you want GTK and spotify color theming to work)
 * Vesktop or Vencord (if you want a pywal-generated theme for your Discord)
 * rofi-calc (if you want a calculator built into your rofi)
 * archwiki-offline & arch-wiki-docs (If you want a functioning offline archwiki search through rofi)
 * Cava (for the polybar visualizer module. polybar may break if you don't have this, so if you don't want to use it, disable it in the polybar config)

# Notes
1. All files should have some explanations included for how to use them (or at least how I've personally used them). Take a look especially at the "walmaker" script in bspwm/scripts as that is the system I use for changing my themes.
2. If you want to use the screenshot script, you will need to set up a $SCREENSHOTS folder in your environment variables. You can export this in your shell configurations or just export it at the top of bspwmrc.
3. GTK theme generation takes time through oomix/themix, but I haven't found a etter method. WPGTK had some issues so I decided not to use it. If you discover a better method for changing Papirus icons and GTK themes all in one, feel free to drop me a message.
4. There is no support for QT in these dotfiles. I don't use QT at all or very little, so if you want pywal to work with QT, it will have to be set up.
5. Your window rules are in the bspwm/config folder, if you want to change how different windows behave.
6. First time launch of BSPWM may have some issues if it can't configure a theme by default. If it doesn't work correctly, make sure you've got a wallpaper in ~/.wallpapers so that it can generate the theme, and you may have to use walmaker to generate one. "walmaker -r -t" in your terminal should work fine. Once Pywal knows what theme its using, it should be consistently reapplied on reboots.

# Credits

rxyhn
   BrightnessCTL script came from here. Also, check out their stuff. Makes you want to use AwesomeWM, doesn't it?
https://github.com/rxyhn

gh0stzk
   gh0stzk's dotfiles have always been an excellent reference for new bspwm users. While I have also made many of my own adaptations for my own usecase, I didn't see any reason to reinvent the wheel, so some of his work has been integrated in part here.
https://github.com/gh0stzk/dotfiles

donovanglover
   It took me some time to figure out how to apply pywal themes to dunst. Donovan Glover made it look easy.
https://github.com/donovanglover/nix-config

ZephyrCodesStuff
   ZephyrCodesStuff built the Vencord css template for use with pywal.
https://github.com/ZephyrCodesStuff/pywal-vencord

yarmo.eu
   The playerctl module shown on this website helped me understand more about how playerctl interacts with polybar.
https://yarmo.eu/blog/playerctl-polybar/

runningnak3d
   Out of all the cava modules for polybar, this one worked the best for my usecase. It will disappear when no audio is playing, which was my biggest priority.
https://gist.github.com/runningnak3d/1b9e2df0239f7326965d918829828bd1

Other pieces of the puzzle:
https://gitlab.com/es20490446e/colors
https://gist.github.com/wimstefan/64e17d257d07b666079628a7e1859823
