**1️⃣ System Information**

| Purpose        | Command               | Example               |
| -------------- | --------------------- | --------------------- |
| System info    | `uname -a`            | OS, kernel version    |
| CPU info       | `lscpu`               | CPU details           |
| Memory         | `free -h`             | RAM usage             |
| Disk usage     | `df -h`               | Disk space            |
| Block devices  | `lsblk`               | Show disks/partitions |
| PCI devices    | `lspci`               | Hardware info         |
| USB devices    | `lsusb`               | USB info              |
| Distro version | `cat /etc/os-release` | OS name & version     |

**2️⃣ Process Management**

| Purpose             | Command          |
| ------------------- | ---------------- |
| List processes      | `ps -ef`         |
| Interactive monitor | `top`, `htop`    |
| Kill process        | `kill <pid>`     |
| Force kill          | `kill -9 <pid>`  |
| Graceful stop       | `kill -15 <pid>` |
| Process tree        | `pstree`         |

**3️⃣ File & Directory Commands**

```bash
ls
ls -l
ls -lah
pwd
cd /path
touch file.txt
mkdir newdir
rm file
rm -rf dir
cp source dest
mv old new
cat file
more file
less file
head file
tail file
tail -f log.txt

```

**4️⃣ Search Commands (Very Important for DevOps)**

```bash
grep "error" file.log
grep -i "fail" file.log
grep -r "timeout" /var/log
find / -name "*.log"
find /var -type f -size +100M
```

**5️⃣ User & Permission Commands**

```bash
useradd devops
passwd devops
id devops
whoami
who
last
 ---
chmod 755 file
chmod u+x script.sh
chown user:group file
chgrp group file
```

**6️⃣ Networking Commands**

```bash
#Interfaces:
ip a
ifconfig (older)

#Routing:
ip route

#Connectivity:
ping google.com
traceroute google.com
curl -I http://site.com
wget file.url

#Open Ports:
ss -tulnp
netstat -tulnp  (older)

#DNS lookup:
nslookup amazon.com
dig google.com
```

**7️⃣ Disk, Storage & LVM**

```bash
#Disk usage:
df -h
du -sh *

#Block devices:
lsblk
blkid

#Mounting:
mount /dev/sdb1 /mnt
umount /mnt

#LVM Commands:
pvcreate /dev/sdb
vgcreate vg_data /dev/sdb
lvcreate -L 10G -n lv_app vg_data
mkfs.ext4 /dev/vg_data/lv_app
mount /dev/vg_data/lv_app /app
```

**8️⃣ Package Management**

```bash
CentOS/RHEL:
yum install nginx
yum update
rpm -qa

Ubuntu/Debian:
apt update
apt install nginx
dpkg -l
```

**9️⃣ Systemctl & Service Commands**

```bash
systemctl status nginx
systemctl start nginx
systemctl stop nginx
systemctl restart nginx
systemctl enable nginx
systemctl disable nginx
systemctl list-units --type=service
```

**🔟 Archiving & Compression**

```bash
tar -cvf files.tar *.log
tar -xvf files.tar

gzip file
gunzip file.gz
```

**1️⃣1️⃣ Shell Scripting Essentials**

```bash
#!/bin/bash

for i in {1..5}; do
  echo "Hello $i"
done
```

Run script below Commands:
chmod +x script.sh

./script.sh

**1️⃣2️⃣ Logs & Debugging**

```bash
journalctl -u nginx
journalctl -xe
dmesg
tail -f /var/log/messages
tail -f /var/log/syslog
```

