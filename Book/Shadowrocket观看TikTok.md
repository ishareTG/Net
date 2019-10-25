# Shadowrocket观看TikTok操作步骤

1.打开Shadowrocket
---------------------  
2.生成证书文件（先查看版本）
---------------------  
Shadowrocket 2.1.24（717）之前版本：设置 – 证书 – 生成新的 CA证书 – 安装证书
Shadowrocket 2.1.24（717）之后版本：配置 – 点击一个配置文件（默认是default.conf） – 编辑配置 – 开启 HTTPS 解密 – 生成新的 CA证书 – 安装证书

3.点右上角 – 安装 – 输入手机锁屏密码 – 再次点右上角 – 安装 – 安装 – 右上角 – 完成
---------------------  

4.打开手机设置 – 通用 – 关于本机 – 证书信任设置 – 找到 – Shadowrocket开头的选项 – 打开右侧开关 – 弹出警告框 – 继续
---------------------  

5.再次打开Shadowrocket – 配置 – 找到[本地文件]内的配置文件，默认是[default.conf] – 点击 – default.conf – 编辑纯文本
---------------------  

6.Shadowrocket 2.1.24之后版本复制第一段代码粘贴到最后
---------------------  
```
[Rule]
DOMAIN,api-h2.tiktokv.com,PROXY
DOMAIN,api2-16-h2.musical.ly,PROXY
DOMAIN,api2-19-h2.musical.ly,PROXY

[URL Rewrite]
(.*video_id=\w{32})(.*watermark=)(.*) $1 302
((carrier|account|sys)_region=)CN JP 302

[MITM]
hostname = ,api*.tiktokv.com,*.musical.ly,
enable = true

```
Shadowrocket 2.1.24之前版本复制下面这一段，粘贴到App内编辑的文档内
---------------------  
```
[Rule]
DOMAIN,api-h2.tiktokv.com,PROXY
DOMAIN,api2-16-h2.musical.ly,PROXY
DOMAIN,api2-19-h2.musical.ly,PROXY

[URL Rewrite]
(.*video_id=\w{32})(.*watermark=)(.*) $1 302
((carrier|account|sys)_region=)CN JP 302

[MITM]
hostname = ,api*.tiktokv.com,*.musical.ly,
enable = true
```

然后点击右上角 – 保存

7.最后返回首页添加节点（节点自备），全局路由选择配置、代理均可，然后开启连接（首次开启需要验证 – Allow – 指纹/密码）
---------------------  
8.开启美区TikTok（强调，不是国内版抖音），愉快~
---------------------  

额外说明：
============
如果需要观看不同国家的视频，只需要修改代码中的JP，比如

* 切换到 US ：((carrier|account|sys)_region=)CN US 302

* 切换到 UK：((carrier|account|sys)_region=)CN US 302

* 切换到台湾省：((carrier|account|sys)_region=)CN TW 302


