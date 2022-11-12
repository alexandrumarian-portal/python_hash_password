# python_hash_password

 * On Debian/Ubuntu
```
sudo apt update
sudo apt install python3-bcrypt -y
```
 * On CentOS/Rocky/Alma Linux
```
sudo yum -y install epel-release
sudo yum -y install python3-bcrypt
```

```
vim gen-pass.py

import getpass
import bcrypt

password = getpass.getpass("password: ")
hashed_password = bcrypt.hashpw(password.encode("utf-8"), bcrypt.gensalt())
print(hashed_password.decode())
```

```
python3 gen-pass.py
password: <INPUT-PASSWORD>
$2b$12$.9J0cFyfcLaNjwBW9McDWObbLjM0n0Wb0ToW9wZArxfmwVlctK8SS
```
