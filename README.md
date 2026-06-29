Plugin Name: **UpdraftPlus Backup/Restore**

The backup contains the entire production website, including things that should remain private, such as:

* WordPress source code
* Themes and plugins
* Database (users, orders, settings)
* Uploaded media
* Potential secrets (depending on configuration)

`INSTALLATION.md`

Example:

```markdown
# Installation Guide

## Requirements

- PHP 8.2+
- MySQL 8+
- Apache/Nginx
- WordPress 6.x
- UpdraftPlus Plugin

## Local Setup

1. Install WordPress.
2. Install and activate UpdraftPlus.
3. Obtain the backup files from the project owner.
4. Go to:
   Settings → UpdraftPlus Backups
5. Upload all backup files.
6. Click **Restore**.
7. Restore:
   - Database
   - Plugins
   - Themes
   - Uploads
8. Log in using the provided administrator credentials.

## Notes

- Backup files are intentionally excluded from this repository.
- Contact the repository owner for authorized access to production backups.
```

Also add the backup files to `.gitignore`:

```gitignore
# UpdraftPlus backups
updraft-*.zip
updraft-*.gz
updraft-*.crypt
*.wpress

# WordPress uploads
wp-content/uploads/

# Environment
.env
```

