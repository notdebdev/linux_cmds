Instalaciones desde AUR
yay -S brave-bin faugus-launcher discord gpu-screen-recorder-git davinci-resolve umu-launcher heroic-games-launcher-bin zram-generator

Instalaciones desde repo oficial
sudo pacman -S btop gnome-disk-utility steam mangohud wine vlc vlc-plugin-ffmpeg libva-utils fastfetch obs-studio

Habilitar bluetooth
sudo systemctl enable --now bluetooth

Montaje hdd en fstab, método mas sencillo con gnome-disk-utility
mkdir /mnt/sdaX
lsblk -f -> copiar uuid y filesystem
sudo nano /etc/fstab
UUID=el-uuid-largo    /mnt/sdaX    filesystem    defaults    0 0
guardar cambios
sudo systemctl daemon-reload
sudo mount -a

zram generator
sudo nano /etc/systemd/zram-generator.conf
[zram0]
zram-size = ram / 2
compression-algorithm = zstd

sudo systemctl daemon-reload
sudo systemctl start systemd-zram-setup@zram0.service
zramctl
