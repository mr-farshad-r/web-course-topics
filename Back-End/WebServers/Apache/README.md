Apache HTTP Server is one of the oldest and most battle-tested web servers. It is highly configurable through `.htaccess` files, powers most shared hosting (cPanel) environments, and remains a solid choice -- especially in the PHP/LAMP stack.

- Apache
  - Introduction 🔴
    - What Apache is (veteran web server, highly modular)
    - Apache vs Nginx (process/thread model vs event-driven)
    - Still dominant on shared hosting
  - Installation 🔴
    - Linux: `sudo apt install apache2`
    - macOS: built-in Apache (`httpd`)
    - Windows: XAMPP, WAMP
    - Docker
  - Commands 🔴
    - `sudo systemctl start|stop|restart apache2`
    - `sudo apache2ctl configtest`
    - `sudo a2ensite <site>` / `sudo a2dissite <site>`
    - `sudo a2enmod <module>` / `sudo a2dismod <module>`
  - Configuration
    - Main config: `/etc/apache2/apache2.conf`
    - Sites: `sites-available/` + `sites-enabled/`
    - Mods: `mods-available/` + `mods-enabled/`
  - **`.htaccess`** 🔴
    - Directory-level configuration
    - When to use (shared hosting) vs when NOT to (performance)
    - Common uses
      - URL rewriting (`mod_rewrite`) 🔴
        - ```
          RewriteEngine On
          RewriteCond %{REQUEST_FILENAME} !-f
          RewriteCond %{REQUEST_FILENAME} !-d
          RewriteRule ^(.*)$ index.php?$1 [L,QSA]
          ```
      - Redirects (301, 302)
      - Password protection (`.htpasswd`)
      - Custom error pages
      - Block / allow IPs
      - MIME types
      - Caching and compression (`mod_deflate`, `mod_expires`)
  - Virtual Hosts 🔴
    - Name-based virtual hosting
    - `<VirtualHost *:80>`
  - MPMs (Multi-Processing Modules) 🔴
    - Prefork (one process per request)
    - Worker (threads)
    - Event (hybrid, modern)
  - Modules 🔴
    - `mod_rewrite` (URL rewriting)
    - `mod_ssl` (HTTPS)
    - `mod_php` (PHP as Apache module)
    - `mod_proxy` (reverse proxy)
    - `mod_deflate`, `mod_expires`
  - HTTPS / SSL 🔴
    - `mod_ssl`
    - Let's Encrypt + Certbot
  - PHP integration 🔴
    - `mod_php` (Apache module -- traditional LAMP)
    - PHP-FPM via `mod_proxy_fcgi` (modern, faster)
  - Logs
    - Access log `/var/log/apache2/access.log`
    - Error log `/var/log/apache2/error.log`
  - Security
    - Directory permissions
    - `AllowOverride` (controls `.htaccess` use)
    - Disable server signature
  - Common use case: cPanel shared hosting 🔴
    - `.htaccess`-based config (no root access)
    - `public_html` document root
  - When to choose Apache vs Nginx 🔴

---
🔴 Very Important
