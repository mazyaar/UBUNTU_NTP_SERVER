
# NTP Server Ubuntu:


### Step 1: Update Your System
```bash
sudo apt-get update 
sudo apt-get upgrade 
```

### Step 2: Install NTP
```bash
sudo apt-get install ntp 
```

### Step 3: Configure NTP Server
```bash
sudo nano /etc/ntp.conf 
```

***add ntp server to configurations file:***

```
server 0.ubuntu.pool.ntp.org iburst
server 1.ubuntu.pool.ntp.org iburst
server 2.ubuntu.pool.ntp.org iburst
server 3.ubuntu.pool.ntp.org iburst
```

### Step 4: Allow NTP Through the Firewall
```bash
sudo ufw allow 123/udp 
sudo systemctl restart ntp 
```

### Step 5: Restart NTP Service
```bash
sudo systemctl restart ntp 
```

### Step 6: Verify NTP is Working
```bash
sudo systemctl status ntp 
```

To check the synchronization status, use:

```bash
ntpq -p 
```
