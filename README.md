# 🐧 Linux for DevSecOps

![Linux](https://img.shields.io/badge/Linux-DevOps%20Foundation-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Bash](https://img.shields.io/badge/Bash-Scripting-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white)
![DevOps](https://img.shields.io/badge/DevOps-Linux%20Skills-2496ED?style=for-the-badge)
![DevSecOps](https://img.shields.io/badge/DevSecOps-Security-critical?style=for-the-badge)

> **Goal:** Build the Linux skills required for DevOps, DevSecOps,
> Cloud, SRE, CI/CD, Docker and Kubernetes.
>
> This README is designed as a **study guide + hands-on lab manual +
> interview preparation guide + ATS-friendly resume skill reference**.

------------------------------------------------------------------------

## 🗺️ Linux DevOps Learning Flow

``` text
Linux Fundamentals
       ↓
Filesystem & Navigation
       ↓
Users / Groups / Permissions
       ↓
Processes / Services / Packages
       ↓
Networking / SSH / Firewall
       ↓
Logs / Storage / CPU / Memory
       ↓
Bash → Shell Scripting → Cron
       ↓
grep / sed / awk / pipes
       ↓
Linux Security
       ↓
Docker → Kubernetes → Jenkins
       ↓
Prometheus / Grafana
       ↓
Troubleshooting + Real-World Projects
```

------------------------------------------------------------------------

# 📚 Complete Topic Index

  \#      Topic                          DevOps Importance
  ------- ------------------------------ -------------------
  🖥️ 01   Linux Fundamentals             ⭐⭐⭐⭐⭐
  📂 02   Filesystem Hierarchy           ⭐⭐⭐⭐⭐
  🧭 03   Navigation & File Management   ⭐⭐⭐⭐⭐
  👤 04   Users & Groups                 ⭐⭐⭐⭐⭐
  🔐 05   Permissions & Ownership        ⭐⭐⭐⭐⭐
  ⚙️ 06   Processes & Jobs               ⭐⭐⭐⭐⭐
  🔧 07   systemd & Services             ⭐⭐⭐⭐⭐
  📦 08   Package Management             ⭐⭐⭐⭐
  🌐 09   Linux Networking               ⭐⭐⭐⭐⭐
  🔑 10   SSH                            ⭐⭐⭐⭐⭐
  🧱 11   Firewall                       ⭐⭐⭐⭐⭐
  📝 12   Logs & Troubleshooting         ⭐⭐⭐⭐⭐
  💾 13   Disk & Storage                 ⭐⭐⭐⭐⭐
  🧠 14   CPU & Memory                   ⭐⭐⭐⭐⭐
  🐚 15   Bash Shell                     ⭐⭐⭐⭐⭐
  📜 16   Shell Scripting                ⭐⭐⭐⭐⭐
  ⏰ 17   Cron & Scheduling              ⭐⭐⭐⭐
  🔎 18   grep, sed & awk                ⭐⭐⭐⭐⭐
  🔗 19   Pipes & Redirection            ⭐⭐⭐⭐⭐
  🛡️ 20   Linux Security                 ⭐⭐⭐⭐⭐
  🐳 21   Linux + Docker                 ⭐⭐⭐⭐⭐
  ☸️ 22   Linux + Kubernetes             ⭐⭐⭐⭐⭐
  🔄 23   Linux + Jenkins                ⭐⭐⭐⭐⭐
  📊 24   Linux Monitoring               ⭐⭐⭐⭐⭐
  🚨 25   Linux Troubleshooting          ⭐⭐⭐⭐⭐
  🧪 26   Hands-on Labs                  ⭐⭐⭐⭐⭐
  🎯 27   Interview Preparation          ⭐⭐⭐⭐⭐

------------------------------------------------------------------------

# 🖥️ 01. Linux Fundamentals

![Fundamentals](https://img.shields.io/badge/01-Linux%20Fundamentals-blue?style=for-the-badge&logo=linux&logoColor=white)

## What is Linux?

Linux is an open-source operating-system kernel. Linux distributions
combine the kernel with utilities, libraries, package managers and other
software.

Common distributions:

-   Ubuntu
-   Debian
-   Red Hat Enterprise Linux
-   Rocky Linux
-   AlmaLinux
-   Amazon Linux
-   SUSE Linux Enterprise

## Why Linux is important for DevOps

Linux is widely used for:

-   Web servers
-   Application servers
-   Cloud virtual machines
-   Containers
-   Kubernetes nodes
-   CI/CD agents
-   Monitoring systems
-   Databases
-   Automation platforms

## Kernel vs Shell vs OS

``` text
User
  ↓
Shell
  ↓
System Calls
  ↓
Linux Kernel
  ↓
Hardware
```

### Important commands

``` bash
uname -a
hostname
whoami
id
pwd
date
uptime
cat /etc/os-release
```

### Real-world example

A DevOps engineer receives a new cloud VM and needs to identify the OS,
kernel and current user before deploying an application.

``` bash
cat /etc/os-release
uname -r
whoami
hostname
```

### Interview questions

-   What is Linux?
-   What is the Linux kernel?
-   What is a Linux distribution?
-   Difference between kernel and shell?
-   Why is Linux preferred in DevOps?
-   What does `uname -r` show?
-   How do you identify the Linux distribution?

### ATS keywords

`Linux Administration`, `Linux`, `RHEL`, `Ubuntu`,
`Linux Troubleshooting`, `Linux Server Administration`

------------------------------------------------------------------------

# 📂 02. Linux Filesystem Hierarchy

![Filesystem](https://img.shields.io/badge/02-Filesystem%20Hierarchy-purple?style=for-the-badge&logo=linux&logoColor=white)

Linux uses a hierarchical filesystem beginning at `/`.

  Directory    Purpose
  ------------ --------------------------------
  `/`          Root filesystem
  `/etc`       Configuration files
  `/var`       Variable data and logs
  `/var/log`   System/application logs
  `/home`      User home directories
  `/root`      Root user's home
  `/tmp`       Temporary files
  `/opt`       Optional application software
  `/usr`       User applications/utilities
  `/bin`       Essential commands
  `/sbin`      System administration commands
  `/boot`      Boot-related files
  `/dev`       Device files
  `/proc`      Process/kernel information
  `/sys`       Kernel/device information
  `/run`       Runtime state
  `/mnt`       Temporary mount point
  `/media`     Removable media

### Real-world example

An application is failing because the server filesystem is full.

Start with:

``` bash
df -h
du -sh /var/*
du -sh /var/log/*
```

You discover `/var/log` is consuming excessive disk space.

### Interview questions

-   What is `/etc`?
-   What is `/var`?
-   Difference between `/home` and `/root`?
-   What is `/proc`?
-   What is `/sys`?
-   Where are Linux logs normally stored?
-   Where would you place custom application software?

------------------------------------------------------------------------

# 🧭 03. Navigation & File Management

![Navigation](https://img.shields.io/badge/03-Navigation%20%26%20Files-orange?style=for-the-badge&logo=linux&logoColor=white)

## Essential commands

``` bash
pwd
ls
ls -la
cd
tree
touch
mkdir
mkdir -p
cp
mv
rm
rm -rf
file
stat
```

## Finding files

``` bash
find /var/log -type f
find /opt -name "*.log"
find /tmp -type f -mtime +7
```

## Real-world example

Find all files larger than 500 MB:

``` bash
find / -type f -size +500M 2>/dev/null
```

### Safe operational practice

Never run:

``` bash
rm -rf /*
```

Understand the path before destructive commands.

### ATS keywords

`Linux File Management`, `find`, `filesystem troubleshooting`,
`shell commands`

------------------------------------------------------------------------

# 👤 04. Users & Groups

![Users](https://img.shields.io/badge/04-Users%20%26%20Groups-green?style=for-the-badge&logo=linux&logoColor=white)

## Important files

``` text
/etc/passwd
/etc/shadow
/etc/group
/etc/sudoers
```

## Commands

``` bash
whoami
id
who
w
last
useradd
usermod
userdel
passwd
groupadd
groupmod
groupdel
groups
su
sudo
```

### Real-world example

A deployment account needs access to Docker without giving full root
access.

Conceptually:

``` bash
sudo usermod -aG docker deployuser
```

Then verify:

``` bash
id deployuser
```

### Interview topics

-   root user
-   UID/GID
-   `/etc/passwd`
-   `/etc/shadow`
-   primary vs supplementary groups
-   sudo
-   service accounts
-   least privilege

------------------------------------------------------------------------

# 🔐 05. Permissions & Ownership

![Permissions](https://img.shields.io/badge/05-Permissions%20%26%20Ownership-red?style=for-the-badge&logo=linux&logoColor=white)

Linux permissions are based on:

``` text
User | Group | Others
 r w x | r w x | r w x
```

Example:

``` bash
-rwxr-x---
```

Permission values:

``` text
r = 4
w = 2
x = 1
```

Examples:

``` bash
chmod 755 script.sh
chmod 640 app.conf
chown appuser:appgroup app.conf
chgrp appgroup app.conf
```

## Special permissions

Learn:

-   SUID
-   SGID
-   Sticky bit
-   ACL

Commands:

``` bash
getfacl file
setfacl -m u:user:rwx file
```

### Real-world example

An application should read a configuration file, but normal users should
not modify it.

``` bash
chown appuser:appgroup app.conf
chmod 640 app.conf
```

### Security principle

Avoid:

``` bash
chmod 777
```

Use the minimum permissions required.

### ATS keywords

`Linux Permissions`, `chmod`, `chown`, `ACL`, `Linux Security`, `RBAC`,
`Least Privilege`

------------------------------------------------------------------------

# ⚙️ 06. Processes & Jobs

![Processes](https://img.shields.io/badge/06-Processes%20%26%20Jobs-yellow?style=for-the-badge&logo=linux&logoColor=black)

## Commands

``` bash
ps aux
ps -ef
top
htop
pgrep
pidof
pstree
kill
pkill
nice
renice
jobs
bg
fg
nohup
```

Process states include:

``` text
R = Running
S = Sleeping
D = Uninterruptible sleep
T = Stopped
Z = Zombie
```

### Real-world example

A Java application is consuming 100% CPU.

``` bash
top
ps -eo pid,ppid,cmd,%cpu,%mem --sort=-%cpu | head
```

Identify the process and investigate logs/application behavior before
terminating it.

### Interview questions

-   What is a process?
-   Process vs thread?
-   What is PID?
-   What is PPID?
-   Zombie process?
-   Difference between `kill` and `pkill`?
-   What does `nohup` do?
-   What is a background process?

------------------------------------------------------------------------

# 🔧 07. systemd & Services

![systemd](https://img.shields.io/badge/07-systemd%20%26%20Services-6f42c1?style=for-the-badge&logo=linux&logoColor=white)

Modern Linux distributions commonly use systemd.

``` bash
systemctl status nginx
systemctl start nginx
systemctl stop nginx
systemctl restart nginx
systemctl reload nginx
systemctl enable nginx
systemctl disable nginx
systemctl is-active nginx
systemctl is-enabled nginx
```

Logs:

``` bash
journalctl -u nginx
journalctl -u nginx -f
```

### Real-world example

A web server fails after reboot because the service was not enabled.

``` bash
systemctl enable nginx
```

### Important concepts

-   Unit
-   Service
-   Target
-   Dependency
-   Startup
-   Restart policy
-   Environment variables
-   Service user

------------------------------------------------------------------------

# 📦 08. Package Management

![Packages](https://img.shields.io/badge/08-Package%20Management-brown?style=for-the-badge&logo=linux&logoColor=white)

## Debian/Ubuntu

``` bash
apt update
apt upgrade
apt install nginx
apt remove nginx
apt search nginx
dpkg -l
```

## RHEL/Rocky/Alma

``` bash
dnf install nginx
dnf update
dnf remove nginx
dnf search nginx
rpm -qa
```

### Real-world example

Install Git on an Ubuntu CI/CD agent:

``` bash
sudo apt update
sudo apt install git
git --version
```

### DevOps relevance

Package management is important for:

-   Server provisioning
-   Configuration management
-   CI agents
-   Application dependencies
-   Security patching

------------------------------------------------------------------------

# 🌐 09. Linux Networking

![Networking](https://img.shields.io/badge/09-Linux%20Networking-0A66C2?style=for-the-badge&logo=linux&logoColor=white)

## Must-know concepts

-   IP address
-   IPv4/IPv6
-   Subnet
-   Gateway
-   DNS
-   TCP/UDP
-   Ports
-   Routing
-   NAT
-   ARP
-   HTTP/HTTPS
-   TLS
-   Network interfaces

## Commands

``` bash
ip addr
ip link
ip route
ip neigh
ss -tulnp
ping
traceroute
tracepath
dig
nslookup
host
curl
wget
nc
```

### Real-world example

An application cannot connect to a database.

Check:

``` bash
ip route
dig db.example.com
nc -vz db.example.com 5432
```

Then determine whether the issue is:

``` text
DNS → Routing → Firewall → Port → Application
```

### Interview questions

-   TCP vs UDP?
-   What is DNS?
-   What is a default gateway?
-   What is a routing table?
-   What does `ss -tulnp` show?
-   How do you test whether port 443 is reachable?
-   How do you troubleshoot DNS?

### ATS keywords

`TCP/IP`, `DNS`, `HTTP/HTTPS`, `Linux Networking`, `Routing`,
`Network Troubleshooting`, `TCP`, `UDP`

------------------------------------------------------------------------

# 🔑 10. SSH

![SSH](https://img.shields.io/badge/10-SSH-black?style=for-the-badge&logo=openssh&logoColor=white)

SSH is essential for secure remote administration.

``` bash
ssh user@server
ssh -p 2222 user@server
scp file.txt user@server:/tmp/
rsync -av ./app/ user@server:/opt/app/
```

## Key authentication

``` bash
ssh-keygen
ssh-copy-id user@server
```

Common files:

``` text
~/.ssh/id_rsa
~/.ssh/id_ed25519
~/.ssh/authorized_keys
~/.ssh/config
```

### Real-world example

A DevOps engineer needs Jenkins to deploy to a Linux server without
interactive passwords. SSH key authentication can be configured with a
dedicated deployment account and least-privilege access.

### Security

Prefer:

-   SSH keys
-   restricted users
-   least privilege
-   controlled source IPs
-   secure key permissions
-   disabling unnecessary password/root login where appropriate

------------------------------------------------------------------------

# 🧱 11. Firewall

![Firewall](https://img.shields.io/badge/11-Firewall-red?style=for-the-badge&logo=linux&logoColor=white)

Understand:

-   Stateful firewall
-   Inbound traffic
-   Outbound traffic
-   Ports
-   Rules
-   Default deny
-   Allow lists

## firewalld examples

``` bash
firewall-cmd --state
firewall-cmd --list-all
firewall-cmd --get-active-zones
```

## UFW examples

``` bash
sudo ufw status
sudo ufw allow 22/tcp
sudo ufw allow 80/tcp
sudo ufw allow 443/tcp
```

### Real-world example

A web server should expose:

``` text
22   SSH   → restricted administration
80   HTTP  → public/redirect
443  HTTPS → public
```

Database ports should generally not be exposed publicly unless
explicitly required and secured.

------------------------------------------------------------------------

# 📝 12. Logs & Troubleshooting

![Logs](https://img.shields.io/badge/12-Logs%20%26%20Troubleshooting-darkgreen?style=for-the-badge&logo=linux&logoColor=white)

Important locations:

``` text
/var/log/
/var/log/messages
/var/log/syslog
/var/log/auth.log
/var/log/secure
```

Commands:

``` bash
journalctl
journalctl -xe
journalctl -f
journalctl -u service
tail -f /var/log/syslog
grep "ERROR" application.log
```

### Real-world example

A service is failing after deployment.

Use:

``` bash
systemctl status myapp
journalctl -u myapp --since "30 minutes ago"
ss -lntp
df -h
free -h
```

Follow the evidence instead of guessing.

### Log investigation workflow

``` text
Symptom
  ↓
Service status
  ↓
Recent logs
  ↓
Process
  ↓
Port
  ↓
Filesystem
  ↓
CPU/Memory
  ↓
Configuration
  ↓
Root cause
```

------------------------------------------------------------------------

# 💾 13. Disk & Storage

![Storage](https://img.shields.io/badge/13-Disk%20%26%20Storage-795548?style=for-the-badge&logo=linux&logoColor=white)

Commands:

``` bash
df -h
df -i
du -sh *
du -xh /var | sort -h
lsblk
blkid
mount
umount
findmnt
```

Learn:

-   partitions
-   filesystems
-   mount points
-   inode
-   LVM
-   RAID concepts
-   swap
-   NFS basics

### LVM concepts

``` text
Physical Volume
      ↓
Volume Group
      ↓
Logical Volume
      ↓
Filesystem
      ↓
Mount Point
```

### Real-world example

A production server has free disk space but cannot create new files.

Check:

``` bash
df -h
df -i
```

The issue may be exhausted inodes rather than storage capacity.

------------------------------------------------------------------------

# 🧠 14. CPU & Memory

![Performance](https://img.shields.io/badge/14-CPU%20%26%20Memory-FF9800?style=for-the-badge&logo=linux&logoColor=white)

Commands:

``` bash
uptime
top
free -h
vmstat
iostat
sar
lscpu
nproc
```

### Load average

Understand:

``` text
1 minute
5 minutes
15 minutes
```

Load must be interpreted relative to CPU count and workload.

### Memory

``` bash
free -h
```

Understand:

-   total
-   used
-   free
-   available
-   buffers/cache
-   swap

### Real-world example

An application becomes slow.

Check:

``` bash
uptime
free -h
vmstat 1 5
top
```

Determine whether the bottleneck is CPU, memory, I/O or the application
itself.

------------------------------------------------------------------------

# 🐚 15. Bash Shell

![Bash](https://img.shields.io/badge/15-Bash%20Shell-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white)

Learn:

-   shell vs terminal
-   environment variables
-   PATH
-   aliases
-   command history
-   quoting
-   command substitution
-   exit codes
-   functions
-   positional parameters

Examples:

``` bash
echo $PATH
echo $HOME
echo $USER
echo $?
history
which python
type cd
```

### Command substitution

``` bash
today=$(date +%F)
echo "$today"
```

### Real-world example

A deployment script needs to locate the application directory from an
environment variable:

``` bash
APP_HOME="/opt/myapp"
echo "$APP_HOME"
```

------------------------------------------------------------------------

# 📜 16. Shell Scripting

![Scripting](https://img.shields.io/badge/16-Shell%20Scripting-2E7D32?style=for-the-badge&logo=gnubash&logoColor=white)

Basic script:

``` bash
#!/bin/bash

set -euo pipefail

APP_NAME="myapp"

echo "Deploying $APP_NAME"
```

Learn:

-   variables
-   conditions
-   loops
-   functions
-   arrays
-   arguments
-   exit status
-   error handling
-   command substitution
-   input/output
-   debugging

## Conditions

``` bash
if [ -f "$FILE" ]; then
    echo "File exists"
else
    echo "File does not exist"
fi
```

## Loops

``` bash
for server in app01 app02 app03; do
    echo "Checking $server"
done
```

## Functions

``` bash
check_service() {
    systemctl is-active --quiet "$1"
}
```

### Real-world DevOps example

Create a script that:

1.  checks disk usage
2.  checks a service
3.  checks an application port
4.  writes results to a log
5.  returns a non-zero exit code when a check fails

### ATS keywords

`Bash`, `Shell Scripting`, `Linux Automation`, `Automation Scripts`,
`Operational Automation`

------------------------------------------------------------------------

# ⏰ 17. Cron & Scheduling

![Cron](https://img.shields.io/badge/17-Cron%20%26%20Scheduling-607D8B?style=for-the-badge&logo=linux&logoColor=white)

Commands:

``` bash
crontab -e
crontab -l
```

Cron format:

``` text
minute hour day month weekday command
```

Example:

``` cron
0 2 * * * /opt/scripts/backup.sh
```

This schedules a daily 2 AM task.

Learn:

-   cron
-   crontab
-   systemd timers
-   environment differences
-   logging scheduled jobs
-   permissions
-   absolute paths

### Real-world example

Schedule a cleanup script to remove application logs older than 30 days.

------------------------------------------------------------------------

# 🔎 18. grep, sed & awk

![Text
Tools](https://img.shields.io/badge/18-grep%20%7C%20sed%20%7C%20awk-795548?style=for-the-badge&logo=linux&logoColor=white)

## grep

``` bash
grep "ERROR" app.log
grep -i "failed" app.log
grep -r "timeout" /var/log
grep -n "ERROR" app.log
```

## sed

``` bash
sed 's/old/new/g' file.txt
sed -n '1,20p' file.txt
```

## awk

``` bash
awk '{print $1}' access.log
awk '{print $1,$7}' access.log
```

### Real-world example

Find the most common HTTP response codes in an access log:

``` bash
awk '{print $9}' access.log | sort | uniq -c | sort -nr
```

These tools are heavily used in troubleshooting and automation.

------------------------------------------------------------------------

# 🔗 19. Pipes & Redirection

![Pipes](https://img.shields.io/badge/19-Pipes%20%26%20Redirection-1565C0?style=for-the-badge&logo=linux&logoColor=white)

Operators:

``` text
>    overwrite
>>   append
<    input
|    pipe
2>   stderr
2>&1 stderr → stdout
&>   stdout + stderr
```

Examples:

``` bash
ps aux | grep nginx
cat app.log | grep ERROR
command > output.txt
command >> output.txt
command 2> error.log
```

### Real-world example

Find failed SSH login attempts:

``` bash
grep "Failed password" /var/log/auth.log
```

Then count source IPs using `awk`, `sort`, `uniq`.

------------------------------------------------------------------------

# 🛡️ 20. Linux Security

![Security](https://img.shields.io/badge/20-Linux%20Security-critical?style=for-the-badge&logo=linux&logoColor=white)

DevSecOps requires security throughout Linux administration.

## Core topics

-   Least privilege
-   sudo
-   file permissions
-   SSH hardening
-   firewall
-   patch management
-   service accounts
-   secrets protection
-   audit logs
-   process isolation
-   SELinux/AppArmor
-   secure configuration
-   vulnerability management

## SELinux

Important concepts:

``` bash
getenforce
sestatus
ls -Z
```

Modes:

``` text
Enforcing
Permissive
Disabled
```

## Security checks

``` bash
ss -tulnp
ps aux
last
who
sudo -l
```

### Real-world example

A production Linux server is compromised because an application runs
with excessive privileges.

Improvement:

``` text
root
 ↓
dedicated service account
 ↓
minimum filesystem permissions
 ↓
restricted network access
 ↓
auditing + monitoring
```

### DevSecOps connection

Linux security supports:

``` text
Secure OS
 ↓
Secure CI Agent
 ↓
Secure Container
 ↓
Secure Kubernetes Node
 ↓
Secure Application Platform
```

------------------------------------------------------------------------

# 🐳 21. Linux + Docker

![Docker](https://img.shields.io/badge/21-Linux%20%2B%20Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

Docker containers use Linux kernel capabilities and isolation
mechanisms.

Learn:

-   namespaces
-   cgroups
-   images
-   containers
-   volumes
-   networks
-   container processes
-   container logs
-   container permissions

Commands:

``` bash
docker ps
docker ps -a
docker images
docker logs container
docker exec -it container /bin/bash
docker inspect container
```

### Real-world example

A containerized application works locally but fails in CI.

Investigate:

``` bash
docker logs app
docker inspect app
docker exec -it app sh
```

Then inspect:

-   environment variables
-   mounted volumes
-   network connectivity
-   permissions
-   ports
-   filesystem paths

### DevSecOps topics

-   non-root containers
-   minimal base images
-   image scanning
-   secrets handling
-   read-only filesystems
-   resource limits

------------------------------------------------------------------------

# ☸️ 22. Linux + Kubernetes

![Kubernetes](https://img.shields.io/badge/22-Linux%20%2B%20Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)

Kubernetes nodes commonly run Linux.

Understand:

-   Pods
-   containers
-   nodes
-   kubelet
-   container runtime
-   namespaces
-   services
-   deployments
-   volumes
-   ConfigMaps
-   Secrets
-   RBAC
-   NetworkPolicy

Commands:

``` bash
kubectl get nodes
kubectl get pods -A
kubectl describe pod POD_NAME
kubectl logs POD_NAME
kubectl exec -it POD_NAME -- sh
```

### Real-world example

A pod is in `CrashLoopBackOff`.

Investigate:

``` bash
kubectl get pod
kubectl describe pod app
kubectl logs app --previous
```

Then check:

``` text
Application logs
Environment
Secrets
ConfigMap
Probes
Resources
Filesystem
Network
```

### Linux connection

Inside the node:

``` text
Linux
 ├── kubelet
 ├── container runtime
 ├── networking
 ├── storage
 ├── cgroups
 └── namespaces
```

------------------------------------------------------------------------

# 🔄 23. Linux + Jenkins

![Jenkins](https://img.shields.io/badge/23-Linux%20%2B%20Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white)

Jenkins controllers and agents frequently run on Linux.

Learn how Jenkins uses Linux for:

-   workspace management
-   shell commands
-   Git operations
-   Maven/Gradle
-   Docker
-   artifact handling
-   deployment scripts
-   credentials
-   service management

Example pipeline shell steps:

``` bash
git clone ...
mvn clean test
docker build -t app:1.0 .
docker push ...
kubectl apply -f deployment.yaml
```

### Real-world project flow

``` text
Developer
   ↓
Git
   ↓
Jenkins Linux Agent
   ↓
Build
   ↓
Test
   ↓
Security Scan
   ↓
Docker Image
   ↓
Registry
   ↓
Kubernetes
```

### Troubleshooting

If Jenkins says:

``` text
Permission denied
```

check:

``` bash
whoami
id
ls -la
pwd
df -h
```

------------------------------------------------------------------------

# 📊 24. Linux Monitoring

![Monitoring](https://img.shields.io/badge/24-Linux%20Monitoring-FF6F00?style=for-the-badge&logo=prometheus&logoColor=white)

Monitor:

-   CPU
-   memory
-   disk
-   filesystem/inodes
-   network
-   processes
-   services
-   load
-   application metrics

Useful commands:

``` bash
top
free -h
df -h
iostat
vmstat
ss -s
uptime
systemctl --failed
```

## Prometheus + Grafana

Typical architecture:

``` text
Linux Server
    ↓
Node Exporter
    ↓
Prometheus
    ↓
Grafana
```

Metrics can include:

-   CPU utilization
-   memory utilization
-   disk usage
-   filesystem usage
-   network traffic
-   system load

### Real-world example

Create an alert when filesystem usage exceeds an operational threshold.

------------------------------------------------------------------------

# 🚨 25. Linux Troubleshooting

![Troubleshooting](https://img.shields.io/badge/25-Troubleshooting-red?style=for-the-badge&logo=linux&logoColor=white)

## Golden troubleshooting method

``` text
1. Understand the symptom
        ↓
2. Check recent changes
        ↓
3. Check service/process
        ↓
4. Check logs
        ↓
5. Check network
        ↓
6. Check CPU/memory
        ↓
7. Check disk/filesystem
        ↓
8. Validate configuration
        ↓
9. Fix safely
        ↓
10. Verify
        ↓
11. Document root cause
```

## Problem: Server is slow

``` bash
uptime
top
free -h
vmstat 1 5
iostat
df -h
```

## Problem: Website is unavailable

``` bash
systemctl status nginx
ss -lntp
curl -I http://localhost
curl -I https://server
```

## Problem: DNS failure

``` bash
dig example.com
cat /etc/resolv.conf
getent hosts example.com
```

## Problem: Disk full

``` bash
df -h
df -i
du -xh / | sort -h | tail
```

## Problem: Permission denied

``` bash
ls -la
id
namei -l /path/to/file
getfacl /path/to/file
```

------------------------------------------------------------------------

# 🧪 26. Hands-on Labs

![Labs](https://img.shields.io/badge/26-Hands--On%20Labs-00A86B?style=for-the-badge&logo=linux&logoColor=white)

## Lab 1 --- Linux Server Discovery

Perform:

``` bash
hostname
uname -a
cat /etc/os-release
uptime
free -h
df -h
ip addr
```

Document the server.

------------------------------------------------------------------------

## Lab 2 --- Users & Permissions

Create:

``` text
devops
developer
appuser
```

Create groups and assign permissions.

Demonstrate:

``` text
user → group → file permission
```

------------------------------------------------------------------------

## Lab 3 --- Web Server

Install Nginx.

``` bash
sudo apt update
sudo apt install nginx
systemctl status nginx
curl http://localhost
```

------------------------------------------------------------------------

## Lab 4 --- Secure Web Server

Configure:

``` text
SSH
Firewall
HTTPS concepts
Service account
File permissions
Log monitoring
```

------------------------------------------------------------------------

## Lab 5 --- Log Analysis

Generate a sample access log and answer:

-   How many requests?
-   Which IP made the most requests?
-   Which URLs returned 404?
-   Which requests returned 500?
-   Which HTTP method is most common?

Use:

``` bash
grep
awk
sort
uniq
```

------------------------------------------------------------------------

## Lab 6 --- Disk Investigation

Simulate disk growth.

Use:

``` bash
df -h
du
find
```

Identify the largest directories/files.

------------------------------------------------------------------------

## Lab 7 --- Bash Health Check

Build a script that checks:

``` text
CPU
Memory
Disk
Nginx
Port 80
```

Output:

``` text
PASS / FAIL
```

------------------------------------------------------------------------

## Lab 8 --- Cron Automation

Schedule your health-check script.

Store results in:

``` text
/var/log/health-check.log
```

------------------------------------------------------------------------

## Lab 9 --- SSH Automation

Configure SSH key authentication and execute a remote health check.

------------------------------------------------------------------------

## Lab 10 --- Docker Troubleshooting

Run an Nginx container and troubleshoot:

``` text
Container
Port
Logs
Filesystem
Network
```

------------------------------------------------------------------------

## Lab 11 --- Jenkins Linux Agent

Create a Linux Jenkins agent and execute:

``` bash
uname -a
whoami
df -h
free -h
git --version
docker --version
```

------------------------------------------------------------------------

## Lab 12 --- Kubernetes Troubleshooting

Deploy an application and intentionally create a configuration error.

Troubleshoot using:

``` bash
kubectl get pods
kubectl describe pod
kubectl logs
kubectl exec
```

------------------------------------------------------------------------

# 🏗️ 27. Real-World Linux DevOps Project

![Project](https://img.shields.io/badge/27-Real--World%20DevOps%20Project-8E44AD?style=for-the-badge&logo=linux&logoColor=white)

## Project: Production Linux Application Platform

### Scenario

A company runs a web application on Linux servers and wants to
standardize operations, automate deployments and improve
monitoring/security.

### Architecture

``` text
                    ┌──────────────┐
                    │   Developer  │
                    └──────┬───────┘
                           ↓
                    ┌──────────────┐
                    │     Git      │
                    └──────┬───────┘
                           ↓
                    ┌──────────────┐
                    │   Jenkins    │
                    │ Linux Agent  │
                    └──────┬───────┘
                           ↓
                 ┌─────────────────────┐
                 │ Build / Test / Scan │
                 └──────────┬──────────┘
                            ↓
                    ┌──────────────┐
                    │    Docker    │
                    └──────┬───────┘
                           ↓
                    ┌──────────────┐
                    │   Registry   │
                    └──────┬───────┘
                           ↓
                    ┌──────────────┐
                    │ Kubernetes   │
                    │ Linux Nodes  │
                    └──────┬───────┘
                           ↓
                    ┌──────────────┐
                    │ Application  │
                    └──────┬───────┘
                           ↓
                ┌─────────────────────┐
                │ Prometheus/Grafana  │
                └─────────────────────┘
```

## Responsibilities to demonstrate

### Linux Administration

-   Server provisioning
-   Users/groups
-   SSH
-   Permissions
-   Package installation
-   systemd
-   log analysis
-   disk management
-   performance analysis
-   networking

### Automation

-   Bash scripts
-   cron/systemd timers
-   health checks
-   deployment scripts
-   log cleanup

### DevOps

-   Git
-   Jenkins
-   Docker
-   Kubernetes
-   monitoring

### DevSecOps

-   least privilege
-   SSH hardening
-   firewall
-   secret protection
-   vulnerability scanning
-   secure container practices

------------------------------------------------------------------------

# 📄 ATS-Friendly Resume Content

Do not copy every command into a resume. Convert the skills into
**impact-oriented statements**.

## Linux DevOps Resume Skills

``` text
Linux Administration | Ubuntu | RHEL | Bash | Shell Scripting |
Linux Networking | TCP/IP | DNS | SSH | systemd | Firewall |
File Permissions | User & Group Management | Log Analysis |
Performance Troubleshooting | Disk & Storage Management |
Docker | Kubernetes | Jenkins | Prometheus | Grafana
```

## Example ATS Bullet Points

-   Administered Linux servers supporting application, CI/CD and
    monitoring workloads, including user management, permissions,
    package management, systemd services and filesystem operations.
-   Automated Linux operational tasks using Bash scripting, reducing
    repetitive manual administration and improving deployment
    consistency.
-   Troubleshot production Linux issues involving CPU, memory, disk,
    networking, processes, services and application logs.
-   Implemented secure Linux access using SSH keys, sudo,
    least-privilege permissions and firewall controls.
-   Analyzed Linux system and application logs using `journalctl`,
    `grep`, `awk`, `sed`, `tail` and standard troubleshooting utilities.
-   Supported Docker workloads on Linux, including container networking,
    volumes, permissions, logs and resource troubleshooting.
-   Supported Kubernetes workloads by troubleshooting Linux nodes,
    containers, networking, storage, processes and application logs.
-   Integrated Linux-based Jenkins agents into CI/CD pipelines for
    automated build, test, packaging and deployment workflows.
-   Implemented Linux monitoring using Prometheus and Grafana for CPU,
    memory, disk, filesystem and system health metrics.
-   Developed Bash health-check and operational automation scripts for
    Linux infrastructure.

------------------------------------------------------------------------

# 🎯 100 Linux DevOps Interview Questions

![Interview](https://img.shields.io/badge/Interview-100%20Questions-DC3545?style=for-the-badge&logo=linux&logoColor=white)

## Linux Fundamentals --- 1--10

1.  What is Linux?
2.  What is the Linux kernel?
3.  What is a Linux distribution?
4.  Linux vs Unix?
5.  What is the shell?
6.  Bash vs shell?
7.  What is a system call?
8.  What does `uname -r` show?
9.  How do you identify the Linux distribution?
10. Why is Linux widely used in DevOps?

## Filesystem --- 11--17

11. What is `/`?
12. What is `/etc`?
13. What is `/var`?
14. What is `/proc`?
15. What is `/sys`?
16. Where are Linux logs stored?
17. Difference between `/home` and `/root`?

## Files & Navigation --- 18--24

18. How do you find a file?
19. Difference between `cp` and `mv`?
20. Difference between `rm` and `rmdir`?
21. How do you find files older than 7 days?
22. How do you find large files?
23. What does `stat` show?
24. What is a symbolic link?

## Users & Groups --- 25--31

25. What is UID?
26. What is GID?
27. `/etc/passwd` vs `/etc/shadow`?
28. Primary vs supplementary group?
29. How do you create a user?
30. How do you add a user to a group?
31. Why should applications use service accounts?

## Permissions --- 32--39

32. Explain `rwx`.
33. What does 755 mean?
34. What does 644 mean?
35. `chmod` vs `chown`?
36. What is SUID?
37. What is SGID?
38. What is sticky bit?
39. What is ACL?

## Processes --- 40--47

40. What is a process?
41. What is PID?
42. What is PPID?
43. What is a zombie process?
44. How do you find CPU-intensive processes?
45. `kill` vs `pkill`?
46. What is `nohup`?
47. What are foreground/background jobs?

## systemd --- 48--54

48. What is systemd?
49. What is a systemd unit?
50. How do you start a service?
51. How do you enable a service?
52. How do you troubleshoot a failed service?
53. How do you view service logs?
54. What is the difference between `restart` and `reload`?

## Packages --- 55--59

55. `apt` vs `dnf`?
56. What is RPM?
57. What is a package repository?
58. How do you find an installed package?
59. Why is patch management important?

## Networking --- 60--70

60. TCP vs UDP?
61. What is DNS?
62. What is a default gateway?
63. What is a subnet?
64. What is NAT?
65. What is a routing table?
66. What does `ip addr` show?
67. What does `ss -tulnp` show?
68. How do you troubleshoot DNS?
69. How do you test a TCP port?
70. How do you troubleshoot application connectivity?

## SSH & Firewall --- 71--77

71. What is SSH?
72. Password vs key authentication?
73. What is `authorized_keys`?
74. How do you troubleshoot SSH?
75. What is a firewall?
76. What is default deny?
77. Why should unnecessary ports be closed?

## Logs & Troubleshooting --- 78--84

78. How do you view system logs?
79. How do you follow a log in real time?
80. How do you troubleshoot a disk-full issue?
81. How do you troubleshoot high CPU?
82. How do you troubleshoot high memory?
83. How do you troubleshoot a failed service?
84. What is your Linux troubleshooting methodology?

## Storage & Performance --- 85--90

85. `df` vs `du`?
86. What is an inode?
87. What is LVM?
88. What is swap?
89. What does load average mean?
90. How do you investigate I/O problems?

## Bash & Automation --- 91--96

91. What is an environment variable?
92. What is `$PATH`?
93. What is `$?`?
94. What is command substitution?
95. How do you write a Bash health-check script?
96. Cron vs systemd timer?

## DevOps / DevSecOps --- 97--100

97. How is Linux used by Jenkins?
98. How does Docker depend on Linux?
99. How is Linux related to Kubernetes?
100. What Linux security practices would you implement on a production
     server?

------------------------------------------------------------------------

# 🧠 Interview Scenario Practice

## Scenario 1 --- CPU is 100%

Answer structure:

``` text
top
↓
identify process
↓
ps
↓
application logs
↓
recent changes
↓
determine root cause
↓
remediate safely
↓
verify
```

## Scenario 2 --- Disk is 100%

``` bash
df -h
df -i
du -xh /var
find /var -type f -size +500M
```

Explain the difference between block-space exhaustion and inode
exhaustion.

## Scenario 3 --- Application is unreachable

Check:

``` bash
systemctl status app
ss -lntp
curl localhost:PORT
ip route
dig hostname
firewall-cmd --list-all
```

## Scenario 4 --- Jenkins deployment fails

Check:

``` text
Jenkins user
↓
workspace permissions
↓
SSH key
↓
target server connectivity
↓
sudo permissions
↓
application service
↓
logs
```

## Scenario 5 --- Kubernetes pod keeps restarting

Check:

``` bash
kubectl get pod
kubectl describe pod
kubectl logs pod
kubectl logs pod --previous
```

Then investigate:

``` text
Application
Configuration
Secrets
Environment
Probes
Resources
Permissions
Network
```

------------------------------------------------------------------------

# 🛡️ Linux DevSecOps Checklist

-   [ ] Understand Linux architecture
-   [ ] Understand filesystem hierarchy
-   [ ] Manage users and groups
-   [ ] Understand permissions
-   [ ] Use sudo safely
-   [ ] Avoid unnecessary root access
-   [ ] Configure SSH securely
-   [ ] Understand firewall rules
-   [ ] Patch systems regularly
-   [ ] Review logs
-   [ ] Monitor CPU/memory/disk
-   [ ] Protect secrets
-   [ ] Use service accounts
-   [ ] Understand SELinux/AppArmor concepts
-   [ ] Use least privilege
-   [ ] Secure Docker containers
-   [ ] Understand Kubernetes Linux nodes
-   [ ] Secure Jenkins agents
-   [ ] Automate repetitive tasks
-   [ ] Document incidents and root causes

------------------------------------------------------------------------

# 🏆 Phase 1 Completion Checklist

## Fundamentals

-   [ ] Linux architecture
-   [ ] Kernel
-   [ ] Shell
-   [ ] Filesystem
-   [ ] Processes
-   [ ] Services
-   [ ] Packages

## Administration

-   [ ] Users
-   [ ] Groups
-   [ ] Permissions
-   [ ] SSH
-   [ ] Firewall
-   [ ] Storage
-   [ ] Logs

## Networking

-   [ ] IP
-   [ ] Subnet
-   [ ] DNS
-   [ ] Routing
-   [ ] TCP/UDP
-   [ ] Ports
-   [ ] HTTP/HTTPS

## Automation

-   [ ] Bash
-   [ ] Shell scripting
-   [ ] grep
-   [ ] sed
-   [ ] awk
-   [ ] pipes
-   [ ] redirection
-   [ ] cron

## DevOps

-   [ ] Docker
-   [ ] Kubernetes
-   [ ] Jenkins
-   [ ] Monitoring
-   [ ] Troubleshooting

## Security

-   [ ] Least privilege
-   [ ] SSH hardening
-   [ ] Permissions
-   [ ] Firewall
-   [ ] SELinux/AppArmor concepts
-   [ ] Secrets
-   [ ] Patch management
-   [ ] Secure containers

------------------------------------------------------------------------

# 📁 Recommended GitHub Repository Structure

``` text
linux-devops/
│
├── README.md
│
├── 01-linux-fundamentals/
├── 02-filesystem/
├── 03-file-management/
├── 04-users-groups/
├── 05-permissions/
├── 06-processes/
├── 07-systemd/
├── 08-packages/
├── 09-networking/
├── 10-ssh/
├── 11-firewall/
├── 12-logs/
├── 13-storage/
├── 14-performance/
├── 15-bash/
├── 16-shell-scripting/
├── 17-cron/
├── 18-grep-sed-awk/
├── 19-pipes-redirection/
├── 20-linux-security/
├── 21-docker/
├── 22-kubernetes/
├── 23-jenkins/
├── 24-monitoring/
├── 25-troubleshooting/
│
├── labs/
│   ├── linux-health-check.sh
│   ├── disk-check.sh
│   ├── service-check.sh
│   └── log-analysis.sh
│
└── projects/
    └── production-linux-devops-platform/
```

------------------------------------------------------------------------

# 🚀 Recommended Learning Sequence

``` text
Week 1
Linux Fundamentals
Filesystem
Navigation
Files
Users
Groups

Week 2
Permissions
Processes
systemd
Packages
Logs

Week 3
Networking
SSH
Firewall
Storage
CPU
Memory

Week 4
Bash
Shell Scripting
grep
sed
awk
Pipes
Cron

Week 5
Linux Security
Docker
Jenkins
Monitoring

Week 6
Kubernetes
Troubleshooting
Real-world project
Interview preparation
```

------------------------------------------------------------------------

# ⭐ Final Goal

By completing this phase, you should be able to take a Linux server and
independently:

``` text
CONNECT
  ↓
UNDERSTAND
  ↓
CONFIGURE
  ↓
SECURE
  ↓
MONITOR
  ↓
AUTOMATE
  ↓
TROUBLESHOOT
  ↓
DEPLOY
```

The most important principle is:

> **Do not memorize Linux commands. Learn what problem each command
> solves, what evidence it provides, and how it fits into a
> troubleshooting or automation workflow.**

------------------------------------------------------------------------

## 🔗 Phase 1 → Phase 2

After completing Linux, move to:

``` text
Linux
  ↓
Networking
  ↓
Git
  ↓
Bash/Python
  ↓
Jenkins
  ↓
Maven
  ↓
Docker
  ↓
SAST/SCA
  ↓
Terraform
  ↓
AWS
  ↓
Kubernetes
  ↓
DevSecOps
```

**Phase 1 status:** 🟢 Complete Linux foundation → ready for DevOps
networking.
