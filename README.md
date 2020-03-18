# Debian-ReInstall
NETINSTALL:     
It can reinstall Debian(Ubuntu) from CentOS/Ubuntu/Debian         

Link to: [Debian(Ubuntu)网络安装/重装一键脚本](https://moeclub.org/2017/03/25/82/)     

--------------------------------------------------------------  
--------------------------------------------------------------  
# Description
Apply to CentOS, Ubuntu, Debian that is booted by the GRUB.      
As long as you have root permissions, you also have a pure system.        
Not suitable for OPENVZ.    
  
Default root password is 'Vicer'      
Please change it as soon as possible.     

--------------------------------------------------------------    
--------------------------------------------------------------   
# 快速使用
```
#Debian10
bash <(wget --no-check-certificate -qO- 'https://raw.githubusercontent.com/sy3tem/InstallNET/master/InstallNET.sh') -d 10 -v 64 -a
#Ubuntu19
bash <(wget --no-check-certificate -qO- 'https://raw.githubusercontent.com/sy3tem/InstallNET/master/InstallNET.sh') -u eoan -v 64 -a
#Ubuntu20 (Beta)
bash <(wget --no-check-certificate -qO- 'https://raw.githubusercontent.com/sy3tem/InstallNET/master/InstallNET.sh') -u focal -v 64 -a

#CENTOS8
bash <(wget --no-check-certificate -qO- 'https://raw.githubusercontent.com/sy3tem/InstallNET/master/InstallNET.sh') -c 8.0.1905 -v 64 -a --ip-addr x.x.x.x --ip-gate x.x.x.x --ip-mask x.x.x.x

```
# 高级用法
```
bash DebianNET.sh       -d/--debian/--ubuntu [Dist Version Name]
                        -v/--ver [32/i386|64/amd64]
                        --mirror '[Mirror Server]'
                        -a/-m
```
                        

```
-----------------------------------------    
| Dists   |  Version    |  Version Name |  
-----------------------------------------    
| Debian  |   7         | wheezy        |   
|         |   8         | jessie        |
|         |   9         | stretch       | 
-----------------------------------------    
| Ubuntu  |   12.04     | precise       |
|         |   14.04     | trusty        |
|         |   15.10     | wily          |
|         |   16.04     | xenial        | 
|         |   16.10     | yakkety       | 
|         |   17.04     | zesty         |
-----------------------------------------      
```
--------------------------------------------------------------    
--------------------------------------------------------------    

# Example
First
```
wget --no-check-certificate -qO DebianNET.sh 'https://raw.githubusercontent.com/sy3tem/InstallNET/master/InstallNET.sh' && chmod -x DebianNET.sh
```
Then
```
bash DebianNET.sh -d trusty -v i386 -a
```
```
bash DebianNET.sh -d stretch -v amd64 -a --mirror 'http://mirrors.ustc.edu.cn/debian/'
```
