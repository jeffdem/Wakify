# Wakify
A spotify alarm clock Raspberry based


#!/bin/bash
PATH=/usr/local/sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin
export DISPLAY=:0.0
exec > /etc/network/if-up.d/spotify.log
echo $(date)
echo 'starting'
sleep 60
echo 'sleep'
mpc clear
echo 'clear'
mpc add spotify:user:spotify:playlist:3ZgmfR6lsnCwdffZUan8EA
echo 'add playlist'
mpc random on
echo 'random'
mpc repeat on
echo 'repeat'
mpc volume 10
echo 'volume'
mpc play
