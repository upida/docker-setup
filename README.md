# Configuration

## Apache2

```bash
# php 7.4
docker build -t apache2-74 -f Dockerfile.php74 .
# php 8.3
docker build -t apache2-83 -f Dockerfile.php83 .
```

```bash
# php 7.4
docker run -d -e TZ=GMT+7 --name apache2-7.4 -v /your/local/path:/var/www/html -v /etc/apache2:/etc/apache2 -p 80:80 apache2-74
# php 8.3
docker run -d -e TZ=GMT+7 --name apache2-8.3 -v /your/local/path:/var/www/html -v /etc/apache2:/etc/apache2 -p 80:80 apache2-83
```

```bash
sudo docker cp {image-id}:/etc/apache2 /etc/apache2
```

open /etc/apache2/apache2.conf

Search for

```
<Directory /var/www/>
	Options Indexes FollowSymLinks
	AllowOverride None
	Require all granted
</Directory>
```

Replace with the following code to allow .htaccess files

```
<Directory /var/www>
	Options Indexes FollowSymLinks
	AllowOverride All
	Require all granted
</Directory>
```

```bash
sudo apachectl restart
```

```bash
brew install shivammathur/php/php@7.4
brew install php@8.3

brew link php@8.3
brew unlink php@8.3
brew link php@7.4
brew unlink php@7.4
```