# 🎓 ScholarAI

<div align="center">

![ScholarAI Logo](https://img.shields.io/badge/ScholarAI-Research%20Platform-blue?style=for-the-badge&logo=education&logoColor=white)

**The Ultimate AI-Powered Research Companion for Academics**

*Built for Javafest 2025 - The Ultimate Battle of Brains & Bytes*

[![Java](https://img.shields.io/badge/Java-21-ED8B00?style=flat&logo=openjdk&logoColor=white)](https://openjdk.org/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.5.0-6DB33F?style=flat&logo=spring&logoColor=white)](https://spring.io/projects/spring-boot)
[![Next.js](https://img.shields.io/badge/Next.js-14+-000000?style=flat&logo=nextdotjs&logoColor=white)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0+-3178C6?style=flat&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Docker](https://img.shields.io/badge/Docker-Enabled-2496ED?style=flat&logo=docker&logoColor=white)](https://www.docker.com/)
[![License](https://img.shields.io/badge/License-Private-red?style=flat&logo=github&logoColor=white)](#license)

</div>

---

## 🌟 What is ScholarAI?

**ScholarAI** is a revolutionary AI-powered research platform that transforms how researchers work - from **idea** to **insight** to **publication**. Built as a comprehensive solution to eliminate the friction of juggling multiple tools throughout the research lifecycle.

### 🎯 The Problem We Solve

Researchers currently struggle with:
- **Fragmented Workflow**: Switching between dozens of single-purpose tools
- **Information Overload**: Manually sifting through thousands of papers
- **Context Loss**: Losing track of insights across different platforms
- **Citation Chaos**: Manually managing references and formatting
- **Collaboration Barriers**: No unified workspace for team research

### ✨ Our Solution

A **single, context-aware workspace** that seamlessly integrates:

🔍 **Intelligent Paper Discovery** - AI-powered search across multiple academic databases  
📄 **Smart PDF Analysis** - Automated extraction, summarization, and gap analysis  
💬 **Contextual Q&A Chat** - Highlight any passage for instant AI explanations  
📝 **AI-Augmented LaTeX Editor** - Live preview with intelligent writing assistance  
📊 **Impact Tracking Dashboard** - Monitor citations and research performance  
🤝 **Collaborative Workspaces** - Team-based project management  

---

## 🏗️ Architecture Overview

### 🔧 Technology Stack

<div align="center">

| **Frontend** | **Backend** | **AI Services** | **Infrastructure** |
|:---:|:---:|:---:|:---:|
| Next.js 14+ | Spring Boot 3.5.0 | FastAPI (Python) | Docker |
| TypeScript | Java 21 | Google Gemini | PostgreSQL |
| Tailwind CSS | Maven | RabbitMQ | Redis |
| Radix UI | JPA/Hibernate | Semantic Scholar API | Eureka Discovery |

</div>

### 🏢 Microservices Architecture

```
📦 ScholarAI Platform
├── 🎨 Frontend (Next.js)                    → Port 3000
├── 🚪 API Gateway (Spring Cloud)            → Port 8989
├── 🔍 Service Registry (Eureka)             → Port 8761
├── 👤 User Service (Authentication)         → Port 8081
├── 📂 Project Service (Research Projects)   → Port 8083
├── 🔔 Notification Service (Alerts)         → Port 8082
├── 🤖 AI Paper Search Agent (FastAPI)       → Port 8084
└── 🧠 AI Writing Assistant (FastAPI)        → Port 8085
```

### 🗂️ Repository Structure

Our project is organized across multiple repositories under the **Javafest2025** organization:

| Repository | Description | Technology |
|:---|:---|:---|
| [`docs`](https://github.com/Javafest2025/docs) | 📚 Complete project documentation | Markdown, LaTeX |
| [`frontend`](https://github.com/Javafest2025/frontend) | 🎨 Next.js user interface | TypeScript, Tailwind |
| [`api_gateway`](https://github.com/Javafest2025/api_gateway) | 🚪 Spring Cloud Gateway | Java, Spring Boot |
| [`user_service`](https://github.com/Javafest2025/user_service) | 👤 Authentication & user management | Java, Spring Security |
| [`project_service`](https://github.com/Javafest2025/project_service) | 📂 Research project management | Java, JPA |
| [`notification_service`](https://github.com/Javafest2025/notification_service) | 🔔 Email & notification system | Java, RabbitMQ |
| [`service_registry`](https://github.com/Javafest2025/service_registry) | 🔍 Eureka service discovery | Java, Spring Cloud |
| [`meta`](https://github.com/Javafest2025/meta) | 🔗 Git submodules orchestration | Shell, Docker |

---

## 🚀 Quick Start

### 📋 Prerequisites

- **Docker** & **Docker Compose** installed
- **Git** with submodule support
- **Java 21** (for local development)
- **Node.js 18+** (for frontend development)

### 🐳 One-Command Startup

```bash
# Clone the meta repository
git clone --recursive https://github.com/Javafest2025/meta.git
cd meta

# Start the entire platform
./Scripts/docker.sh start-all

# 🎉 Access ScholarAI at http://localhost:3000
```

### 🛠️ Development Setup

> **📍 Important**: All the following commands should be executed inside the [`meta`](https://github.com/Javafest2025/meta) repository after cloning it.

```bash
# Clone the meta repository first
git clone --recursive https://github.com/Javafest2025/meta.git
cd meta

# Start everything all at once
./Scripts/docker.sh start-all

# Start infrastructure only (databases, message queues)
./Scripts/docker.sh start infra

# Start specific service
./Scripts/docker.sh start user-service

# View logs for specific service
./Scripts/docker.sh logs frontend

# Stop everything
./Scripts/docker.sh stop-all
```

---

## 🎯 Key Features

### 🔬 Pre-Research Phase
- **📖 Paper Web Search**: Integration with Semantic Scholar, arXiv, CrossRef
- **🔍 Smart PDF Viewer**: Annotation and highlighting capabilities
- **🤖 AI Summarization**: Automated extraction of key insights
- **⭐ Quality Scoring**: AI critic evaluates paper relevance and quality
- **🎯 Gap Analysis**: Identifies unexplored research opportunities
- **💬 Contextual Chat**: Highlight-to-ask AI assistance

### ✍️ Active Research Phase
- **📝 AI-Powered LaTeX Editor**: Live preview with intelligent suggestions
- **📚 Smart Citations**: Auto-complete and format references
- **✅ Writing Review**: AI feedback following academic standards
- **🔗 Template Generation**: Convert topic suggestions to structured outlines

### 📈 Post-Research Phase
- **📊 Impact Dashboard**: Track citations and research metrics
- **📈 Performance Analytics**: Monitor paper downloads and views
- **🔔 Citation Alerts**: Notifications when your work is cited
- **📄 Export Reports**: Generate comprehensive impact summaries

### 🔐 General Platform Features
- **🛡️ Secure Authentication**: JWT + OAuth2 (Google, GitHub)
- **👥 User Profiles**: Customizable researcher profiles
- **🌙 Dark/Light Mode**: Personalized interface themes
- **🔔 Smart Notifications**: Configurable alerts and reminders
- **📱 Responsive Design**: Seamless experience across devices

---

## 📖 API Documentation

### 🔌 Service Endpoints

| Service | Base URL | Documentation |
|:---|:---|:---|
| API Gateway | `http://localhost:8989` | [Gateway Docs](docs/API/api-gateway.md) |
| User Service | `http://localhost:8081` | [User API](docs/API/user-service.md) |
| Project Service | `http://localhost:8083` | [Project API](docs/API/project-service.md) |
| Notification Service | `http://localhost:8082` | [Notification API](docs/API/notification-service.md) |

### 📋 Use Cases

Explore our comprehensive use case documentation:

- [🔐 Authentication & Authorization](docs/Usecase/general-usecases.md)
- [🔍 Pre-Research Workflows](docs/Usecase/pre-research-usecases.md)
- [✍️ Active Research Workflows](docs/Usecase/ongoing-research-usecases.md)
- [📈 Post-Research Analytics](docs/Usecase/post-research-usecases.md)

---

## 🏆 About Javafest 2025

**ScholarAI** is our submission to [**Javafest 2025**](https://www.therapjavafest.com/) - *The Ultimate Battle of Brains & Bytes* organized by **Therap (BD) Ltd.**

### 🏁 Competition Timeline

| Date | Milestone |
|:---|:---|
| **May 31** | Registration Deadline |
| **Jun 3** | Online Screening Test |
| **Jun 11** | Results Announcement |
| **Jun 24** | Group Registration |
| **Jul 7** | Project Proposal Deadline |
| **Sep 20** | **Final Project Deadline** |
| **Oct 7** | **Grand Finale** 🏆 |

---

## 👥 Team ScholarAI

This repository is maintained by the **ScholarAI team** under the `Javafest2025` GitHub organization.

<div align="center">

### 🧑‍💻 Core Developers

| Name | GitHub |
|:---|:---|
| **Tasriad Ahmed Tias** | [@Tasriad](https://github.com/Tasriad) | 
| **Farhad Al-Amin Dipto** | [@Legend-2727](https://github.com/Legend-2727) | 

</div>

---

## 🤝 Contributing

### 🔒 Repository Access

- **✅ Core Team**: Only the two main developers can commit directly
- **👀 Community**: Others are welcome to view, star, and open issues
- **💡 Suggestions**: We appreciate feedback and feature suggestions via issues

### 🛠️ Development Workflow

```bash
# Fork the repository (if external contributor)
# Create feature branch
git checkout -b feature/amazing-feature

# Make changes and test
./scripts/test.sh

# Commit with conventional commits
git commit -m "feat: add amazing new feature"

# Push and create pull request
git push origin feature/amazing-feature
```

---

## 📚 Documentation

| Document | Description |
|:---|:---|
| [🏗️ Architecture Guide](docs/Schema/) | System design and database schemas |
| [🔌 API Reference](docs/API/) | Complete API documentation |
| [🎯 Use Cases](docs/Usecase/) | Detailed user workflows |
| [🐳 Docker Guide](DOCKER_README.md) | Container deployment instructions |
| [📝 Development Log](LEARNING_SUMMARY.md) | Technical learning journey |

---

## 🛡️ License

This project is **proprietary** and developed exclusively for **Javafest 2025**. 

**© 2025 ScholarAI Team - All Rights Reserved**

---

## 📊 Project Activity & Development Metrics

### 🔥 Active Development Status

<div align="center">

![GitHub commit activity](https://img.shields.io/github/commit-activity/m/Javafest2025/meta?style=for-the-badge&logo=github&label=Meta%20Commits)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/Javafest2025/frontend?style=for-the-badge&logo=react&label=Frontend%20Commits)
![GitHub commit activity](https://img.shields.io/github/commit-activity/m/Javafest2025/user_service?style=for-the-badge&logo=spring&label=Backend%20Commits)

![GitHub repo size](https://img.shields.io/github/repo-size/Javafest2025/meta?style=flat&logo=github&label=Total%20Codebase)
![GitHub language count](https://img.shields.io/github/languages/count/Javafest2025/frontend?style=flat&logo=code&label=Languages)
![GitHub top language](https://img.shields.io/github/languages/top/Javafest2025/user_service?style=flat&logo=java&label=Primary%20Language)

</div>

### 🏗️ Repository Activity Overview

| Repository | Purpose | Status | Latest Activity |
|:---|:---|:---:|:---|
| [`meta`](https://github.com/Javafest2025/meta) | 🔗 Main orchestration | ![Status](https://img.shields.io/github/last-commit/Javafest2025/meta?style=flat&logo=github) | Active development |
| [`frontend`](https://github.com/Javafest2025/frontend) | 🎨 User interface | ![Status](https://img.shields.io/github/last-commit/Javafest2025/frontend?style=flat&logo=react) | UI/UX implementation |
| [`user_service`](https://github.com/Javafest2025/user_service) | 👤 Authentication | ![Status](https://img.shields.io/github/last-commit/Javafest2025/user_service?style=flat&logo=spring) | Auth system complete |
| [`project_service`](https://github.com/Javafest2025/project_service) | 📂 Project management | ![Status](https://img.shields.io/github/last-commit/Javafest2025/project_service?style=flat&logo=spring) | Core features ready |
| [`api_gateway`](https://github.com/Javafest2025/api_gateway) | 🚪 API routing | ![Status](https://img.shields.io/github/last-commit/Javafest2025/api_gateway?style=flat&logo=spring) | Gateway configured |
| [`notification_service`](https://github.com/Javafest2025/notification_service) | 🔔 Notifications | ![Status](https://img.shields.io/github/last-commit/Javafest2025/notification_service?style=flat&logo=spring) | Email system active |
| [`service_registry`](https://github.com/Javafest2025/service_registry) | 🔍 Service discovery | ![Status](https://img.shields.io/github/last-commit/Javafest2025/service_registry?style=flat&logo=spring) | Registry operational |
| [`docs`](https://github.com/Javafest2025/docs) | 📚 Documentation | ![Status](https://img.shields.io/github/last-commit/Javafest2025/docs?style=flat&logo=markdown) | Comprehensive docs |

### 📈 Development Highlights

- **🏗️ Microservices Architecture**: 8 independent repositories with specialized functions
- **🔄 Active Development**: Consistent commits across all repositories throughout the competition period
- **📝 Comprehensive Documentation**: Detailed API docs, use cases, and setup guides
- **🐳 Production-Ready**: Fully dockerized with orchestration scripts
- **🧪 Testing Coverage**: Unit tests and E2E testing implemented
- **🎨 Modern Tech Stack**: Latest versions of Spring Boot 3.5.0, Next.js 14+, Java 21

### 🚀 Recent Milestones

- ✅ **Complete Microservices Setup**: All 6 backend services operational
- ✅ **Frontend Integration**: Modern React-based UI with TypeScript
- ✅ **Docker Orchestration**: One-command deployment system
- ✅ **Authentication System**: JWT + OAuth2 social login implementation
- ✅ **API Gateway Configuration**: Centralized routing and load balancing
- ✅ **Documentation Complete**: Full technical documentation and use cases
- 🔄 **AI Integration**: Paper search and LaTeX editor (in progress)
- 🔄 **Advanced Features**: Impact tracking and analytics (in progress)

---

## 🌟 Show Your Support

If you find ScholarAI innovative and useful:

- ⭐ **Star** this repository
- 👀 **Watch** for updates
- 🍴 **Fork** to explore the code
- 💬 **Share** with fellow researchers

---

<div align="center">

### 🎓 *Empowering Researchers, One AI Feature at a Time*

**Built with ❤️ for the academic community**

[Website](https://scholar-ai.vercel.app) • [Documentation](docs/) • [Demo Video](https://youtu.be/demo) • [Javafest 2025](https://www.therapjavafest.com/)

---

![Footer](https://img.shields.io/badge/Made%20for-Javafest%202025-blue?style=for-the-badge&logo=java&logoColor=white)

</div>
