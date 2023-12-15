# Nextcloud Docker compose environment

Usage

Start and run detached:
`$ docker compose up -d`

Bring the environment down:
`$ docker compose down`

Forcefully rebuild containers
`$ docker compose up --force-recreate --build -d`

Use 'occ':
- First; find container id of app container:
  `docker container ls -f "name=nextcloud-app-1"`
docker exec -ti -u www-data <container_id> php occ <occ_command>
