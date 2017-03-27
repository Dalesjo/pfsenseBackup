# pfsenseBackup
Backup script for pfSense 2.3 or above. Downloads config file to directory and store it as a gzip file. Based on information from the pfSense doc https://doc.pfsense.org/index.php/Remote_Config_Backup

#### Example:
pfsenseBackup -d /var/backup/pfsense/ -h 192.168.0.1 -u admin -p mypassword

#### Return codes
0) Successfull backup
1) Missing parameter
2) Directory does not exist or is not writable.
3) wget is missing or can not be found in path.
4) gzip is missing or can not be found in path.
5) backupfile could not be downloaded, possible network error/timeout.
6) backupfile does not include xml tag &lt;pfsense&gt;, possible wrong credentials.
