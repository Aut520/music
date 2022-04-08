# 音乐搜索器
[📦 下载开发版](https://github.com/maicong/music/archive/master.zip) [📦 获取稳定版](https://github.com/maicong/music/releases)

## 解决方案

**1. 提示数据获取失败**

方案1：

```
修改 index.php 文件里的 MC_PROXY 为您的代理地址
将 core/music.php 里需要代理的 URL 'proxy' => false 改为 'proxy' => true
```

方案2：

```
在 core/music.php 里查找 setTimeout，将其后面的数值 20 改为更大。
在 static/js/music.js 里查找 `timeout`，将其数值 30000 改为更大。
```

方案3：

```
服务器要支持 curl。
更换服务器，选择延迟更低的服务器。
```

**2. 播放器显示 `Error happens ╥﹏╥`**

音乐链接为空

```
1. 音乐需要付费才能收听
2. 版权限制，外站无法获取
3. 服务器 IP 所在地不在源站允许的区域
4. 音乐下架了，链接被去除
```

音乐链接不为空

```
1. 当前 IP 所在地因版权限制而无法播放
2. 音乐格式浏览器无法正常解析
```

**3. 国内接口优化**

如果你的网站在国内，打开 [/index.php](index.php)，将 `define('MC_INTERNAL', 0);` 修改为 `define('MC_INTERNAL', 1);`，这样就可以取到咪咕和网易云音乐的 320k 音频了。

## 更新日志

请查看 [CHANGELOG.md](CHANGELOG.md)

## 免责声明

1. 本站音频文件来自各网站接口，本站不会修改任何音频文件
2. 音频版权来自各网站，本站只提供数据查询服务，不提供任何音频存储和贩卖服务
3. 本项目代码仅供学习交流，不得用于商业用途，如有侵犯与代码贡献人员无关
