# DISABLED LAPTOP KEYBOARD ON UBUNTU

### 1. Edit file /etc/default/grub

>vi /etc/default/grub

### 2. Find

>GRUB_CMDLINE_LINUX_DEFAULT="quiet splash"

### 3. Replace it with

>GRUB_CMDLINE_LINUX_DEFAULT="quiet splash i8042.nokbd"

### 4. Regenerate grub.cfg with

>update-grub2

### 5. Reboot Laptop, Built in keyboard will be disabled by default. No need to run xinput command and manually disable each time.
