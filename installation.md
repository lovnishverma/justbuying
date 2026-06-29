# Installation Guide

## JustBuying – WordPress WooCommerce Project

This document describes how to restore the project using the provided UpdraftPlus backup files.

---

# System Requirements

* PHP 8.2 or later
* MySQL 8.0 or MariaDB 10.6+
* Apache or Nginx
* WordPress 6.x
* **UpdraftPlus Backup/Restore Plugin**

<img src="https://ps.w.org/updraftplus/assets/icon-256x256.jpg">

  The UpdraftPlus Backup & Migration Plugin is trusted by the WordPress community to backup, restore and migrate their WordPress websites. UpdraftPlus is actively installed on more than 3 million websites around the world.

---

# Backup Files

The project backup is distributed as multiple password-protected archive files.

Example:

```
part1.zip
part2.zip
part3.zip
```

These archives collectively contain the complete website backup.

**Important**

* All backup archives are password protected.
* The extraction password is **not included** in this repository.
* Authorized users should obtain the password directly from the repository owner.

---

# Restoring the Backup

## Step 1 – Install WordPress

Install a fresh WordPress instance on your server.

Do not configure any themes or plugins yet.

---

## Step 2 – Install UpdraftPlus

1. Login to WordPress Admin.
2. Navigate to:

```
Plugins
→ Add New
```

3. Search for:

```
UpdraftPlus Backup/Restore
```

4. Install the plugin.
5. Activate it.

---

## Step 3 – Extract the Backup Archives

Extract the password-protected archives using the password provided by the repository owner.

Example:

```
part1.zip
part2.zip
part3.zip
        │
        ▼
Extract
        │
        ▼
UpdraftPlus Backup Files
```

The extracted files may include:

```
backup_db.gz
backup_plugins.zip
backup_themes.zip
backup_uploads.zip
backup_others.zip
```

The exact filenames may vary depending on the backup date and UpdraftPlus version.

---

## Step 4 – Upload Backup Files

Open WordPress Admin.

Navigate to:

```
Settings
→ UpdraftPlus Backups
```

Click:

```
Upload Backup Files
```

Upload all extracted UpdraftPlus backup files.

---

## Step 5 – Restore

After all files are uploaded:

Click

```
Restore
```

Select all available components:

* Database
* Plugins
* Themes
* Uploads
* Others

Proceed with the restore process.

---

## Step 6 – Finish Restoration

Once restoration completes:

* Clear all caches.
* Log in using the administrator credentials provided by the project owner.
* Verify:

  * Homepage
  * Products
  * Checkout
  * Images
  * Plugins
  * Theme
  * Admin Dashboard

---

# Notes

* This repository is intended for portfolio and educational purposes.
* Production credentials are not included.
* Environment-specific configuration should be updated after restoration.
* Database credentials may need to be adjusted in `wp-config.php` if restoring to a different server.

---

# Security Notice

The backup archives included with this project are password protected.

The password is intentionally omitted from this repository.

Only authorized users should request the password from the repository owner.

---

# Troubleshooting

### Restore button is disabled

Ensure all required backup components have been uploaded.

---

### White screen after restore

* Clear browser cache.
* Disable conflicting plugins.
* Enable WordPress debugging.
* Check the PHP error log.

---

### Database connection error

Verify the database settings in:

```
wp-config.php
```

* Database Name
* Username
* Password
* Host

---

### Missing Images

Confirm that the **Uploads** component was restored successfully.

---

# Disclaimer

This project represents a production WooCommerce implementation.

The backup archives are provided only for authorized restoration and evaluation purposes.

Redistribution, commercial use, or unauthorized access to client data is strictly prohibited.
