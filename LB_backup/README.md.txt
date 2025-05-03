# LB_mysqlbkp

Automated MySQL/MariaDB backup script using `mysqldump`, built for Windows environments with HeidiSQL support.

## Features
- Runs every 6 hours via Task Scheduler
- Saves SQL backups with timestamp
- Optional auto-push to GitHub

## Setup

1. Clone this repo:
    ```bash
    git clone https://github.com/yourname/LB_mysqlbkp.git
    ```

2. Configure your database:
    Edit the `config.env` file with your DB credentials.

3. Set the correct `mysqldump` path in `LB_backup.bat`.

4. Add to Windows Task Scheduler:
    - Trigger: Daily
    - Repeat every: 6 hours
    - Action: Start a program → point to `LB_backup.bat`

## Notes
- Requires Git installed and repo initialized (`git init`, `git remote add origin ...`)
- Backup files are stored in `/backup/` with timestamps

## License
MIT
