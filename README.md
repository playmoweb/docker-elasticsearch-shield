# Docker elasticsearch with shield

## Start a container
### interactive :
```
docker run --name myproject-elasticsearch -v /tmp/esdata:/usr/share/elasticsearch/data -it playmoweb/elasticsearch-shield elasticsearch -Des.node.name="myproject"
```

### daemon :
```
docker run --name myproject-elasticsearch -v /tmp/esdata:/usr/share/elasticsearch/data -d playmoweb/elasticsearch-shield elasticsearch -Des.node.name="myproject"
```

## Add an admin user :
```
docker exec -it myproject-elasticsearch /usr/share/elasticsearch/bin/shield/esusers useradd myuser -p mypassword -r admin
```

## More infos
- [Official elasticsearch docker image documentation](https://github.com/docker-library/docs/tree/master/elasticsearch)
