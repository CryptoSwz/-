一个命令去进行root获取权限
sudo -i
接着去添加BBR加速，一共四个命令，分别输入即可
echo "net.core.default_qdisc=fq" >> /etc/sysctl.conf

echo "net.ipv4.tcp_congestion_control=bbr" >> /etc/sysctl.conf

sysctl -p

lsmod | grep bbr
最后返回20480说明开启成功
