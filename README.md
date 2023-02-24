# Nextcloud Backup

Custom Frappe App for backups to your nextcloud instance.

Also works with other WebDAV based systems like owncloud

### Features
This app lets you take backup of your database, config and files to your Nextcloud instance. You can configure it to take daily or weekly backups.

### Installation
On your site you can download and install *nextcloud-integration* app using

```
bench get-app https://github.com/frappe/nextcloud-backup.git
bench --site {site_name} install-app nextcloud_backup
```

### Configuration

After successful installation of *nextcloud-integration* app You can search for **Nextcloud Settings** in the **Awesome Bar** which will direct you to the following **Nextcloud Settings** page

<kbd><img src=".github/nextcloud_setting_screen.png" alt="Nextcloud Setting Screen" /></kbd>

* **Username**: Your *Nextcloud Account Username*
* **Password**: Your *Nextcloud Account password* or *App Password* you might have created for this app.
* **Nextcloud URL**: URL of site where Nextcloud Account exist. *For eg("https://example.com")*.
Optionally you can also provide a port number after your URL as *("https://example.com:443")*
* **WebDav URL**: You will find this in your Nextcloud Account. Example: */remote.php/dav/files/*{email_address}*/*
* **Path to Upload Folder**: You can provide the *path* of folder where you would like your files to be uploaded.
	* **NOTE**:
		1. The folder should have already been created.
		2. If not provided, a folder *Frappe Backups* will be created.
* **Backup Frequency**: One of either *Daily* or *Weekly* can be choosen.
* **Backup Files**: Check this option to *Backup public and private files along with the database*.
* **Send Notifications To**: Email on which the notification for Backups should be sent.
* **Send Email for Successful Backup**: Check this option to receive email for successful backups, by default emails for failed backups are sent.

After saving the configuration click on **Backup Now** button and verify if the files where uploaded in your *Nextcloud* instance.

**NOTE**: This process generally takes from a few minutes to half an hour depending on the size of your backup.

### License
This repository has been released under the [MIT License](LICENSE).
