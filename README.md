# better-cloudflare-ip
原作者: https://github.com/badafans ~（已删库）~

原作者版本已更新：https://github.com/badafans/better-cloudflare-ip

查找适合自己当前网络环境的优选Cloudflare Anycast IP
**因为原作者的api已经失效，项目暂时不可使用，请等待我重写一个API**
## 用户数据安全声明

1.此版本需要上传用户部分非敏感数据到服务器（Anycast IP、峰值速度、用户AS自治域、用户META城市归属）

2.用户上传的数据用来做模型分析建立关系数据库，建立精准IP推送的模型（类似机器学习）

3.人人为我，我为人人的原则！数据提交的样本越多，同一运营商级别下的匹配程度越高（快速出结果）

4.服务端不会保存任何关系用户的其它无效数据，只为提高数据精确程度设计的定向性算法（避免大海捞针）

5.服务端程序目前不会对外开源，涉及到算法模型结构等问题，后续版本会不断改进算法模型（此项目的侧重点）

6.对于担心用户数据安全问题的，请自觉使用20210307以前的版本（无法使用大数据分析模型带来优质的IP）


## Windows版本

windows批处理全自动无门槛操作

fping-4.2 for win32 修改版（基于 msys2.0 修改编译）点击下载[Windows版本](https://proxy.freecdn.workers.dev/?url=https://github.com/daycat/better-cloudflare-ip/releases/latest/download/windows.zip)

## Linux版本

linux shell脚本+fping

具体使用流程，需要编译里面 fping 4.2 修改版本，另外需要系统安装curl支持。

下载修改过的源码 fping-4.2.tar.gz  点击下载[Linux源码](https://proxy.freecdn.workers.dev/?url=https://github.com/daycat/better-cloudflare-ip/releases/latest/download/linux.tar.gz)

具体编译使用流程如下
 
 ```bash
curl 'https://proxy.freecdn.workers.dev/?url=https://github.com/daycat/better-cloudflare-ip/releases/latest/download/linux.tar.gz' -o linux.tar.gz

tar -vxf linux.tar.gz

cd linux

./configure

make

cd src

sudo ./cf.sh
```

## Android版本

安装termux，完整复制下方链接粘贴到termux并回车，后续运行只需输入./cf.sh并回车即可

``` bash
curl https://proxy.freecdn.workers.dev/?url=https://raw.githubusercontent.com/daycat/better-cloudflare-ip/master/shell/cf.sh -o cf.sh && chmod +x cf.sh && ./cf.sh
```

## OpenWrt版本

完整复制下方链接粘贴到openwrt shell并回车，后续运行只需输入./cf-openwrt.sh并回车即可

``` bash
curl https://proxy.freecdn.workers.dev/?url=https://raw.githubusercontent.com/daycat/better-cloudflare-ip/master/shell/cf-openwrt.sh -o cf-openwrt.sh && chmod +x cf-openwrt.sh && ./cf-openwrt.sh
```

## 引用声明

其中 fping 是基于 GitHub 开源项目 https://github.com/schweikert/fping  4.2发行版修改而来，所有脚本均为本人原创内容，转载请注明出处！

对于 Cloudflare Anycast 节点汇总，定期扫描 Cloudflare 公开节点汇总而来，Cloudflare IP Ranges 来自 https://www.cloudflare.com/zh-cn/ips/
