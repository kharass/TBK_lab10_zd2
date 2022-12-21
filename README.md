```
docker swarm init
docker stack deploy -c img-gallery.yml image-gallery

docker-compose -f img-gallery.yml -f img-gallery-v2.yml --log-level ERROR config > stack.yml
docker stack deploy -c stack.yml image-gallery
docker service ps image-gallery_iotd
```
