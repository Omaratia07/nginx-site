# Dockerized Nginx Website 🌐

This project demonstrates how to host a **static website** using **Nginx** inside a Docker container.

---

## 📂 Project Structure

* **Dockerfile** → Instructions to build the Nginx image.
* **website/** → Contains the static website files (HTML, CSS, JS).

---

## ⚙️ Steps to Run

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/<YourUserName>/nginx-website-docker.git
cd nginx-website-docker
```

### 2️⃣ Build the Docker Image

```bash
docker build -t my-nginx-site .
```

### 3️⃣ Run the Container

```bash
docker run -d -p 8080:80 my-nginx-site
```

### 4️⃣ Open the Website

Visit in your browser:
👉 [http://localhost:8080](http://localhost:8080)

---
🖼️ Screenshot

<img width="1918" height="938" alt="Screenshot from 2025-09-13 17-33-41" src="https://github.com/user-attachments/assets/b641a35a-557f-4f72-95a8-dd0cfa5f4812" />


## 🐳 Dockerfile Explained

```dockerfile
FROM nginx:alpine              # Use Nginx lightweight image
COPY website/ /usr/share/nginx/html  # Copy website files into Nginx default directory
EXPOSE 80                      # Expose port 80 for HTTP traffic
WORKDIR /app
 
```

* **FROM** → uses the lightweight `nginx:alpine` image.
* **COPY** → copies your local website files into Nginx’s default HTML directory.
* **EXPOSE** → tells Docker that the container will listen on port 80.

---

## 🎯 What You’ll Learn

* How to serve a static website using **Nginx + Docker**.
* How to build and run a **custom Nginx image**.
* How to expose and map container ports.

---

## 🚀 Next Steps

* Push your Docker image to a registry (Docker Hub, AWS ECR, Nexus).
* Deploy it to a cloud service or Kubernetes cluster.
* Automate the build & deploy process with **GitHub Actions**.


