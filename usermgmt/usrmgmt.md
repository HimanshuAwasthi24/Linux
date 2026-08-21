# Add User
- Normal user with default directory created 
```bash
 useradd john 
 ```
- With options
```bash
useradd -g QA -s /bin/bash -c "Part of QA" -m -d /home/victor UserName
passwd UserName
```
*Flags explanation:*
` -g ` group name 
,` -s ` Which shell is assigned
,` -c ` description
,` -m ` Home directory needs to be created
,` -d ` Path

# Delete User
```bash
userdel username //Deletes the users but directory remains
userdel -r username //Deletes with directories as well(-r recursive)
userdel -f username // deletes user even he is logged(-f forceful)
```

# Modify
```bash
usermod -G groupName Username //Added user to new group without changing his default group
usermod -g groupname username //Added user to new group with changing his default group
usermod -L username //user locked
usermod -U username //user unlocked
```

# Groups
```bash
groupadd groupname
```

## Some Important files
1. /etc/passwd -> Users details
2. /etc/group -> Group Details
3. /etc/shadow -> More about users(Password last changed, Hashed passwd,  etc)