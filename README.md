# Mongo

A MongoDB with mongo-express. 

- First I started without a persistent volume so there was no volume code in the docker-compose file and it ran fine but when the contrainers are removed the data is lost. 

- Second I added a persistent volume to the docker engine and then made the docker-compose file use the external persistent volume to store the database. 

# Notes

- You can check the commits for the changes. 

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

## Create persistent volume sharedb

```
sudo docker volume create sharedb
```

## Docker compose Build Detached

```
sudo docker compose up --build -d
```

When done press Ctrl + C to quit

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


# Diagram

<p align="center">
<a href="https://github.com/RichardDeodutt/Mongo/blob/main/images/Mongo.drawio.png"><img src="https://github.com/RichardDeodutt/Mongo/blob/main/images/Mongo.drawio.png" />
</p>