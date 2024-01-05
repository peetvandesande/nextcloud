# Nextcloud Docker compose environment

Usage  

Start and run detached:  
`$ docker compose up -d`  

Bring the environment down:  
`$ docker compose down`  

Forcefully rebuild containers  
`$ docker compose up --force-recreate --build -d`  

Use 'occ':  
<<<<<<< HEAD
Create alias in ~/.bash_aliases:
echo "alias occ='docker exec -it -u www-data nextcloud-app-1 php occ'" >> ~/.bash_aliases
=======
- First; find container id of app container:  
  `docker container ls -f "name=nextcloud-app-1"`  
docker exec -ti -u www-data <container_id> php occ <occ_command>  
>>>>>>> a8d488bf956cf38b88fd1c15ef48e5f84de6231f
