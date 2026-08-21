# Add User
- Normal user with default directory created 
```bash
 useradd john 
 ```
- With options
```bash
useradd -g QA -s /bin/bash -c "Part of QA" -m -d /home/victor UserName
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