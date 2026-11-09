sudo podman stop

# Eliminar todos los contenedores
podman rm -af

# Eliminar todos los pods
podman pod rm -af

# Eliminar todas las imágenes
podman rmi -af

Instalar ADguard
sudo podman run -d \
  --name adguard \
  --restart always \
  -v ~/adguard/conf:/opt/adguardhome/conf \
  -v ~/adguard/work:/opt/adguardhome/work \
  -p 53:53/tcp \
  -p 53:53/udp \
  -p 8084:3000/tcp \
  -p 443:443/tcp \
  -p 853:853/tcp \
  docker.io/adguard/adguardhome:latest
