# 这是一个固定使用 Caddy v1.0.4 和 V2Ray v4.27.0 的 233脚本 v3.34

# 修改说明
本repo从233脚本 v3.34 fork过来

本repo修改了src/download-v2ray.sh 第3行，将最新V2Ray版本写死为 v4.27.0，不会跟随最新的V2Ray版本

233脚本v3.34已经在src/download-caddy.sh 第9行，固定下载v1.0.4的Caddy

# 如果已经跑过233脚本了
依次执行

```bash
v2ray uninstall
rm -rf /tmp/233boy/v2ray
git clone https://github.com/crazypeace/v2ray -b "master" /tmp/233boy/v2ray --depth=1
cd /tmp/233boy/v2ray
chmod +x install.sh
./install.sh local
```

# 如果还没有跑过233脚本
依次执行

```bash
apt-get update -y
apt-get install -y lrzsz git zip unzip curl wget qrencode libcap2-bin dbus
git clone https://github.com/crazypeace/v2ray -b "master" /tmp/233boy/v2ray --depth=1
cd /tmp/233boy/v2ray
chmod +x install.sh
./install.sh local
```

# 后记
233的脚本从本地安装时，必须在 install.sh 脚本所在的目录执行

install.sh 的 795 行，检查$(pwd)/config目录
