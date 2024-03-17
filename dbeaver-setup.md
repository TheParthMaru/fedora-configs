- After installing dbeaver, if you encounter dark theme issue use the following commands.
- Edit the `dbeaver.desktop` entry file
```
sudo nano /usr/share/applications/dbeaver.desktop
```
- Add the following config:
```
[Desktop Entry]
Version=1.0
Type=Application
Terminal=false
Name=dbeaver-ce
GenericName=Universal Database Manager
Comment=Universal Database Manager and SQL Client.
Path=/usr/share/dbeaver-ce/
Exec=env GTK_THEME=Yaru:Light /usr/share/dbeaver-ce/dbeaver
Icon=/usr/share/dbeaver-ce/dbeaver.png
Categories=IDE;Development
StartupWMClass=DBeaver
StartupNotify=true
Keywords=Database;SQL;IDE;JDBC;ODBC;MySQL;PostgreSQL;Oracle;DB2;MariaDB
MimeType=application/sql
```

- Make the desktop entry executable:
```
sudo chmod +x /usr/share/applications/dbeaver.desktop
```

- Update desktop db
```
sudo update-desktop-database
```
