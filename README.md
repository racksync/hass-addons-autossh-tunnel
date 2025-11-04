# Home Assistant AutoSSH Tunnel

[![Base Image](https://img.shields.io/badge/Base%20Image-3.22-blue)](https://github.com/home-assistant/docker-base)  [![alpine-armhf](https://img.shields.io/badge/armhf-yes-brightgreen)](https://alpinelinux.org/releases/)
[![alpine-armv7](https://img.shields.io/badge/armv7-yes-brightgreen)](https://alpinelinux.org/releases/)
[![alpine-aarch64](https://img.shields.io/badge/aarch64-yes-brightgreen)](https://alpinelinux.org/releases/)
[![alpine-amd64](https://img.shields.io/badge/amd64-yes-brightgreen)](https://alpinelinux.org/releases/)
[![alpine-i386](https://img.shields.io/badge/i386-yes-brightgreen)](https://alpinelinux.org/releases/)
[![autossh-tunnel-release](https://img.shields.io/github/v/release/racksync/hass-addons-autossh-tunnel)](https://github.com/racksync/hass-addons-autossh-tunnel/releases) [![last commit](https://img.shields.io/github/last-commit/racksync/hass-addons-autossh-tunnel)](https://github.com/racksync/hass-addons-autossh-tunnel/commit/)

## 🚨 Legacy Repository Notice

**This is a legacy repository** that automatically syncs changes to the main mono repository:
👉 [https://github.com/racksync/hass-addons-suite/tree/main/autossh](https://github.com/racksync/hass-addons-suite/tree/main/autossh)

### How it works:
- Changes pushed to the `main` branch in this repository are automatically synced to the mono repository
- GitHub Actions handles the deployment and validation
- Use this repository for development and testing
- The mono repository contains the final published version


## How to configure

1. Add repository : https://github.com/racksync/hass-addons-autossh-tunnel into Home Assistant Add-ons Section
2. Install and Setup ```hostname```  ```user``` ```remote_forwarding``` for destination expose
3. Start adddon and copy public key into ```~/.ssh/authorized_keys``` 
4. Restart addon again

5. Enable GatewayPorts in ```sshd_config```

  ```
  GatewayPorts clientspecified
  ```
### Forwarding Explanation

```
127.0.0.1:8123:192.168.0.10:8123
```


| Host & Port          | Explain |
|------------------|------|
| ``127.0.0.1:8123``              | Destination | 
| ``192.168.0.10:8123``              | Origin | 


## Caution

- Beware to use root permit login on production!
- Do not expose to 0.0.0.0 or public address

## Welcome for any issue ticket

### Automation Training

- [Services & Products](http://racksync.com)
- [Automation Course](https://facebook.com/racksync)

### Community

- [Home Automation Thailand](https://www.facebook.com/groups/hathailand)
- [Home Automation Marketplace](https://www.facebook.com/groups/hatmarketplace)
- [Home Automation Thailand Discord](https://discord.gg/Wc5CwnWkp4) 

## About RACKSYNC COMPANY LIMITED

**[🌐 RACKSYNC CO., LTD.](https://racksync.com)** - Innovative Cloud & Infrastructure Solutions

### 🏢 Company Overview
RACKSYNC CO., LTD. is a leading technology company based in Bangkok, Thailand, specializing in innovative cloud and infrastructure solutions. We help our customers create life easier across the entire technology stack with household and business solutions, modernizing life with Information Technology to make everything possible, secure, and trustworthy.

### 🚀 Our Services

#### **Cloud & Infrastructure Services**
- **Cloud Infrastructure Design & Implementation** - AWS, GCP, Azure solutions
- **DevOps Implementation & Consulting** - CI/CD pipelines, automation, and optimization
- **System Integration & Architecture** - Enterprise system design and integration
- **Kubernetes & Container Orchestration** - Modern container management and deployment
- **Infrastructure as Code (IaC)** - Terraform, Ansible, and automation frameworks
- **Site Reliability Engineering (SRE)** - Monitoring, reliability, and performance optimization

#### **Automation Solutions**
- **Home Automation Solutions** - Smart home integration, voice-controlled systems, IoT deployment
- **Industrial Automation** - SCADA systems, PLC programming, industrial IoT implementation
- **Automated Deployment Pipelines** - GitHub Actions, GitLab CI, Jenkins workflows
- **Monitoring & Observability** - Prometheus, Grafana, ELK stack implementations

#### **Training & Consulting**
- **On-the-Job Training** - Hands-on technology training for teams
- **Professional Courses** - Certified technology and automation courses
- **Technology Consulting** - Strategic technology planning and roadmap development

### 🛠️ Technology Stack
- **Cloud Platforms**: AWS, Google Cloud Platform, Microsoft Azure
- **Containerization**: Docker, Kubernetes, Podman
- **Infrastructure**: Terraform, Ansible, Packer
- **CI/CD**: GitHub Actions, GitLab CI, Jenkins
- **Monitoring**: Prometheus, Grafana, ELK Stack, Datadog
- **Home Automation**: Home Assistant, Node-RED, MQTT, Zigbee, Z-Wave
- **Industrial**: SCADA, PLC systems, Industrial IoT protocols

### 🌍 Community & Social Presence
- **GitHub**: [@racksync](https://github.com/racksync) - Open source contributions and projects
- **Discord**: [Home Automation Thailand](https://discord.gg/Wc5CwnWkp4) - Active community participation
- **Facebook**: [@racksync](https://facebook.com/racksync) - Updates and community engagement
- **Twitter**: [@racksync](https://twitter.com/racksync) - Tech insights and updates

### 📞 Contact Information
**RACKSYNC COMPANY LIMITED**
- **📍 Location**: Bangkok, Thailand (Previously Suratthani, Thailand 84100)
- **📧 Email**:
  - General: contact@racksync.com
  - DevOps: devops@racksync.com
  - Careers: people@racksync.com
- **🌐 Website**: [www.racksync.com](https://racksync.com)
- **📱 Phone**: +66 85 880 8885
- **💼 LinkedIn**: [RACKSYNC Company Limited](https://linkedin.com/company/racksync)

### 🤝 We're Hiring!
RACKSYNC is actively looking for talented individuals to join our team. If you're passionate about cloud technologies, automation, and innovative solutions, we'd love to hear from you. Contact us at **people@racksync.com**.

### 🏆 Why Choose RACKSYNC?
- **Expertise**: Deep knowledge in cloud infrastructure and automation
- **Innovation**: Cutting-edge solutions using latest technologies
- **Reliability**: Proven track record with enterprise clients
- **Community**: Active contributors to open source projects
- **Support**: Comprehensive training and ongoing support
- **Quality**: Security-first approach with best practices

---

**Connect with us:**

[![Website](https://img.shields.io/website?down_color=grey&down_message=Offline&style=for-the-badge&up_color=green&up_message=Online&url=https%3A%2F%2Fracksync.com&label=Website)](https://racksync.com)
[![GitHub followers](https://img.shields.io/github/followers/racksync?style=for-the-badge&label=GitHub&logo=github)](https://github.com/racksync)
[![Discord](https://img.shields.io/discord/986181205504438345?style=for-the-badge&logo=discord&label=Discord)](https://discord.gg/Wc5CwnWkp4)
[![Facebook](https://img.shields.io/badge/Facebook-racksync-blue?style=for-the-badge&logo=facebook)](https://facebook.com/racksync)