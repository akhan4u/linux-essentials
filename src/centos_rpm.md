## Redhat Package Manager ( rpm )

`rpm` is a powerful Package Manager for Red Hat, Suse and Fedora Linux. It can be
used to build, install, query, verify, update, and remove/erase individual software
packages. A Package consists of an archive of files, and package information,
including name, version, and description:

Syntax Description Example(s)

### Install the package

```bash
rpm -ivh {rpm-file}
rpm -ivh mozilla-mail-1.7.5-17.i586.rpm
rpm -ivh --test mozilla-mail-1.7.5-17.i586.rpm
```

### Upgrade package

```bash
rpm -Uvh {rpm-file}
rpm -Uvh mozilla-mail-1.7.6-12.i586.rpm
rpm -Uvh --test mozilla-mail-1.7.6-12.i586.rpm
```

### Erase/remove/ an installed package

```bash
rpm -ev {package}
rpm -ev mozilla-mail
```

### Erase/remove/ an installed package without checking for dependencies

```bash
rpm -ev --nodeps {package}
rpm -ev --nodeps mozilla-mail
```

### Display list all installed packages

```bash
rpm -qa
rpm -qa
rpm -qa | less
```

### Display installed information along with package version and short description

```bash
rpm -qi {package}
rpm -qi mozilla-mail
```

### Find out what package a file belongs to i.e. find what package owns the file

```bash
rpm -qf {/path/to/file}
rpm -qf /etc/passwd
rpm -qf /bin/bash
```

### Display list of configuration file(s) for a package

```bash
rpm -qc {pacakge-name}
rpm -qc httpd
```

### Display list of configuration files for a command

```bash
rpm -qcf {/path/to/file}
rpm -qcf /usr/X11R6/bin/xeyes
```

### Display list of all recently installed RPMs

```bash
rpm -qa --last
rpm -qa --last
rpm -qa --last | less
```
### Find out what dependencies a rpm file has

```bash
rpm -qpR {.rpm-file}
rpm -qR {package}
rpm -qpR mediawiki-1.4rc1-4.i586.rpm
rpm -qR bash
