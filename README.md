# Automotion++ Enterprise DevOps Platform

**Next-Gen Infrastructure Automation Suite with AIOps Integration**
> A comprehensive CLI and API-driven platform for managing cloud-native infrastructure, database orchestration, CI/CD pipelines, and observability with built-in security compliance checks.

---

## 🌟 Core Capabilities

- ✅ **Multi-Cloud Provisioning** (AWS/GCP/Azure/Terraform)
- ✅ **Database Cluster Management** (PostgreSQL/MySQL/MongoDB/Redis)
- ✅ **Kubernetes Operator Framework** (CRDs, Helm, ArgoCD)
- ✅ **Advanced Networking** (NGINX+, HAProxy, Traefik, Istio)
- ✅ **GitOps Workflows** (GitHub Actions, GitLab CI, Argo Workflows)
- ✅ **Security & Compliance** (Vault, Cert Manager, CIS Benchmarks)
- ✅ **Observability Stack** (Prometheus, Grafana, ELK, OpenTelemetry)
- ✅ **AI-Powered Anomaly Detection** (ML-based log analysis)

---

## 🗂️ Enterprise File Structure

```shell
/opt/automotion-enterprise/
├── bin/                          # CLI entrypoints
│   ├── autoctl                   # Main CLI
│   ├── autoctl-ai                # AIOps assistant
│   └── autoctl-sec               # Security scanner
├── lib/                          # Core libraries
│   ├── framework/
│   │   ├── auth.sh               # IAM integration
│   │   ├── crypto.sh             # PKI management
│   │   └── audit.sh              # Compliance logging
│   └── modules/
│       ├── cloud/
│       │   ├── aws/              # AWS Landing Zone
│       │   ├── gcp/              # GCP Foundation
│       │   └── terraform/        # Multi-cloud IaC
│       ├── databases/
│       │   ├── postgres/         # HA Patroni clusters
│       │   ├── mysql/            # Group replication
│       │   └── mongodb/          # Sharded clusters
│       ├── k8s/
│       │   ├── operators/        # Custom CRDs
│       │   ├── helm/             # Chart repository
│       │   └── gitops/           # ArgoCD configs
│       ├── networking/
│       │   ├── nginx/            # OSS/Plus configurations
│       │   ├── haproxy/          # TCP/HTTP load balancing
│       │   └── service-mesh/     # Istio/Linkerd
│       └── pipelines/
│           ├── github-actions/   # Composite actions
│           ├── gitlab-ci/        # Templates
│           └── tekton/           # Kubernetes-native CI/CD
├── etc/
│   ├── compliance/               # CIS benchmarks
│   ├── policies/                 # OPA/Gatekeeper
│   └── secrets/                  # Vault templates
├── var/
│   ├── log/                      # Structured JSON logs
│   ├── cache/                    # Terraform states
│   └── lib/                      # Database backups
├── api/                          # REST/gRPC interfaces
└── ui/                           # React dashboard

```

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
echo "deb [trusted=yes] https://toolkit.jedantechnology.site/apt ./" | sudo tee /etc/apt/sources.list.d/automotion.list
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
© [Jedan Code Academy](https://jedantechnology.site)

---

## 👨‍💻 Author

Built with 💚 by [Solomon Kassa](https://solomonkassa.et)  
Empowering DevOps engineers with elegant, scalable automation tools.

