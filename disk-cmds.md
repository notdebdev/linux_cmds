Crear particion
  sudo gdisk /dev/sdX
  n
  enter
  enter
  enter
  enter
  w
  y
  sudo mkfs.ext4 /dev/sdX
  sudo partprobe /dev/sdX

Montar discos
  sudo mkdir /mnt/sdXX
  sudo mount /dev/sdXX mnt/sdXX

sudo apt install samba
sudo smbpasswd -a peliculas

sudo cp /etc/samba/smb.conf /etc/samba/smb.conf.backup
sudo nano /etc/samba/smb.conf
[Juegos]
path = /mnt/sdXX
browseable = yes
read only = no
guest ok = no
valid users = peliculas
create mask = 0644
directort mask = 0755
