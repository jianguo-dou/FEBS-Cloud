-> 后台启动
nohup java -jar XXX.jar >XXX.txt &
使用这种方式运行的程序日志会输出到当前目录下的nohup.out文件，使用ctrl+c中断或者关闭窗口都不会中断程序的执行

E.g.
nohup java -jar febs-tx-manager-2.2-RELEASE.jar &
nohup java -jar febs-admin-2.2-RELEASE.jar &
nohup java -jar febs-auth-2.2-RELEASE.jar &
nohup java -jar febs-server-system-2.2-RELEASE.jar &
nohup java -jar febs-gateway-2.2-RELEASE.jar &

-> 查看进程
ps aux|grep xxx.jar

ps aux|grep febs-tx-manager-2.2-RELEASE.jar
ps aux|grep febs-admin-2.2-RELEASE.jar
ps aux|grep febs-auth-2.2-RELEASE.jar
ps aux|grep febs-server-system-2.2-RELEASE.jar
ps aux|grep febs-gateway-2.2-RELEASE.jar

-> 停止
kill -9 {pid}

-> target目录下查看后台任务
jobs

-> 批量启动
cd /
cd /Users/doujianguo/FEBS-Cloud/febs-tx-manager/target
nohup java -jar febs-tx-manager-2.2-RELEASE.jar &
cd /
cd /Users/doujianguo/FEBS-Cloud/febs-apm/febs-admin/target
nohup java -jar febs-admin-2.2-RELEASE.jar &
cd /
cd /Users/doujianguo/FEBS-Cloud/febs-auth/target
nohup java -jar febs-auth-2.2-RELEASE.jar &
cd /
cd /Users/doujianguo/FEBS-Cloud/febs-server/febs-server-system/target
nohup java -jar febs-server-system-2.2-RELEASE.jar &
cd /
cd /Users/doujianguo/FEBS-Cloud/febs-gateway/target
nohup java -jar febs-gateway-2.2-RELEASE.jar &
