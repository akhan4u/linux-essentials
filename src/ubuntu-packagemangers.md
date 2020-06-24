
# Package Managers of Ubuntu

apt, apt-get and dpkg are Package manager's of Ubuntu Linux.



### To check the list of packages available in the repositories
```bash
  apt list | grep package-name
  apt-cache pkgnames | grep package-name
  apt-cache search package-name
  apt-file search/find package-name
```

### To list the installed packages of the system
```bash
  apt list --installed | grep package-name
  dpk --get-selections
```
  Also you can evaluate the `/var/log/apt/history.log` file for looking at the history of packages installed.

### To get the list of files installed from a particular package
```bash
  apt-file list package-name | grep conf$
  dpkg-query -L package-name | grep filename
```

### To update the packages available in the system
```bash
  apt-get update
  apt update
```

### To upgrade the packages in the system
```bash
  apt-get upgrade
  apt upgrade
```

### To hold a package for the upgrade/update
```bash
  apt-mark hold package-name
  echo "package-name    hold" | dpkg --set-selections
```

### To get the details of the packages kept on hold
```bash
  apt-mark showhold
  dpkg --get-selections | grep hold
```

### To unhold the package for the system update
```bash
  apt-mark unhold
  echo "package-name   install" | dpkg --set-selections
```

### To list the packages installed automatically or manually
```bash
  apt-mark showauto
  apt-mark showmanual
```

### To see the list of up-gradable packages in the system
```bash
  apt list --upgradable
  apt-get upgrade --dry-run
```

### To remove the packages automatically from the system that are not needed anymore
```bash
  apt autoremove
  apt-get autoremove - Remove automatically all unused packages
  apt-get autoclean  - Erase old downloaded archive files
  apt-get clean      - Erase downloaded archive files
```

### To see the list of sources of repositories configured
```bash
  apt edit-sources	-- sources file /etc/apt/sources.list.
```

### This gives you information of all available package versions
```bash
  apt-cache policy <packageName>
```

### To install a package in the system
```bash
  apt install package-name
  apt-get install package-name
  dpkg -i package-name.deb
```

### To erase the package from the system
```bash
  apt remove package-name
  apt-get remove package-name  - Remove the package
  apt-get purge package-name   - Remove the package/configuration files
```

### To go for the distribution update
```bash
  apt-get dist-upgrade
  do-release-upgrade
```

### To check the package for broken dependencies
```bash
  apt-get check package-name
```

### `apt-add-repository` is a script for adding apt sources.list entries
  `apt-add-repository <source-line>` - The apt repository source line to add. This is one of:
 - a complete apt line in quotes,
 - a repo url and areas in quotes (areas defaults to'main')
 - a PPA shortcut.
 - a distro component

### To get the changelog information of some package (so we can check for the vulnerability updates viz: CVE)

```bash
apt-get changelog package-name | grep -i cve
rpm -q --changelog package-name   - Incase of rpm based distro
aptitude changelog package-name   - Incase of the aptitude pkg manager.
```
