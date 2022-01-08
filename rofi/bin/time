#!/usr/bin/env bash

wdir="$HOME/.config/leftwm/themes/current"
dir="$wdir/rofi/applets/menu/configs"
rofi_command="rofi -theme $dir/time.rasi"

## Get time and date
TIME="$(date +"%I:%M %p")"
DN=$(date +"%A")
MN=$(date +"%B")
DAY="$(date +"%d")"
MONTH="$(date +"%m")"
YEAR="$(date +"%Y")"

options="$DAY\n$MONTH\n$YEAR"

## Main
chosen="$(echo -e "$options" | $rofi_command -p "   at $TIME on $DN in $MN" -dmenu -selected-row 1)"
