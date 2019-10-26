# IOS版本使用方法

•  点击 [tap to install on device v13]

•  此时回到桌面看到YouTube已经下载完成

•  去ios设置->描述文件与设备管理->点击[china telecon corporation]->信任


完成,此时已经可以打开YouTube观看,但底部会有开发者设置的广告。


# 关于去广告

1. 在surge中添加如下字段即可去YouTube++底部广告

```
[URL Rewrite]
https?://api.catch.gift/api/v3/pagead/ - reject
```

2. 在quanX中添加如下字段即可去YouTube++底部广告
```
[rewrite_local]
^https?://api.catch.gift/api/v3/pagead/ url reject
```
