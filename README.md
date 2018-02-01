# mkinitcpio-btinput
mkinitcpio hook to enable bt support during boot

This code is based on the work of Aline Freitas <aline@alinefreitas.com.br> and the original Arch Linux AUR package mkinitcpio-bluetooth-input which is no longer available on github.


# Instructions

1. Make sure your BT keyboard is paired with your PC and works correctly
2. Find the BT profile ID of your keyboard
* For Arch Linux, go to ```/var/bluetooth``` and inspect all folders until you find your keayboard's
3. Paste the ID you found in step 2 into ```hook_btinput```, replacing the ID in the following line ```echo -e 'power on\nconnect 00:11:22:33:44:55\nquit' | bluetoothctl```
4. Reapply this PKGBUILD after every kernel update to not loose BT connectivity at the next boot
