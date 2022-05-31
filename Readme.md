# Build container

`docker build -t httpd-proxyenabled .`

# Run container

`docker container run --publish 90:80 -d --name apacheserver -v <Full Path To Folder>/docker/apacheconf/sites:/usr/local/apache2/conf/sites -v <Full Path To Folder>/docker/apacheconf/htmlfiles:/usr/local/apache2/techolaf httpd-proxyenabled`

# Stop and remove container

`docker stop apacheserver && docker rm apacheserver`

# Configuration

We need to update `docker/apacheconf/sites/website.conf` file with the following content:

`<Destination Domain>` should be the destination domain
