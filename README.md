# FinanceMe - DevOps CI/CD Project (Banking & Finance Domain)

FinanceMe is a DevOps-driven microservices project built for the banking and financial services domain. It demonstrates automation of application deployment using industry-standard DevOps tools such as Jenkins, Docker, Terraform, Ansible, and AWS.

---

## 🏦 Project Overview

**FinanceMe** simulates a modern banking platform offering services like account creation, policy management, and account updates. The backend is developed using **Spring Boot**, connected to an **AWS RDS MySQL database**, and deployed in a fully automated CI/CD pipeline.

---

## 🚀 CI/CD Pipeline Highlights

1. Code push to GitHub `main` branch triggers Jenkins pipeline
2. Jenkins:
   - Pulls the latest code
   - Compiles via Maven
   - Runs unit & integration tests (JUnit/TestNG)
   - Builds Docker image
   - Pushes image to Docker Hub
3. **Terraform** provisions new EC2 instances
4. **Ansible** installs dependencies & prepares environments
5. App deployed to **Test Server**
6. Selenium runs automated test cases
7. On success, app is auto-deployed to **Production Server**
8. **Prometheus + Grafana** monitor system metrics

---

## 🧪 REST API Endpoints

| Endpoint | Method | Description |
|---------|--------|-------------|
| `/createAccount` | POST | Create a new bank account |
| `/updateAccount/{accountNo}` | PUT | Update account details |
| `/viewPolicy/{accountNo}` | GET | View policy info for an account |
| `/deletePolicy/{accountNo}` | DELETE | Delete policy for a given account |

> **Database**: Uses AWS RDS (MySQL)  
> **Data**: Preloaded account and policy information

---

## 🔧 Tech Stack

| Category | Tools |
|----------|-----------------------------|
| Language | Java (Spring Boot) |
| Build Tool | Maven |
| Version Control | Git + GitHub |
| CI/CD | Jenkins |
| Containerization | Docker |
| Deployment | AWS EC2 via Terraform + Ansible |
| Testing | JUnit, Selenium, TestNG Reports |
| Monitoring | Prometheus + Grafana |
| Database | AWS RDS - MySQL |

---

## 📦 Project Structure

finance-me/
├── src/ # Spring Boot source code
├── test/ # JUnit & Selenium test cases
├── Dockerfile # Docker build instructions
├── Jenkinsfile # Jenkins CI/CD pipeline
├── terraform/ # Infra-as-code scripts
├── ansible/ # Configuration management
├── monitoring/ # Prometheus & Grafana configs
├── project-report.pdf
└── README.md


---

## 📊 Monitoring Dashboard (via Grafana)

Real-time system metrics displayed:
- CPU Utilization
- Disk Space
- Available Memory

> Metrics collected using **Prometheus Node Exporter**

---

## 📎 Reference Repository

This project is based on StarAgile's certification POC:  
🔗 [https://github.com/StarAgileDevOpsTraining/star-agile-banking-finance](https://github.com/StarAgileDevOpsTraining/star-agile-banking-finance)

---

## 👨‍💻 Author

**Anmol Upadhyay**  
DevOps Engineer  
📧 anmolupadhayay80@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/anmolupadhyay2025)

---

## 📜 License

This project is for educational and demonstration purposes only.
