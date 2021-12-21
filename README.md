# gaotie
#在Variables中点击添加变量名为PORT，值为80
A. 在Linux VPS的Terminal上安装配置命令：

1. 安装npm命令：

apt install npm

2. 安装wstunnel命令：

sudo npm install -g wstunnel


B. 在Linux VPS上远程登录Railway云的Linux系统命令：

如果提示输入密码验证，密码为 

1. 配置连接进程命令,打通与railway云的隧道连接，此处域名换成自己的：

wstunnel -t 7001:127.0.0.1:22 wss://uncleluo.up.railway.app &

注意：这里wss://后面是你自己自定义后的域名，不要忘记&符号前面有个空格，我这里以uncleluo为域名开头，你可以替换为你自己的。
如果你是Mac电脑有本地socks代理是使用1086端口的，可以直接用以下命令，此处域名换成自己的：

wstunnel -t 7001:127.0.0.1:22 --proxy socks://127.0.0.1:1086 wss://gaotie.up.railway.app &

2. 自己的Linux VPS远程登录Railway云VPS命令：

ssh root@127.0.0.1 -p 7001
