# FakeToa
Fake IP sources using Linux's BPF feature

The prerequisite is that you must use the Root's shell.

运行不成功请用tcpdump抓包看下toa是否已经添加到tcp options，请不要使用公司、手机热点等会重组tcp包的网络环境，可以尝试使用腾讯云/阿里云

## Usage

> Tested On Ubuntu 22.04.03

```
# pre job
sudo apt update
sudo apt-get install linux-tools-common linux-tools-generic linux-tools-`uname -r`
git clone https://github.com/passwa11/FakeToa
cd FakeToa
python3 toa.py attach --to_ip 8.8.8.8
# set proxy
wet https://github.com/proxy/3proxy/releases/download/0.9.4/3proxy-0.9.4.×86_64.deb
dpkg -i 3proxy-0.9.4.×86 64. deb
chmod 755 /us/local/3proxy/conf/add3proxyuser.sh
/us/local/3proxy/conf/add3proxyuser.sh username password
systemctl start 3proxy.service
# use proxy
BurpSuite or SwitchyOmega: socks5://username:password@yourIP:1080 http://username:password@yourIP:3128
MacOS or unix: curl http://qifu-api.baidubce.com/ip/local/geo/v1/district -x socks5://username:password@yourIP:1080

```

![Alt text](image.png)

Refer:
![Usage](https://github.com/passwa11/FakeToa/assets/112363374/f4c9bf18-4624-4375-b9b5-08d76e1ede50)
