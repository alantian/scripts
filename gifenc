#!/bin/sh
# Converting vdeo to gif, with turned params for palette for better quality.

palette="/tmp/palette.png"

filters="fps=15,scale=1080:-1:flags=lanczos"

ffmpeg -v warning -i $1 -vf "$filters,palettegen" -y $palette
ffmpeg -v warning -i $1 -i $palette -lavfi "$filters [x]; [x][1:v] paletteuse" -y $2

reset
