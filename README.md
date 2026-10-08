# Jenkins Webhook CI/CD Demo

A simple static website demonstrating the integration between **GitHub, Webhooks and Jenkins Pipeline**.

## Project Structure

```text
jenkins-webhook-demo/
│
├── Jenkinsfile
├── index.html
└── README.md
```

## CI/CD Flow

```text
Developer
    |
    | git push
    ↓
GitHub Repository
    |
    | Webhook
    ↓
Jenkins
    |
    ↓
Pipeline
    |
    ├── Checkout
    ├── Build
    ├── Test
    └── Deploy
```

## Technologies Used

* HTML
* CSS
* GitHub
* GitHub Webhook
* Jenkins
* Jenkins Pipeline
* CI/CD

## Jenkins Pipeline

The `Jenkinsfile` contains the CI/CD pipeline with four stages:

1. Checkout
2. Build
3. Test
4. Deploy

## Webhook

The GitHub webhook automatically notifies Jenkins whenever a new push is made to the repository.

### Webhook URL

```text
http://YOUR-JENKINS-IP:8080/github-webhook/
```

## How to Run

Clone the repository:

```bash
git clone https://github.com/YOUR-USERNAME/jenkins-webhook-demo.git
```

Open:

```text
index.html
```

in a web browser.

## Jenkins Configuration

Create a Jenkins **Pipeline** job.

Select:

```text
Definition:
Pipeline script from SCM

SCM:
Git

Repository URL:
https://github.com/YOUR-USERNAME/jenkins-webhook-demo.git

Branch:
*/main

Script Path:
Jenkinsfile
```

Enable:

```text
GitHub hook trigger for GITScm polling
```

## Result

Whenever code is pushed to GitHub:

```text
GitHub Push
     ↓
Webhook
     ↓
Jenkins
     ↓
Pipeline
     ↓
Build → Test → Deploy
```

This demonstrates a basic **Continuous Integration and Continuous Delivery workflow**.
