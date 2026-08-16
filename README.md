# 🌐 Paulo Pedreira — Portfólio Profissional

Website pessoal e portfólio profissional de **Paulo Pedreira**, desenvolvido para apresentar experiência, conhecimentos e projetos na área de **Infraestrutura de TI, Cloud, AWS e DevOps**.

🔗 **Website:** [paulo.pedreira.com.br](https://paulo.pedreira.com.br)

---

## 🚀 Sobre o projeto

Este repositório contém o código-fonte do meu website pessoal, desenvolvido em **HTML e CSS**, com uma abordagem simples, leve e responsiva.

O projeto também é utilizado como laboratório prático para aplicar conceitos de **Cloud Computing, CI/CD, AWS, segurança e automação de infraestrutura**.

O código-fonte fica hospedado no **GitHub** e, a cada atualização, uma pipeline realiza automaticamente o processo de publicação do website na infraestrutura AWS.

---

## 🏗️ Arquitetura

O website utiliza uma arquitetura baseada em **Amazon S3 + Amazon CloudFront**, mantendo o bucket S3 privado.

```text
                    ┌──────────────────────┐
                    │       Usuário        │
                    │      Internet        │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │   CloudFront (CDN)   │
                    │ HTTPS / Distribuição │
                    └──────────┬───────────┘
                               │
                               │ Origin Access
                               │
                               ▼
                    ┌──────────────────────┐
                    │     Amazon S3        │
                    │   Bucket Privado     │
                    │                      │
                    │  index.html          │
                    │  foto-paulo.*        │
                    └──────────────────────┘


        ┌──────────────────────┐
        │       GitHub         │
        │                      │
        │  Código-fonte       │
        │  HTML / CSS / Foto   │
        └──────────┬───────────┘
                   │
                   │ Push / Merge
                   ▼
        ┌──────────────────────┐
        │    CI/CD Pipeline    │
        │                      │
        │  Build / Deploy      │
        └──────────┬───────────┘
                   │
                   │ Deploy
                   ▼
        ┌──────────────────────┐
        │       Amazon S3      │
        └──────────────────────┘
```

### 🔐 Segurança

O bucket utilizado para armazenar os arquivos do website **não é público**.

O acesso aos objetos é realizado através do **Amazon CloudFront**, permitindo manter o armazenamento protegido enquanto o conteúdo é distribuído pela CDN.

---

## 🔄 Processo de Deploy

O fluxo de publicação foi estruturado seguindo o conceito de **CI/CD**:

```text
Alteração no código
        │
        ▼
     Git Push
        │
        ▼
 GitHub Repository
        │
        ▼
   CI/CD Pipeline
        │
        ▼
 Deploy para S3
        │
        ▼
   CloudFront
        │
        ▼
paulo.pedreira.com.br
```

Dessa forma, uma alteração no website não exige publicação manual no servidor.

O processo de atualização é automatizado através da pipeline configurada no repositório.

---

## ☁️ Tecnologias utilizadas

### Front-end

* HTML5
* CSS3
* Responsive Design

### Cloud / AWS

* Amazon S3
* Amazon CloudFront
* HTTPS
* CDN
* Bucket privado

### DevOps

* Git
* GitHub
* CI/CD
* Pipeline automatizada
* Deploy automatizado

---

## 📁 Estrutura do projeto

```text
.
├── index.html
├── foto-paulo.png
└── README.md
```

O projeto foi mantido propositalmente simples no front-end, utilizando HTML e CSS, enquanto a infraestrutura de publicação demonstra conceitos de Cloud e DevOps.

---

## 🎯 Objetivos do projeto

Além de funcionar como meu website profissional, este projeto tem como objetivo demonstrar na prática conhecimentos relacionados a:

* ☁️ Cloud Computing
* 🔐 Segurança de infraestrutura
* 🚀 CI/CD
* 📦 Deploy automatizado
* 🌐 CDN
* 🗄️ Object Storage
* 🏗️ Arquitetura Cloud
* 🔧 Infraestrutura como plataforma para aplicações web
* 📈 Boas práticas de operação e sustentação

---

## 👨‍💻 Sobre mim

Sou **Analista de Infraestrutura** com experiência em ambientes corporativos, atuando com:

* AWS
* Linux
* Windows Server
* VMware
* Docker
* Docker Swarm
* Redes
* Firewalls
* Veeam
* Zabbix
* Grafana
* Graylog
* GitLab / CI/CD
* Virtualização
* Cloud

Atualmente atuo também na modernização de infraestrutura, migração de workloads para Cloud e implementação de práticas relacionadas a DevOps.

---

## 📫 Contato

**Paulo Pedreira**

📧 [paulo.pedreira@outlook.com.br](mailto:paulo.pedreira@outlook.com.br)

💼 [LinkedIn](https://linkedin.com/in/paulopedreira)

🌐 [paulo.pedreira.com.br](https://paulo.pedreira.com.br)

---

<p align="center">
  <strong>Infraestrutura • Cloud • AWS • DevOps</strong>
</p>

<p align="center">
  Desenvolvido e hospedado utilizando serviços AWS.
</p>
