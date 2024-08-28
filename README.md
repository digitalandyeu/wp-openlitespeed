# Server Setup

Manual: https://docs.litespeedtech.com/cloud/images/wordpress/

## Install Script

https://docs.openlitespeed.org/installation/script/

```bash
bash <( curl -k https://raw.githubusercontent.com/litespeedtech/ols1clk/master/ols1clk.sh ) -w
## DEV ONLY
curl -k https://raw.githubusercontent.com/andriilive/ols1clk-wp-version/master/ols1clk.sh
```

```shell
wget -O ~/ols1clk.sh https://raw.githubusercontent.com/andriilive/ols1clk-wp-version/master/ols1clk.sh
sudo mv ~/ols1clk.sh /usr/bin/ols1clk && chmod +x /usr/bin/ols1clk && sudo chown root:root /usr/bin/ols1clk
ols1clk -A ZGQyNmE0 -E admin@domain.eu -R "" -W --wordpressplus "domain.eu" --dbname "prod" --dbuser "wp" --dbpassword "" --mariadbver 10.11 --pure-mariadb --with-mysql
```
