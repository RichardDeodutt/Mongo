# Mongo

A MongoDB with mongo-express

## Install Docker

```
curl -fsSL https://get.docker.com -o get-docker.sh
```

```
sudo sh get-docker.sh
```

## Get this Repo

```
git clone https://github.com/RichardDeodutt/Mongo.git
```

```
cd Mongo
```

## Docker compose Build Detached

```
sudo docker compose up --build -d
```

When done press Ctrl + C to quit

## Create persistent volume sharedb

```
sudo docker volume create sharedb
```

# One Liner which runs in the background

```
curl -fsSL https://get.docker.com -o get-docker.sh && sudo sh get-docker.sh && git clone https://github.com/RichardDeodutt/Mongo.git && cd Mongo && git pull && sudo docker create volume && sudo docker compose up --build -d
```

# Take down running containers from compose

```
sudo docker compose down
```

# Remove persistent volume sharedb

```
sudo docker volume rm sharedb
```

# Rerun in the background

```
git pull && sudo docker compose down && sudo docker compose up --build -d
```