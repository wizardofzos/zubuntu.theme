# zubuntu splash loader :)

## Instructions 

1. Install Plymouth themes:

`sudo apt install plymouth-themes`

2. create new plymouth themes folder

`
mkdir /usr/share/plymouth/themes/mainframetheme
`

3. Move all files from this repo into that folder

`
cp * /usr/share/plymouth/themes/mainframetheme
`

4. Setup the bootloader
```
 sudo update-alternatives --install /usr/share/plymouth/themes/default.plymouth default.plymouth /usr/share/plymouth/themes/mainframetheme/mainframetheme.plymouth 100
```

5. Select the default theme.
`sudo update-alternatives --config default.plymouth`
And select the number for your theme.

6. Update the initramfs image.

`
sudo update-initramfs -u
`

4. Now reboot.


## Credits

Made with https://github.com/jcklpe/Plymouth-Animated-Boot-Screen-Creator
(and some mucking about)
