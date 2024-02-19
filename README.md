# Local Web Server Docker Compose
This repository provides a Docker Compose setup for a local web server with:

* **Caddy web server:** Secure and automatic HTTPS configuration.
* **PHP:** Popular language for dynamic websites.
* **MariaDB:** Robust and widely used database engine.
* **phpMyAdmin:** Web-based interface for managing MariaDB databases.
* **FTP access:** Easy file transfer capabilities.

**Prerequisites:**

* Docker and Docker Compose installed on your system.

**Getting started:**

1. Clone this repository: `git clone https://github.com/aera128/caddy-local-web-server-docker-compose.git`
2. Replace the following placeholders in `docker-compose.yml`:
    * `changeme` with strong passwords for `MYSQL_ROOT_PASSWORD`, `PMA_PASSWORD`, and `FTP_PASS`. (use the same password for `MYSQL_ROOT_PASSWORD` and `PMA_PASSWORD`)
    * Update file paths for custom configurations (optional):
        * `./Caddyfile`
        * `./www` (web root)
        * `./php_config/php.ini`
        * `./db_data`
        * `./ftp_data`
3. Start the application: `docker-compose up -d`

**Accessing your application:**

* Web interface: https://localhost (automatically serves your files from `./www`)
* phpMyAdmin: http://localhost:8123 (use the passwords you set)
* FTP access:
    * Use any FTP client (e.g., FileZilla, Cyberduck)
    * Connect to `localhost` on port `21` or `40000` - `40009` (passive mode)
    * Use the username and password you set in `docker-compose.yml`

**Customization:**

* Refer to the official documentation for further configuration options:
    * Caddy: [https://caddyserver.com/docs/](https://caddyserver.com/docs/)
    * PHP: [https://www.php.net/](https://www.php.net/)
    * MariaDB: [https://mariadb.com/kb/en/documentation/](https://mariadb.com/kb/en/documentation/)
    * phpMyAdmin: [https://www.phpmyadmin.net/](https://www.phpmyadmin.net/)
    * GarethFlowers/ftp-server: [https://github.com/garethflowers/docker-ftp-server](https://github.com/garethflowers/docker-ftp-server)

**Disclaimer:**

* This setup is intended for development purposes only.
* Consider security best practices for production environments.

**Contributions:**

Pull requests and suggestions are welcome!

**Additional notes:**

* This README provides a basic outline. You may need to adjust it based on your specific needs and preferences.
* You can add links to relevant documentation and resources.
* Consider including information about how to build custom images or use a CI/CD pipeline.

I hope this helps!