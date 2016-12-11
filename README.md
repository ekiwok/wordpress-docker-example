# wordpress-docker-example

Copy `.env.dist` as `.env`. If you want, change PORT in `.env`.

Run `docker-compose up -d`.

Go to `http://YOUR_IP_OR_DOMAIN[:PORT]/admin/install.php` and finish installation.

# data-* directories

- `data-wordpress` will contain `wp-content`. It might be usefull for example to work on themes.
- `data-mysql`     will conatain files from `/var/lib/mysql`.
- `data-nginx`     will containt nginx logs.

# Hints

- It might be necessary for some plugins to have additional php extensions installed. Add whatever you need in wp/Dockerfile
Install desired extension [as described in official php image](https://hub.docker.com/_/php/).
- To access database on your host you may add `ports` configuration to `mysql` service.
Yet it might be good idea to do backup using some wp plugin.
- It might be a good idea to edit `nginx/nginx.conf`, turn on gzip, etc.

# Disclaimer

This uses official [wordpress docker image](https://hub.docker.com/_/wordpress/) but it should not be used on production environment.

This is an example only.

Use on your own risk.
