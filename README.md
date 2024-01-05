# Nextcloud Docker compose environment

Usage

Start and run detached:
`$ docker compose up -d`

Bring the environment down:
`$ docker compose down`

Forcefully rebuild containers
`$ docker compose up --force-recreate --build -d`

Use 'occ':  
Create alias in ~/.bash_aliases:
echo "alias occ='docker exec -it -u www-data nextcloud-app-1 php occ'" >> ~/.bash_aliases
