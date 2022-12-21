---
sidebar_position: 1
---

# Migration

Let's migrate **Phyliactyl in less than 5 mins! ⌛**.

# Migrating to Phyliactyl

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
php artisan migrate --seed --force
chown -R www-data:www-data /var/www/pterodactyl/*
chown -R www-data:www-data /var/www/pterodactyl/Phyliactyl
sudo systemctl restart --now redis-server
sudo systemctl restart --now pteroq.service
php artisan up
```

Done `Phyliactyl` shuttle installed and migrated successfully!
Thanks a lot for usage Phyliactyl! **[Our Discord](https://discord.gg/TNxDenRcxx)**.