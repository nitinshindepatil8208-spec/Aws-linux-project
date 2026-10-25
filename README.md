
# AWS Linux Server Deployment and Monitoring

## 1. Project Overview
This project demonstrates deploying an Apache web server on an AWS EC2 Ubuntu Linux instance and configuring Prometheus and Grafana for monitoring.

## 2. Technologies Used
- AWS EC2
- Ubuntu Linux
- Apache Web Server
- Prometheus
- Grafana
- Git and GitHub
- Bash Scripting

## 3. Project Objectives
- Create and manage an AWS EC2 instance.
- Install and configure Apache.
- Execute basic Linux commands.
- Configure Prometheus as a Grafana data source.
- Learn server monitoring and troubleshooting.
- Maintain project documentation on GitHub.

## 4. Architecture
AWS EC2 Ubuntu Linux
       |
       v
Apache Web Server
       |
       v
Prometheus Monitoring
       |
       v
Grafana Dashboard

Note: Prometheus requires appropriate scrape configuration
and exporters to collect server metrics.

## 5. Apache Installation

Update Ubuntu packages:

```bash
sudo apt update
```

Install Apache:

```bash
sudo apt install apache2 -y
```

Start and enable Apache:

```bash
sudo systemctl enable --now apache2
```

Check Apache status:

```bash
sudo systemctl status apache2
```

Test the web server:

```bash
curl -I http://localhost
```

## 6. Linux Commands

| Command | Purpose |
|---|---|
| pwd | Show current directory |
| ls -la | List files and directories |
| whoami | Display current user |
| df -h | Check disk usage |
| free -h | Check memory usage |
| uptime | Show system uptime |
| systemctl | Manage services |
| curl | Test HTTP responses |
| chmod | Change file permissions |
| git status | Check Git changes |

## 7. Prometheus Configuration
- Open the Prometheus web interface.
- Configure Prometheus as a Grafana data source.
- Enter the Prometheus server URL.
- Click Save & test.
- Verify that the connection succeeds.

## 8. Grafana Monitoring
- Access the Grafana web interface.
- Add the Prometheus data source.
- Create a dashboard to visualize available metrics.
- Verify the metrics and dashboard queries.

## 9. Project Verification

Check Apache:

```bash
sudo systemctl is-active apache2
```

Test Apache locally:

```bash
curl http://localhost
```

Check Git status:

```bash
git status
```

## 10. Screenshots
Project screenshots are stored in the screenshots folder.

## 11. Learning Outcomes
- AWS EC2 server administration
- Ubuntu Linux commands
- Apache installation and deployment
- Prometheus data source configuration
- Grafana dashboard basics
- Git version control and GitHub

## 12. Author
Nitin Shinde
