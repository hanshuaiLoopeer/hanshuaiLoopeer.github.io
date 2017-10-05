#Swift 服务端部署文档

##准备服务器
* 部署 unbuntu 系统，系统版本参考 [https://swift.org/download/](https://swift.org/download/)
* 设置并记录 root 用户密码
* 终端用 root 用户，公网 ip，ssh 登录服务器
* 创建自己的用户，以后都用自己的用户登录，参考[在Ubuntu上创建用户](https://www.howtoing.com/how-to-create-a-sudo-user-on-ubuntu-quickstart/) 
* 给自己用户配上ssh, 参考 [How To Set Up SSH Keys](https://www.digitalocean.com/community/tutorials/how-to-set-up-ssh-keys--2)
* 给 server 配上域名 A 解析

##配置环境
* 安装 git： sudo apt install git (可能需要更新 apt: sudo apt-get update)
* 用 root 用户生成 ssh key, 设置到 bitbucket。（在生成ssh的命令前加上 sudo，就是用 root 用户生成。普通用户的key放在 /home/user/.ssh/ 而 root 用户生成的key放在 /root/.ssh/，生成 ssh 的命令参考 [生成sshkey](http://www.jianshu.com/p/697fe0815689)）
* 配置 swift 环境
	* 推荐用脚本安装 [Perfect-Ubuntu](https://github.com/PerfectlySoft/Perfect-Ubuntu)
	* 可以用 apt-get 安装 [Swift 3.0 安装](http://swift.gg/2016/07/19/swift-3-0-for-ubuntu-16-04-xenial-xerus/)
	* 可以自己下压缩包，解压 [Ubuntu 部署 Perfect](http://www.bijishequ.com/detail/427445?p=56-50)
	* 如果 Swift 环境安装失败（或没有安装），输入 swift --version, 会返回：

	```
	The program 'swift' can be found in the following packages:
 * python-swiftclient
 * python3-swiftclient
Try: sudo apt-get install 
	
	```
	
##部署SQL



