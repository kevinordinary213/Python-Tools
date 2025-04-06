需要用到scapy
可以随便找一个国内镜像站安装，例如清华的：https://pypi.tuna.tsinghua.edu.cn/simple

```
from whois import whois
from scapy.all import *
from random import randint


def main():
    print('xxx.xxx.xxx.xxxis up')
    ip = 'xxx.xxx.xxx.xxx'
    dport = randint(1, 65535)

    packet = IP(dst=ip) / TCP(flags="A", dport=dport)
    response = sr1(packet, timeout=1.0, verbose=0)
    if response:
        # RST
        if int(response[TCP].flags) == 4:
            time.sleep(0.5)
            print(ip + 'is up')
        else:
            print(ip + 'is down')

    pass


if __name__ == '__name__':
    main()

```
之后可实现简单的tcp扫描
