# Redhat Package Manager ( YUM )

`yum` is the package manager for Redhat based system.

Help display yum commands and options
```
yum help
```
### Individual packages

List package names from repositories
```
yum list available
```

List all available packages
```
yum list installed
```

List all installed packages
```
yum list all
```

List installed and available packages
```
yum list kernel
```

List info about vsftpd package
```
yum info vsftpd
```

Display dependencies for a package (deplist)
```
yum deplist nfs-utils
```

### Find packages that provide the queried file

Show package that contains top command
```
yum provides “*bin/top”
```

Show package containing README.top file
```
yum provides “*/README.top”
```

### Search package names and descriptions for a term

Find packages with samba in name or description
```
yum search samba
```

Get information about available package updates
```
yum updateinfo security
```

### Groups of packages

Display description and contents of a package group
```
yum groupinfo “Web Server”
```
### Manage Yum Repositories

Display information about enabled yum repositories

```
yum repoinfo rhel-7-server-rpms
```

See info on rhel-7-server-rpms repo
```
yum repo-pkgs my-rpms list
```

List packages from my-rpms repo
```
yum repo-pkgs my-rpms install
```

Remove all packages from my-rpms repo
```
yum repo-pkgs my-rpms remove
```

### Troubleshoot And Maintain Yum

List all yum install, update and erase actions
```
yum history list
```

Show details of yum transaction 3
```
yum history info 3
```

Undo the yum action from transaction 3
```
yum history undo 3
```

Clear out cached package data
```
yum clean packages
```

Clean out all packages and meta data from cache
```
yum clean all
```

### Install, Remove And Upgrade Packages With Yum

Install the vsftpd package
```
yum install vsftpd
```

Update one or all packages on your system
```
yum update
```

Update the httpd package (if available)
```
yum update httpd
```

Apply security-related package updates
```
yum update --security
```

Reinstall the current version of a package
```
yum reinstall util-linux
```

Downgrade a package to an earlier version
```
yum downgrade abc
```

Install abc package from local directory
```
yum localinstall http://myrepo/abc-1-1.i686.rpm
```

Remove the vsftpd package and dependencies
```
yum remove vsftpd
```

autoremove Same as erase, plus removes additional unneeded packages *
```
yum autoremove httpd
```

### Popular Options For Different Yum Commands

Option Description

```
-y                               - Assume yes if prompted
--assumeno                       - Assume no if prompted
-q                               - Produce no output
-v                               - Produce extra debugging output
--noplugins                      - Run command without loading any yum plugins
--disableplugin                  - Disable a particular plugin for single command
--enableplugin                   - Enable a plugin that is installed, but currently disabled
--changelog                      - Display changelog information of package
--enablerepo                     - Enable currently disabled repo for a single command (wildcards okay)

yum install docker --enablerepo=rhel-7-server-extras-rpm

--disablerepo                    - Disable currently enabled repo for a single command (wildcards okay)

yum list available --disablerepo=epel

--downloadonly                   - Download to /var/cache/yum/ arch / prod / repo / packages/, but don’t install

Download vsftpd package to cache
yum install --downloadonly vsftpd

```

### More Yum-Related Commands (install the yum-utils package)

Command Description

```
find-repos-of-install               - Find which repository a package comes from
needs-restarting                    - Find processes that have been updated and need to restart
repoquery --requires --resolve bash - Show dependent packages
reposync                            - Synchronize yum repositories to a local directory
repotrack                           - Download a package and all its dependencies
show-installed                      - List installed RPM packages and statistics
verifytree                          - Check the local yum repository for consistency
yum-complete-transaction            - Try to complete yum transactions that didn’t finish
yumdb                               - Check or change the yum database
yumdownloader                       - Download a package from a repo to current directory
```
