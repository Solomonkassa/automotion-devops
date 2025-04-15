# Automotion DevOps Toolkit

**Enterprise-Grade Shell Automation Framework for Modern DevOps Workflows**  
> A robust CLI-first automation suite to manage Docker, NGINX, PostgreSQL, MySQL, Kubernetes, CI/CD, Cloud provisioning, and more using advanced modular shell scripting. Ideal for production-grade infrastructure and system administration.

---

## 🌟 Features

- ✅ **APT Installable CLI** — `sudo apt install automotion`
- ✅ **Multi-module Support** — Docker, NGINX, PostgreSQL, MySQL, Kubernetes, CI/CD
- ✅ **Dynamic Configuration** — `.env` templates, runtime variables
- ✅ **Production-ready NGINX & Docker Setup**
- ✅ **Kubernetes Deployment Manifests**
- ✅ **Robust Logging and Error Handling**
- ✅ **Backup & Restore Modules**
- ✅ **Self-hostable APT repository for your organization**

---

## 🗂️ File Structure

```shell
automotion-devops/
├── DEBIAN/                       # Control file for dpkg (.deb packaging)
├── usr/
│   └── local/
│       └── bin/
│           └── automotion       # CLI executable launcher
├── opt/
│   └── automotion/              # Core framework
│       ├── core/                # Logger, env loader, CLI base
│       ├── modules/             # NGINX, Docker, DBs, K8s, CI/CD
│       │   ├── docker/
│       │   ├── nginx/
│       │   ├── databases/
│       │   │   ├── postgres/
│       │   │   └── mysql/
│       │   ├── k8s/
│       │   ├── ci-cd/
│       │   └── cloud/
│       ├── templates/           # .env, .conf, .yml templates
│       ├── logs/                # Audit and task logs
│       ├── docs/                # Developer documentation
│       └── assets/              # Banners, logos, shell colors
```

---

## ⚙️ Installation

### 🔧 Method 1: Local Installation with `.deb`

```bash
git clone https://github.com/your-org/automotion-devops.git
cd automotion-devops
dpkg-deb --build .
sudo dpkg -i automotion-devops.deb
```

### 🌐 Method 2: Install from Custom APT Repo

```bash
echo "deb [trusted=yes] https://yourdomain.com/apt ./" | sudo tee /etc/apt/sources.list.d/automotion.list
sudo apt update
sudo apt install automotion
```

---

## 🚀 CLI Usage

```bash
automotion nginx       # Deploy NGINX reverse proxy via Docker
automotion docker      # Docker image build, prune, logs
automotion postgres    # PostgreSQL install and configuration
automotion mysql       # MySQL secure install + .env templating
automotion k8s         # Apply Kubernetes manifests
automotion help        # CLI command reference
```

---

## 🧱 Modules Overview

| Module       | Path                                 | Description                             |
|--------------|--------------------------------------|-----------------------------------------|
| Docker       | `modules/docker/`                    | Build, clean, prune, push, compose       |
| NGINX        | `modules/nginx/`                     | Docker-based reverse proxy automation    |
| PostgreSQL   | `modules/databases/postgres/`        | Secure install, init.sql, envs          |
| MySQL        | `modules/databases/mysql/`           | Secure install, SQL dump/load           |
| Kubernetes   | `modules/k8s/`                       | Helm/YAML deployments and ingress        |
| CI/CD        | `modules/ci-cd/`                     | GitHub Actions / GitLab pipeline setup  |
| Cloud        | `modules/cloud/`                     | AWS CLI, GCP SDK, Terraform base        |

---

## 🧰 Templates

Pre-bundled configs available in `templates/`:

- `docker-compose.yml`
- `nginx.conf`, `default.conf`
- `postgres.env`, `init.sql`
- `mysql.env`, `setup.sql`
- `k8s/*.yaml`

---

## 📜 Logging & Auditing

- Logs stored in `logs/automation.log`
- Each command logs output, errors, timestamps
- Useful for rollback, audit trails, monitoring

---

## 📖 Documentation

```shell
docs/
├── install.md
├── README.md
└── modules/
    ├── docker.md
    ├── nginx.md
    ├── postgres.md
    ├── mysql.md
    ├── k8s.md
    └── ci-cd.md
```

---

## 🤝 Contributing

We welcome modules, templates, and patches.

```markdown
1. Fork the repo
2. Create a feature branch
3. Follow standards in `core/logger.sh`, `env.sh`
4. Submit a detailed pull request
```

---

## 🔐 Security Practices

- Secrets via `.env` files — never hardcoded
- Isolated execution environments encouraged
- Logs redact sensitive credentials
- Supports container-based sandbox execution

---

## 🧩 Roadmap

- [ ] Web UI Dashboard (Flask/Django)
- [ ] Terraform + Ansible integrations
- [ ] GitOps Remote Deployment via SSH
- [ ] Secrets Manager Integration

---

## 📝 License

**MIT License**  
© [Jedan Code Academy](https://jedancodeacademy.com)

---

## 👨‍💻 Author

Built with 💚 by [Solomon Kassa](https://solomonkassa.et)  
Empowering DevOps engineers with elegant, scalable automation tools.

