# User Management

### Add Users

Create A User (Called "ashley")
```bash
useradd --create-home ashley
```
Create A User In Groups "users" And "dev"
```bash
useradd --create-home --groups users dev ashley
```

Create A User With The Uid 1337
```bash
useradd --create-home --uid 1337 ashley
```

Create Or Change A User Password
```bash
passwd ashley
```

Add User To A Group ("coder")
```bash
usermod --append --groups coder ashley
```

### Permissions

Set Default Permission Of Files To 644
```bash
echo "masc 022" >> /etc/profile
```

Set Default Permission Of Files To 664
```bash
echo "umask 002" >> /etc/profile
```

Change Ownership Of A File ("example.txt") To User ("ashley")
```bash
chown ashley:users example.txt
```

Give Read Permission To User, Group, And Others
```bash
chmod ugo+r example.txt
```

Give Write Permission To User And Group
```bash
chmod ug+w example.txt
```

Remove Write Permission To A File For Group Members
```bash
chmod g-w example.txt
```

Make A File Executable
```bash
chmod +x example.txt
```

Log In As A Different User
```bash
su - ashley
```

Run A Command ("ls") As A Different User
```bash
su - ashley --command ls
```

### Delete Users

Remove A User From A Group ("coder")
```bash
gpasswd --delete ashley coder
```

Delete A User From The System
```bash
userdel ashley
```

Delete A User And All User Data From The System
```bash
userdel --remove ashley
```

### History

Show Which Users Are Currently Logged In
```bash
w
```

Show Login History
```bash
last
```
