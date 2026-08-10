Nginx (pronounced "Engine-X") is a high-performance, event-driven web server and reverse proxy. It is the standard choice for modern deployments -- serving static content at scale, terminating TLS, and proxying to application servers like Node.js, PHP-FPM, or Python back-ends.

- Nginx
  - Introduction 🔴
    - What Nginx is (web server + reverse proxy + load balancer)
    - Event-driven, asynchronous architecture
    - Nginx vs Apache
  - Installation 🔴
    - Linux: `sudo apt install nginx`
    - macOS: `brew install nginx`
    - Docker: `docker run -p 80:80 nginx`
  - Commands 🔴
    - Start/stop: `sudo systemctl start|stop|restart nginx`
    - Reload (zero-downtime config): `sudo nginx -s reload`
    - Test config: `sudo nginx -t`
    - Status: `sudo systemctl status nginx`
  - Configuration 🔴
    - Main config: `/etc/nginx/nginx.conf`
    - Site configs: `/etc/nginx/sites-available/` + `sites-enabled/`
    - Default config structure
      - `http` -> `server` -> `location`
    - Directives and blocks
  - Serving static files 🔴
    - `root` vs `alias`
    - `index`
    - ```
      server {
          listen 80;
          server_name example.com;
          root /var/www/html;
          index index.html;
      }
      ```
  - Reverse proxy 🔴
    - `proxy_pass http://127.0.0.1:3000;`
    - Proxying to Node.js, Python, etc.
    - Passing headers (`proxy_set_header`)
  - PHP-FPM 🔴
    - `location ~ \.php$ { fastcgi_pass unix:/run/php/php-fpm.sock; }`
  - Location blocks 🔴
    - Prefix match `location /api { }`
    - Exact match `location = / { }`
    - Regex `location ~ \.css$ { }`
    - Match priority
  - Server blocks (virtual hosts) -- multiple sites on one server 🔴
  - HTTPS / SSL 🔴
    - `listen 443 ssl;`
    - `ssl_certificate`, `ssl_certificate_key`
    - Let's Encrypt with Certbot 🔴
      - `sudo certbot --nginx -d example.com`
      - Auto-renewal
  - Load balancing 🔴
    - `upstream` block
    - `least_conn`, `ip_hash`
  - Logging
    - Access log `/var/log/nginx/access.log`
    - Error log `/var/log/nginx/error.log`
    - Custom log formats
  - Performance tuning
    - `worker_processes auto;`
    - `worker_connections`
    - Gzip compression 🔴
    - Client caching headers (`expires`)
    - Buffer sizes
  - Security 🔴
    - Security headers
    - Rate limiting (`limit_req`)
    - Deny/allow IPs
    - Hide Nginx version (`server_tokens off`)
  - HTTP/2 and HTTP/3
  - Common pitfalls 🔴
    - `proxy_pass` trailing slash semantics
    - `try_files` for SPAs (React/Vue)
    - File permissions (`www-data` user)

---
🔴 Very Important
