# 📝 Flask ToDo App with Authentication, Docker, Ansible, EC2 & CI/CD

This is a full-stack ToDo application built using **Flask**, featuring **user authentication (SQLite)**, containerized with **Docker**, provisioned to **AWS EC2** using **Ansible**, and automated via **GitHub Actions CI/CD**.

---

## 📌 Features

- ✅ Add, delete ToDo tasks
- 🔐 User authentication using **Flask-Login** and **SQLite**
- 🐳 Dockerized for easy deployment
- ☁️ EC2 instance provisioning with **Ansible**
- 🚀 CI/CD pipeline setup using **GitHub Actions**

---

## 🛠️ Tech Stack

| Purpose               | Technology             |
|-----------------------|------------------------|
| Backend Framework     | Flask                  |
| Authentication        | Flask-Login + SQLite   |
| Database (ToDos)      | SQLite                 |
| Containerization      | Docker                 |
| Provisioning & Config | Ansible                |
| Deployment Target     | AWS EC2 (Amazon Linux) |
| Automation            | GitHub Actions         |

---

### 🧪 GitHub Actions CI/CD

The CI/CD pipeline is defined in .github/workflows/main.yml. On every push to main:

- Code is linted/tested.
- Docker image is built.
- Code is pushed to EC2 and the container is restarted using Ansible.

### EC2 Deployment with Ansible:

#### 🔧 Prerequisites:

- AWS CLI configured
- SSH key setup for EC2
- Python + Ansible installed locally

### 🪄 Run Ansible Playbook

```
ansible-playbook ansible/playbooks/ec2-instance.yml
```

_Follwing command wil:_

- Create a security group
- Launch an EC2 instance
- Copy your app code
- Build Docker container on remote host
- Run the Flask app in container