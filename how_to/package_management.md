# Package Management

Below is the commands you can use in eopkg our package management system.

| Command | Shortcut | Action taken | Example |
|----|----|----|----|
| add-repo | ar | Add a new repository | sudo eopkg ar Solus2 http://www.example.com/main/eopkg-index.xml.xz |
| delete-cache | dc | Delete's .eopkg file cache | sudo eopkg dc |
| fetch | fc | Download an eopkg but do not install | eopkg fc gedit |
| help | ? | Displays help information | eopkg help |
| history | hs | Displays eopkg's activity history | eopkg hs |
| info | N/A | Display information on a package | eopkg info gedit |
| install | it | Install a specified package | sudo eopkg it gedit |
| list-available | la | List packages available for installation | eopkg la |
| list-installed | li | List packages already installed | eopkg li |
| list-repo | lr | List repositories on the PC  | eopkg lr |
| rebuild-db | rdb | Rebuilds local database | sudo eopkg rdb |
| remove | rm | Remove specific package(s) | sudo eopkg rm gedit |
| remove-repo | rr | Remove the specified repository | sudo eopkg rr Solus2 |
| search | sr | Search repository for text | eopkg sr gedit / eopkg sr editor |
| update-repo | ur | Update package information from the repository | sudo eopkg ur |
| upgrade | up | Upgrade installed packages on the system | sudo eopkg up |
