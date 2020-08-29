# 说明
修改了src/download-v2ray.sh

将最新v2ray版本写死为 v4.27.0

# 如果你已经跑过233脚本了
v2ray uninstall

rm -rf /tmp/233boy/v2ray

git clone https://github.com/crazypeace/v2ray -b "master" /tmp/233boy/v2ray --depth=1

cd /tmp/233boy/v2ray

chmod +x install.sh

./install.sh local


# 如果还没有跑过233脚本
apt-get update -y

apt-get install -y lrzsz git zip unzip curl wget qrencode libcap2-bin dbus

git clone https://github.com/crazypeace/v2ray -b "master" /tmp/233boy/v2ray --depth=1

cd /tmp/233boy/v2ray

chmod +x install.sh

./install.sh local
