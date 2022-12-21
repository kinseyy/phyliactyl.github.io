---
sidebar_position: 1
---

# Uninstall Phyliactyl

Back again to **Pterodactyl in less than 5 mins! ⌛**.

# Migrating back!

### Supported panel and wings operating systems

| Operating System | Version | Supported          | PHP Version    |
| ---------------- | ------- | ------------------ | -------------- |
| Ubuntu           | 18.04   | :red_circle:       |                |
|                  | 20.04   | :white_check_mark: | 8.1.13         |
|                  | 22.04   | :white_check_mark: | 8.1.13         |
| Debian           | 9       | :red_circle: \*    |                |
|                  | 10      | :white_check_mark: | 8.1.13         |
|                  | 11      | :white_check_mark: | 8.1.13         |

#### Few commands.
```bash
cd /var/www/pterodactyl
php artisan down
curl -L https://github.com/pterodactyl/panel/releases/latest/download/panel.tar.gz | tar -xzv
chmod -R 755 storage/* bootstrap/cache
echo \"yes\" | composer install --no-dev --optimize-autoloader
php artisan view:clear && php artisan config:clear
php artisan migrate --seed --force
chown -R www-data:www-data /var/www/pterodactyl/*
chown -R nginx:nginx /var/www/pterodactyl/*
php artisan queue:restart
php artisan up
```

Done `Pterodactyl` has been restored! **[Our Discord](https://discord.gg/TNxDenRcxx)**.