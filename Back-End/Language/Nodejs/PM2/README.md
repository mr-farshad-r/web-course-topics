PM2 is a production-grade process manager for Node.js applications. It keeps your app running 24/7, restarts it after crashes, enables zero-downtime reloads, and provides built-in load balancing across CPU cores.

- PM2
  - Introduction 🔴
    - What PM2 is (daemon process manager)
    - Why `node app.js` is not enough in production
  - Installation
    - `npm install -g pm2`
  - Basic commands 🔴
    - Start: `pm2 start app.js`
    - Start with name: `pm2 start app.js --name "api"`
    - List: `pm2 list`
    - Stop: `pm2 stop <app>`
    - Restart: `pm2 restart <app>`
    - Reload (zero-downtime): `pm2 reload <app>` 🔴
    - Delete: `pm2 delete <app>`
  - Cluster mode 🔴
    - `pm2 start app.js -i max`
    - Load balancing across CPU cores
  - Ecosystem file (`ecosystem.config.js`) 🔴
    - Define multiple apps
    - Environment variables per env
    - Instance count, max memory restart
    - ```
      module.exports = {
        apps: [{
          name: "api",
          script: "./src/app.js",
          instances: "max",
          env: { NODE_ENV: "production" }
        }]
      }
      ```
  - Logs 🔴
    - `pm2 logs`
    - `pm2 logs <app> --lines 100`
    - Log files location (`~/.pm2/logs`)
  - Monitoring
    - `pm2 monit` 🔴
    - CPU, memory, event loop latency
    - `pm2 status`
  - Startup script (auto-restart on boot) 🔴
    - `pm2 startup` (generates system service)
    - `pm2 save` (snapshot current process list)
  - Key metrics dashboard
    - `pm2 plus` (managed dashboard)
  - Common flags
    - `--watch` (restart on file change)
    - `--max-memory-restart`
    - `--cron`
  - Deploying updates
    - `pm2 reload ecosystem.config.js --env production`

---
🔴 Very Important
