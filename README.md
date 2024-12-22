# myNextcloudDockerSetup
#1 main command to run after stopping all containers by going to https://localhost:8080
docker run --init --sig-proxy=false --name nextcloud-aio-mastercontainer --restart always --publish 80:80 --publish 8080:8080 --publish 8443:8443 --volume nextcloud_aio_mastercontainer:/mnt/docker-aio-config --volume //var/run/docker.sock:/var/run/docker.sock:ro --env NEXTCLOUD_DATADIR="/run/desktop/mnt/host/c/Users/VenkuGamer/Documents/NextCloudData" nextcloud/all-in-one:latest

#2 Values of DataDir arg (change after full copy between them--- https://github.com/nextcloud/all-in-one?tab=readme-ov-file#how-to-change-the-default-location-of-nextclouds-datadir)
  "/run/desktop/mnt/host/c/Users/VenkuGamer/Documents/NextCloudData"
  "/run/desktop/mnt/host/d/NextCloudData"
