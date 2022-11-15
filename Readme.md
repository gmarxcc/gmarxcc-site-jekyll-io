# Readme

## During first run
The container was created using:
```
docker run -it --rm --volume="$PWD:/srv/jekyll" -p 4000:4000 jekyll/jekyll  /bin/bash
```
then, several commands were used to create the site and its basic pages:
```
$ jekyll new name-of-site

```
after this we can just call the docker commands to build and serve the site.

```
$ docker run -it --rm --volume="$PWD:/srv/jekyll" -p 4000:4000 jekyll/jekyll  jekyll build --incremental
```

then, to serve the site just use:
```
$ docker run -it --rm --volume="$PWD:/srv/jekyll" -p 4000:4000 jekyll/jekyll  jekyll rever 
```

## To Run the container with Traefik##  
The container is prepared to work with Traefik. Thus, to serve and build the page just run:
 
```
docker-compose up -d
```

To update the build execute:
```
docker-compose exec  jekyll /bin/bash jekyll build --incremental --verbose
```

where `jekyll` is the service name on the `docker-compose.yml` file. 

Finally, if you want to execute the bash to explore the container use: 
```
docker-compose exec  jekyll /bin/bash 
```
