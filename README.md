# Jellyfin-NVIDIA-Docker-Compose
My Jellyfin Docker Compose file with Nvidia GPU on Ubuntu Server

> [!NOTE]
> This repo is for Ubuntu Server
> This repository is just the docker compose file, you will need to install [Nvidia Toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html) And [Docker](https://docs.docker.com/engine/install/ubuntu/)

> [!NOTE]
> This repo uses a network called `backend` which is created in my reverse proxy.

### Installation Instructions
Once you install Docker and Nvidia Toolkit, you need to get the path of where the Jellyfin data mounts will go. I like to keep everything in the home directory, but you can select another location

1. Go to the desire destination in this case the home directory for the current user with `cd ~`
2. Create the jellyfin directory and enter that directory `mkdir jellyfin && cd jellyfin`
3. Clone the repo with `git clone https://github.com/CodeFallacy/Jellyfin-NVIDIA-Docker-Compose.git`
4. Modify the `.env` file. set `COMMON_PATH` with the path of Jellyfin directory we just created. in this case `/home/username/jellyfin`
5. Then start the container in detached mode with `docker compose up -d`
