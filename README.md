# github无法访问

从昨天开始，我电脑的github就开始无法访问了。

找了很多，发现改hosts文件是最简单的，但网上有很多给了在我的电脑上并不管用，比如

```
192.30.252.131 github.com
185.31.16.185 github.global.ssl.fastly.net
```

后面我以为是自己蓝灯打开了的问题，所以我把蓝灯关了，但还是没有用。

后面看到有说道是dns污染，我打开我的命令行窗口，输入

```
ipconfig/flushdns
```

来清理dns缓存，还是无效。最后发现了一个很好的[博主](http://blog.csdn.net/friend_ly/article/details/51933287)说明了一切。

将hosts文件改为

```
#Github
192.30.252.131 https://github.com 
185.31.16.185 https://github.global.ssl.fastly.net
```

将可以打开github了。