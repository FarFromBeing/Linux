1.给新用户创建root密码：用当前登录用户打开终端，在终端输入命令 sudo passwd，输入当前用户的密码然后回车
2.删除所有内容：先用G 转到文件尾，然后使用下面命令：1, .d
3.显示网卡接口，实现上网：/sbin/dhclient 
4.强制无条件删除非空文件夹：rm -rf dirname
  删除空文件夹：rmdir -p dirname
5.查看所有用户列表：cat /etc/passwd
6.创建用户：useradd test1
7.给创建的用户设置密码：passwd test1
8.删除用户：userdel test1
9.Centos命令：yum update
10.SS重启：systemctl restart shadowsocks  
查看进程号:netstat -anp | grep 1080
11.查看ss: systemctl status shadowsocks -l
	   ssserver -c /etc/shadowsocks.json -d start
	   ssserver -c /etc/shadowsocks.json -d stop
	   ssserver -c /etc/shadowsocks.json -d restart
12.查看最近用户登录,显示ip,时间，状态：last
13.查看内核信息：uname -a 
14.查看进程：ps -au
15.杀死yum进程：kill -s 9 (制定了传递给进程的信号是９，即强制、尽快终止进程) yum
16.改变文件名mv xxx xxx1
17.cat | bash #执行这条命令后可以直接在其之后执行其他命令，除了这条命令不会留下其他目录的历史，Tab键功能不能用
	echo > ~/.bash_history #清除当前用户所有记录到文件里的记录
	history -c #清楚所有历史纪录，不能清除文件里的
	history -d {n} #清除历史纪录中指定的某条记录，{n}为数字
	history -d {n} && history -d {x} && history -d {y} #清除指定的多条记录，包括可以清除自身这条
	for i in {99..233}; do history -d $i; done #使用for循环清除指定连续的多条命令
18.查看当前活跃的用户：w
19.循环实时查看log:tail -f /var/log/shadowsocks.log
20. Bash下循环执行某个命令:mycount=0; while (( $mycount < 30 )); do `需要执行的命令` >>name.txt(保存名字到文件);((mycount=$mycount+1)); done;
21.scp: 
scp local_file remote_username@remote_ip:remote_folder  
scp local_file remote_username@remote_ip:remote_file  
scp local_file remote_ip:remote_folder  
scp local_file remote_ip:remote_file  

第1,2个指定了用户名，命令执行后需要输入用户密码，第1个仅指定了远程的目录，文件名字不变，第2个指定了文件名  

第3,4个没有指定用户名，命令执行后需要输入用户名和密码，第3个仅指定了远程的目录，文件名字不变，第4个指定了文件名

22.解压tar -xvf kibana-6.5.1-linux-x86_64.tar
23.解压tar.gz:tar -zxvf ×××.tar.gz
24.ls -lt|head -10（只显示前10条）
25.升序：ls -lrt
26.wc -l auth.txt: 统计auth.txt行数
27.ls | head -10|xargs -i cp -r {} /home/others: 拷贝前10个文件夹到其他目录
28.watch "ls| wc -l":每2s显示文件个数
29.lsof -i:22查看22端口情况
30.du -sh 查看磁盘使用情况
