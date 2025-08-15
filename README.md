# Netdata Monitoring Task

## Objective
Install Netdata and visualize system and application performance metrics using Docker.

## Tools Used
- **Netdata** (Free, open-source monitoring tool)
- **Docker**

## Steps Followed

### 1. Install and Run Netdata with Docker
```bash
docker run -d --name=netdata   -p 19999:19999   --cap-add SYS_PTRACE   --security-opt apparmor=unconfined   netdata/netdata
```

### 2. Access the Dashboard
Open your browser and go to:
```
http://localhost:19999
```
You will see a live dashboard displaying CPU, Memory, Disk, Network, and Docker container metrics.

### 3. Explore Metrics
- **CPU Tab** → Load averages & usage per core
- **Memory Tab** → Used, cached, and free memory
- **Disks Tab** → Read/write throughput
- **Network Tab** → Incoming/outgoing packets
- **Docker Tab** → Stats of running containers

### 4. Explore Alerts
Netdata has built-in alert thresholds. Alerts appear in **red** or **yellow** when triggered.

### 5. Check Logs
Inside the container:
```bash
docker exec -it netdata /bin/bash
cd /var/log/netdata
ls
```

### 6. GitHub Submission
1. **screenshots** of the dashboard.
<img width="2159" height="1246" alt="image" src="https://github.com/user-attachments/assets/4764ab10-dfe7-485c-b3c3-cc07a0c380ba" />
<img width="2159" height="1245" alt="image" src="https://github.com/user-attachments/assets/e2da4c31-b97f-422d-b3ba-11bf95e37d74" />

2. Push to GitHub:
```bash
git init
git add .
git commit -m "Netdata monitoring task"
git branch -M main
git remote add origin https://github.com/Manthan-Sinojiya/Netdata-Monitoring-Task.git
git push -u origin main
```

## Outcome
- Learned lightweight monitoring for servers or apps.
- Able to visualize system performance metrics in real time.

---
**Author:** Manthan Sinojiya
