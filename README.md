
# 📦 MySQL Docker Setup

This repository contains a **Dockerized MySQL setup** that allows you to quickly build and run a MySQL container using Docker.
It demonstrates how to create a **custom MySQL Docker image**, run containers, and manage databases using Docker.

---

# 🚀 Project Overview

This project demonstrates:

* Building a **custom MySQL Docker image**
* Running MySQL using Docker containers
* Managing databases inside containers
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
docker build -t mysql-custom .
```

---

# ▶️ Run the MySQL Container

```bash
docker run -d \
-p 3306:3306 \
-e MYSQL_ROOT_PASSWORD=rootpassword \
--name mysql-container \
mysql-custom
```

---

# 🔍 Check Running Containers

```bash
docker ps
```

---

# 🗄 Connect to MySQL Container

```bash
docker exec -it mysql-container mysql -u root -p
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
* Using Git for version control
* Deploying projects on GitHub

---

# 👨‍💻 Author

**Adnan Khan**
Computer Science Engineering Student

🔗 LinkedIn
[www.linkedin.com/in/mohammad-adnan-khan-8099802b1](http://www.linkedin.com/in/mohammad-adnan-khan-8099802b1)

---
