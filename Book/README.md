### 操作步骤：

####  1.打开Quantumult

#### 2.更多 – 模块 – TUN+HTTP(Default)

#### 3.开启HTTPS解密并信任Quantumult证书，iOS12.3以下和iOS12.3以上操作略有不同：

#####     iOS12.3以下：打开设置 – HTTPS解密 – 开启HTTPS解密 – 生成密钥及证书 – 右上角点保存 – 允许安装描述文件 – 右上角点安装 – 输入手机的解锁密码 – 右上角点安装 – 安装，然后前往手机的设置 – 通用 – 关于本机 – 证书信任设置 – 找到Quantumult Custom Root Certificate…点绿它以信任该根证书 – 继续

#####     iOS12.3以上：打开设置 – HTTPS解密 – 开启HTTPS解密 – 生成密钥及证书 – 右上角点保存 – 允许安装描述文件 – 关闭，然后打开手机设置 – 找到已下载描述文件 – 安装 – 输入手机的解锁密码 – 安装，最后打开手机的设置 – 通用 – 关于本机 – 证书信任设置 – 找到Quantumult Custom Root Certificate…点绿它以信任该根证书 – 继续

#### 4.添加订阅分流链接：

##### 前往Quantumult – 设置 – 订阅 – 右上角加号 – 分流 – 链接处添加网址https://raw.githubusercontent.com/lhie1/Rules/master/Quantumult/Quantumult.conf – 名称输入分流俩字 – 个性化选项勾上 – 右上角保存 – 左划刚添加的分流 – 点选替换（这里如果失败请重试，直到出现保存页面，或者往下翻有解决方案）- 保存 – 好

#### 5.添加订阅链接阻止：

##### 再次返回设置 – 订阅 – 右上角添加 – 链接阻止 – 链接添加网址https://raw.githubusercontent.com/lhie1/Rules/master/Quantumult/Quantumult_URL.conf – 名称输入阻止俩字 – 包含主机名选项勾上 – 保存 – 左划刚添加的阻止 – 点选替换 – 好（这里如果失败请重试，直到出现保存页面，或者往下翻有解决方案）

#### 6.关于换区（默认为日本）：

##### 返回设置 – HTTP复写 – 右上角+ – 命令那选302 – 匹配填写(?<=&watermark=)1& –  替换填写& – 好 – 右上角好 ； 再次右上角加号+ – 命令307 – 匹配 – (?<=&carrier_region=|&sys_region=)CN(?=.*) – 替换改为你想看的国家/地区简写（比如日本就是JP，换区改这里） – 好 – 左上角保存
