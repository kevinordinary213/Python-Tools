```
pip install Pexpect
```

```
from pexpect import pxssh
def Login(server,username,password):
  try:
    s = pxssh.pxssh()
    s.login(server,username,password)
    print("yse")
  except:
    print("no")
def main():
  Login("xxx.xxx.xxx.xxx","root","root")
```

配合字典生成器，可以写一个暴破工具
