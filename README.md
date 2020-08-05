# headphones docker
```bash
sudo mkdir -p  /var/lib/docker/storage/headphones/{config,downloads,music}

sudo docker create \
  --name=headphones \
  -e PUID=1000 \
  -e PGID=1000 \
  -e TZ=America/New_York \
  -p 8181:8181 \
  -v /var/lib/docker/storage/headphones/config:/config \
  -v /var/lib/docker/storage/headphones/downloads:/downloads \
  -v /var/lib/docker/storage/headphones/music:/music \
  --restart unless-stopped \
  linuxserver/headphones
```  
