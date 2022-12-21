---
sidebar_position: 1
---

# Introduction

Let's discover **Phyliactyl in less than 5 mins! ⌛**.

## Getting Started

Get started by **Installing Pterodactyl**.

Or **try Docusaurus immediately** with **[pterodactyl-installer.se](https://github.com/pterodactyl-installer/pterodactyl-installer)**.

### Pterodactyl Auto-Installer
- [Pterodactyl-Installer](https://pterodactyl-installer.se) ():
```bash
bash <(curl -s https://pterodactyl-installer.se)
```
- Then just continue install with your own options.

## Installing Phyliactyl


### Supported panel and wings operating systems

| Operating System | Version | Supported          | PHP Version    |
| ---------------- | ------- | ------------------ | -------------- |
| Ubuntu           | 18.04   | :red_circle:       |                |
|                  | 20.04   | :white_check_mark: | 8.1.13         |
|                  | 22.04   | :white_check_mark: | 8.1.13         |
| Debian           | 9       | :red_circle: \*    |                |
|                  | 10      | :white_check_mark: | 8.1.13         |
|                  | 11      | :white_check_mark: | 8.1.13         |

#### First go to pterodactyl directory.
```bash
cd /var/www/pterodactyl
```

#### First go to pterodactyl directory.
```bash
wget https://github.com/kinseyy/Phyliactyl/archive/refs/tags/1.15.0-beta1.zip
```
or
```bash
git clone https://github.com/kinseyy/Phyliactyl.git
```

#### Then, let's unzip and apply files to Pterodactyl.

```bash
cd /var/www/pterodactyl
mkdir Phyliactyl
cd Phyliactyl
unzip 1.15.0-beta1.zip
cd Phyliactyl-1.15.0-beta1
mv 1.15.0-beta1.zip ../.. && cd ../..
unzip 1.15.0-beta1.zip # Choose option [A] All when system asks you replace option.
```

#### Building Phyliactyl

```bash
cd /var/www/pterodactyl
php artisan down
php artisan phyliactyl:install
php artisan up
```

Then for continue installation process write word `CONFIRM` (with CAPS).
After install go to **[Migration to Phyliactyl](/migration)**.