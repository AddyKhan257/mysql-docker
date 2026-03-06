# 📦 MySQL Docker Setup

This repository contains a **Dockerized MySQL setup** that allows you to quickly build and run a MySQL container using Docker.
It demonstrates how to create a **custom MySQL Docker image**, run containers, and manage databases using Docker.

---

# 🚀 Project Overview

This project demonstrates:

* Building a **custom MySQL Docker image**
* Running MySQL using Docker containers
* Managing databases inside containers
* Using **Docker Volumes for persistent storage**
* Version control using Git
* Publishing projects on GitHub

---

# 🛠 Technologies Used

* Docker
* MySQL
* Linux (Ubuntu)
* Git
* GitHub

---

# 📂 Project Structure

```
mysql-docker
│
├── Dockerfile
├── README.md
```

---

# ⚙️ Build the Docker Image

Run the following command to build the MySQL Docker image:

```bash
docker build -t mysql-cont .
```

Check the built image:

```bash
docker images
```

---

# ▶️ Run the MySQL Container

```bash
docker run -d \
-p 3306:3306 \
-e MYSQL_ROOT_PASSWORD=rootpassword \
--name mysql-container \
mysql-cont
```

Check running containers:

```bash
docker ps
```

---

# 🔍 Check Running Containers

```bash
docker ps
```

To see all containers:

```bash
docker ps -a
```

---

# 🗄 Connect to MySQL Container

```bash
docker exec -it mysql-container mysql -u root -p
```

You can also open a bash shell inside the container:

```bash
docker exec -it mysql-container bash
```

---

# 💾 Docker Volumes (Persistent Storage)

Docker volumes allow you to **store MySQL data outside the container**.
This ensures that **data is not lost even if the container is deleted**.

---

## Create a Docker Volume

```bash
docker volume create mysql-vol
```

List available volumes:

```bash
docker volume ls
```

Inspect the volume:

```bash
docker volume inspect mysql-vol
```

---

## Run MySQL Container with Volume

Mount the volume to the MySQL data directory:

```bash
docker run -d \
-v mysql-vol:/var/lib/mysql \
-p 3306:3306 \
-e MYSQL_ROOT_PASSWORD=060606 \
--name mysql-container \
mysql-cont
```

Now MySQL will store its database files inside **mysql-vol**.

---

# 📜 View Container Logs

```bash
docker logs <container_id>
```

Example:

```bash
docker logs mysql-container
```

---

# 🧹 Docker Cleanup Commands

Stop container:

```bash
docker stop <container_id>
```

Remove container:

```bash
docker rm <container_id>
```

Remove image:

```bash
docker rmi <image_id>
```

Remove all images:

```bash
docker rmi -f $(docker images -aq)
```

Remove unused Docker resources:

```bash
docker system prune -a
```

---

# ☁️ Push Image to Docker Hub

Login to Docker Hub:

```bash
docker login
```

Tag the image:

```bash
docker tag mysql-custom username/mysql-custom
```

Push the image:

```bash
docker push username/mysql-custom
```

---

# 📚 What I Learned

Through this project I practiced:

* Creating Docker images
* Running and managing containers
* Working with MySQL inside Docker
* Using **Docker volumes for persistent storage**
* Using Git for version control
* Deploying projects on GitHub

---

# 👨‍💻 Author

**Adnan Khan**
Computer Science Engineering Student

🔗 LinkedIn
[www.linkedin.com/in/mohammad-adnan-khan-8099802b1](http://www.linkedin.com/in/mohammad-adnan-khan-8099802b1)

---
