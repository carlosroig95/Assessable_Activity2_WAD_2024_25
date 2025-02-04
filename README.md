# Assessable_Activity2_WAD_2024_25

1. **Configure a group of specific rules to allow the following ports to connect**
	1.1 Puerto 80 para el acceso http.
	1.2 Puerto 22 para el acceso SSH. Con mi IP como unico origen
	1.3 Puerto 5173 para servicio VITEPuerto 80 para el acceso http.
2. **Created an EC2 instance** using Ubuntu 22.04.
	2.1 I create the key pair
	2.2 I associate the previously created security group
3. **Assigned an Elastic IP** to ensure a stable public IP address.
4. **Connected via SSH with PUTTY** to the instance.
	4.1 I change the key pair generated from pem to ppk with the PuTTY Key Generator application
5. **Installed necessary packages**:
   - Apache (`sudo apt install apache2 -y`)
   - Node.js and npm (`curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash - && sudo apt install -y nodejs`)
   - PM2 (`sudo npm install -g pm2`)
   - Apache proxy modules (`sudo a2enmod proxy proxy_http`)
6. **Cloned the React project from GitHub** and installed dependencies (`npm install`).
7. **Configured Apache as a reverse proxy** to forward requests from port 80 to port 5173.
8. **Deployed the application** using PM2 (`pm2 start npm --name "vite-server" -- run dev -- --host`).
9. **Set up PM2 to restart on reboot** (`pm2 startup && pm2 save`).
