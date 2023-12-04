# FakeToa
Fake IP sources using Linux's BPF feature

The prerequisite is that you must use the Root's shell.

运行不成功请用tcpdump抓包看下toa是否已经添加到tcp options，请不要使用公司、手机热点等会重组tcp包的网络环境，可以尝试使用腾讯云/阿里云

## Usage
```

python3 toa.py attach --toa_ip 8.8.8.8

```

![Alt text](image.png)