1.配置谷歌云
1.1 谷歌云免费试用300美金3个月
1.2 创建VM实例
1.2.1 选择最简单的内核（省钱）， 配置linux则选择标准配置，50GB.允许https，，后期开启ssh，则可以在安全中配置公钥
1.2.2 创建实例后得到外部ip， terminal ping ip，速度50ms左右则到VMC的ip外部网络中将类型设置成固定ip。
1.2.3设置防火墙。设置出站规则， 开启出站out， 范围设置0.0.0.0/0;  开启入站in， 范围设置0.0.0.0/0, 两个协议和关口都选择全部允许

2. 配置v2ray
2.1 sudo passwd 设置root密码，切换root账户
2.2 v2ray 
(1)安装脚本  bash <(curl -s -L https://git.io/v2ray.sh)
(2)选择tcp
(3)设置自己的端口
(4)完成配置

2.3魔改加速内核脚本
    wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh"
    chmod +x tcp.sh
    ./tcp.sh
后续操作可使用./tcp.sh操作

2.4 sudo v2ray url 获取vemms连接， v2ray-1 查看配置手工配置

