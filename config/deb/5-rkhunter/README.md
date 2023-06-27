#### Make a backup of rkhunter defaults config

```bash
sudo cp -p /etc/default/rkhunter /etc/default/rkhunter-BACKUP
sudo cp -p /etc/rkhunter.conf /etc/rkhunter.conf.local
```

then, edit rkhunter config in `/etc/rkhunter.conf.local`

```text
UPDATE_MIRRORS=1
MIRRORS_MODE=0
MAIL-ON-WARNING=root
COPY_LOG_ON_ERROR=1
PKGMGR=DPKG
PHALANX2_DIRTEST=1
WEB_CMD=""
USE_LOCKING=1
SHOW_SUMMARY_WARNINGS_NUMBER=1
```

after some changes

```bash
sudo dpkg-reconfigure rkhunter
sudo rkhunter -C
sudo rkhunter --versioncheck
sudo rkhunter --update
sudo rkhunter --propupd
```