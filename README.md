此 repo 是 CMU(卡内基梅隆大学) 15-213/18-213/15-513: **[Intro to Computer systems](http://www.cs.cmu.edu/~213/index.html)** 课程对应的实验部分

实验主页：[Lab Assignments](http://csapp.cs.cmu.edu/3e/labs.html)

课程主页：[CMU~213](http://www.cs.cmu.edu/~213/index.html)

教材：[Computer Systems A Programmer's Perspective](http://csapp.cs.cmu.edu/)

### Todo
- [x] Data Lab
- [ ] Bomb Lab
- [ ] Attack Lab
- [ ] Buffer Lab(IA32)
- [ ] Architecture Lab
- [ ] Architecture Lab(Y86)
- [ ] Cache Lab
- [ ] Performance Lab
- [ ] Shell Lab
- [ ] Malloc Lab
- [ ] Proxy Lab

### Tips
Ubuntu 平台 linux 环境下首次编译程序时若遇到：
```
fatal error: sys/cdefs.h: No such file or directory|
```

可通过安装 g++-multilib 解决：
```
sudo apt-get install g++-multilib
```


用 dlc compiler 时若遇到 `dlc: Permission denied` 可尝试：
```
chmod u+x dlc
```

运行 `sudo apt-get update` 时若出现
```
Err http://archive.canonical.com natty InRelease    
Err http://security.ubuntu.com oneiric-security InRelease               
Err http://extras.ubuntu.com natty InRelease                            
Err http://security.ubuntu.com oneiric-security Release.gpg
  Temporary failure resolving ‘security.ubuntu.com’
...
```
可运行：

`echo "nameserver 8.8.8.8" | sudo tee /etc/resolv.conf > /dev/null`

再重新运行 

`sudo apt-get update`。

若仍遇到问题：
```
E: Could not get lock /var/lib/apt/lists/lock - open (11: Resource temporarily unavailable)
E: Unable to lock directory /var/lib/apt/lists/
```
可尝试：
```
sudo rm /var/lib/apt/lists/lock
sudo rm /var/cache/apt/archives/lock
sudo rm /var/lib/dpkg/lock
```


