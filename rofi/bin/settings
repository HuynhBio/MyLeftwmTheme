#!/usr/bin/env bash

wdir="$HOME/.config/leftwm/themes/current"
dir="$wdir/rofi/applets/menu/configs"
rofi_command="rofi -theme $dir/settings.rasi"

# Links
Fcitx=""
pulseaudio="墳"
networkmanager=""
#browser=""
#music=""
#settings=""

# Error msg
msg() {
	rofi -theme "$wdir/rofi/applets/styles/message.rasi" -e "$1"
}

# Variable passed to rofi
options="$Fcitx\n$pulseaudio\n$networkmanager"

chosen="$(echo -e "$options" | $rofi_command -p "Settings system" -dmenu -selected-row 0)"
case $chosen in
    $Fcitx)
		if [[ -f /usr/bin/fcitx-configtool ]]; then
			fcitx-configtool &
		else
			msg "No suitable terminal found!"
		fi
        ;;
    $pulseaudio)
		if [[ -f /usr/bin/pavucontrol ]]; then
			pavucontrol &
		else
			msg "No suitable file manager found!"
		fi
        ;;
    $networkmanager)
		if [[ -f /usr/bin/nm-connection-editor ]]; then
			nm-connection-editor &
		else
			msg "No suitable text editor found!"
		fi
        ;;
esac
