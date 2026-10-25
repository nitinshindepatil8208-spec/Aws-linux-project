
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
## Install Grafana on Ubuntu

### Step 1: Install Required Packages

```bash
sudo apt-get update
sudo apt-get install -y apt-transport-https wget gnupg
```

### Step 2: Add Grafana GPG Key

```bash
sudo mkdir -p /etc/apt/keyrings
sudo wget -O /etc/apt/keyrings/grafana.asc https://apt.grafana.com/gpg-full.key
sudo chmod 644 /etc/apt/keyrings/grafana.asc
```

### Step 3: Add Grafana Repository

```bash
echo "deb [signed-by=/etc/apt/keyrings/grafana.asc] https://apt.grafana.com stable main" | sudo tee /etc/apt/sources.list.d/grafana.list
```

### Step 4: Install Grafana

```bash
sudo apt-get update
sudo apt-get install -y grafana
```

### Step 5: Start and Enable Grafana

```bash
sudo systemctl enable --now grafana-server
```

### Step 6: Verify Grafana Service

```bash
sudo systemctl status grafana-server
```

Check the installed version:

```bash
grafana-server -v
```

### Step 7: Access Grafana

Open your browser and visit:

```text
http://localhost:3000
```

If Grafana is installed on a remote server, use:

```text
http://YOUR_SERVER_IP:3000
```

### Step 8: Configure Prometheus Data Source

1. Log in to Grafana.
2. Navigate to **Connections → Data sources**.
3. Select **Add data source → Prometheus**.
4. Enter the URL:

   `http://localhost:9090`

5. Click **Save & test**.

#**Steps for  Installing Prometheus on Ubuntu**
(Metrics/logs collector) 
1️⃣ Update system
sudo apt update
sudo apt upgrade -y

2️⃣ Install Prometheus and Node Exporter
sudo apt install prometheus prometheus-node-exporter -y

3️⃣  Start and enable Prometheus services
sudo systemctl enable --now prometheus prometheus-node-exporter
4. Check if Prometheus is running:
systemctl status prometheus

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
