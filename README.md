# Server Setup

Manual: https://docs.litespeedtech.com/cloud/images/wordpress/

## Install Script

https://docs.openlitespeed.org/installation/script/

```bash
bash <( curl -k https://raw.githubusercontent.com/litespeedtech/ols1clk/master/ols1clk.sh ) -w
# OR
curl -k https://raw.githubusercontent.com/andriilive/ols1clk-wp-version/master/ols1clk.sh
```

```shell
./ols1clk.sh --wordpressplus site.eu --mariadbver 10.5 --lsphp 80 --wplang cs_CZ -e admin@site.eu --sitetitle "site.eu" --prefix wp --wpuser admin.digitalandyeu --wppassword $WP_PASSWORD --wpversion 5.8
--dbname "prod_wordpress" --dbuser --dbpassword
```

### OLS Configuration

```shell
ufw allow 7080
cat .db_password && cat .litespeed_password

groupadd wordpress
usermod -aG wordpress www-data
usermod -aG wordpress sftpuser
chown -R www-data:wordpress /var/www/html
```

### IF PUBLIC KEYS

```shell
cat ~/.ssh/authorized_keys
cp .ssh && /home/sftpuser
cat ~/.ssh/authorized_keys > /home/sftpuser/.ssh/authorized_keys

# AS SFTPUSER
su sftpuser
chmod go-w /home/$USER
chown sftpuser:sftpuser /home/$USER/.ssh
chown sftpuser:sftpuser /home/$USER/.ssh/authorized_keys
chmod 700 /home/$USER/.ssh
chmod 644 /home/$USER/.ssh/authorized_keys
```

![CleanShot 2024-08-27 at 12 56 46](https://github.com/user-attachments/assets/2aa2302d-6f82-4292-80d8-ad1f0829cbe3)

## WP DUMP

```shell
cd /var/www/html/
wp db export .db.sql

```
