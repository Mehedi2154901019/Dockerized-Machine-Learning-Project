# Dockerized Machine Learning Project

This project is a **machine learning app** to predict laptop prices using `scikit-learn` and `Streamlit`. The project has been fully Dockerized and pushed to Docker Hub.

---

## 📦 Features

- Predict laptop prices based on various specs
- Built with `scikit-learn` and `streamlit`
- Dockerized for portability and deployment
- Docker image available on Docker Hub

---

## Getting Started

### 1. Clone the Repository

```bash
cd Desktop
git clone https://github.com/campusx-official/laptop-price-predictor-regression-project.git
cd laptop-price-predictor-regression-project
```

### 2. Add Required Files

#### Create `requirements.txt`

```txt
streamlit
scikit-learn
```

#### Create `Dockerfile`

```Dockerfile
FROM python:3.7

WORKDIR /app

COPY . /app

RUN pip install -r requirements.txt

EXPOSE 8501

CMD ["streamlit", "run", "app.py"]
```

---

## 🛠️ Build & Run with Docker

### 1. Build Docker Image

```bash
docker build -t yourdockerhubname/laptop-price-predictor .
```

### 2. Run Docker Container

```bash
docker run -p 8501:8501 yourdockerhubname/laptop-price-predictor
```

> 🔗 Open your browser and go to: [http://localhost:8501](http://localhost:8501)

---

## ☁️ Push to Docker Hub

### 1. Log in to Docker Hub

```bash
docker login
```

### 2. Push the image

```bash
docker push yourdockerhubname/laptop-price-predictor
```

---

## 📥 Pull from Docker Hub (Optional)

If the image exists on Docker Hub:

```bash
docker pull yourdockerhubname/laptop-price-predictor
docker run -p 8501:8501 yourdockerhubname/laptop-price-predictor
```

---

## ✅ What I Learned

- Cloning projects from GitHub
- Writing a Dockerfile
- Creating and using `requirements.txt`
- Building, pushing, pulling, and running Docker images
- Deploying Streamlit apps via Docker Desktop and Docker Hub

---

## 📚 License

This project is for learning purposes. Original model belong to [CampusX](https://github.com/campusx-official).
