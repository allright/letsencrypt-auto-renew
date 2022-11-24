1. Copy contents of this repository into /opt/letsencrypt_auto_renew/ directory on your server
2. You are free to change directory name, but also you have to change ./etc/crontab, cron_job.sh for abother name of project directory
3. Add to DNS records your server IP
4. Run ./install.sh your.domain email@your.domain  (also use your domain names)
  - certificates will be issued first time
  - cron job will be scheduled for automatic renew
5. Use your server, using docker-compose up