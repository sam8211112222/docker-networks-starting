[//]: # (1&#41; docker run -d --name mongodb mongo  )

[//]: # (2&#41; docker container inspect mongodb  )

[//]: # (3&#41; docker build -t favorites-node .  )

[//]: # (4&#41; docker run --name favorites -d --rm -p 3000:3000 favorites-node  )

1) docker network create favNet
2) docker run -d --name mongodb --network favNet mongo 
3) docker rmi favorites-node
4) modify container name in mongoose.connect(
   'mongodb://YOUR_CONTAINER_NAME:27017/swfavorites',
5) docker build -t favorites-node .
6) docker run --name favorites --network favNet -d --rm -p 3000:3000 favorites-node
