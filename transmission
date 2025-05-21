sudo apt update
sudo apt install transmission-daemon
sudo systemctl stop transmission-daemon
sudo nano /etc/transmission-daemon/settings.json

Indicar carpeta a donde descargar
"download-dir": "/mnt/sdXX/Carpeta"
"incomplete-dir": "/mnt/sdXX/Incomplete"
"incomplete-dir-enabled": true

Whitelist de ip local
"rpc-whitelist": "127.0.0.1,192.168.*.*"
"rpc-whitelist-enabled": true:
Usuario web
"rpc-username": "tu_usuario_web":
"rpc-password": "tu_contraseña_web":

Crear carpeta a donde se descargara
sudo mkdir -p /mnt/sdXX/Carpeta
sudo mkdir -p /mnt/sdXX/Incomplete

Configurar usuario de tranmission
sudo chown -R debian-transmission:debian-transmission /mnt/sdXX/Carpeta
sudo chown -R debian-transmission:debian-transmission /mnt/sdXX/Incomplete
sudo chmod -R 775 /mnt/sdXX/Downloads
sudo chmod -R 775 /mnt/sdXX/Incomplete

sudo systemctl start transmission-daemon
sudo systemctl enable transmission-daemon
