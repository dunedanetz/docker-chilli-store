Chilli Store – DevOps Case Study

📖 Overview
Chilli Store is a demo e-commerce web application for exploring DevOps practices.

It evolves step by step into a full DevOps project, covering:
- Application development (Flask, Python, HTML/CSS).
- Automation (Bash, Python, Ansible).
- Containerization (Docker, docker-compose).
- CI/CD pipelines (GitHub Actions / GitLab CI).
- Deployment (Kubernetes).
- Cloud fundamentals (Azure AZ-900).

✨ Features:

🛒 Browse chilli products by category (Mild, Hot, Super Hot).

🌶️ Each chilli has name, description, price, and image.

📂 Categories and product data stored in Postgres.

🔐 Authentication planned (future enhancement).

📊 Logging and monitoring (future enhancement with Prometheus + Grafana).


🛠️ Tech Stack
- Backend: Python (Flask)
- Frontend: HTML, CSS, Jinja templates
- Database: PostgreSQL (Dockerized)
- Automation: Bash, Python scripts, Ansible
- Containerization: Docker, docker-compose
- Orchestration: Kubernetes (Minikube/k3s)
- CI/CD: GitHub Actions / GitLab CI
- Cloud: Azure (AZ-900 Fundamentals certified)

📂 Repository Structure
bash
Copy
Edit
chilli-store/
│── src/               # Flask app code
│   ├── templates/     # HTML pages
│   ├── static/        # Images, CSS
│   └── app.py         # Flask app entry
│
│── db/                # Database schema, seed data
│── scripts/           # Bash/Python automation scripts
│── ansible/           # Ansible playbooks
│── k8s/               # Kubernetes manifests
│── docker/            # Dockerfile, docker-compose.yml
│── .github/workflows/ # CI/CD pipelines
│── README.md          # Project documentation
🚀 Setup & Run

Option 1 – Local (Dev)
# Clone repo
git clone https://github.com/YOURNAME/chilli-store.git
cd chilli-store/src

# Install dependencies
pip install -r requirements.txt

# Run Flask app
python app.py
App runs at: http://localhost:5000

Option 2 – Docker
# Build and run
docker-compose up --build

Option 3 – Kubernetes (Minikube)
kubectl apply -f k8s/
kubectl get pods
🔄 CI/CD
Build: Docker image built from Dockerfile.

Test: Run Flask unit tests.

Deploy: Push image to registry → deploy with Ansible/Kubernetes.

Pipeline example (GitHub Actions):

name: CI/CD
on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Build Docker image
        run: docker build -t chilli-store .
      - name: Run tests
        run: pytest
📸 Screenshots
(Add later once you have header, footer, categories, chilli images)

Home page

Product page

Categories view

📊 Roadmap
 Add chilli categories + products

 Dockerize app + Postgres

 Ansible playbooks for deployment

 CI/CD pipeline

 Kubernetes deployment

 Monitoring (Prometheus + Grafana)

 Authentication & login system

🏆 Certifications
Microsoft Certified: Azure Fundamentals (AZ-900) ✅

👤 Author
Emil Iliev
💼 LinkedIn

🐙 GitHub
