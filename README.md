# 流量消耗器
https://api.vv1234.cn/llxhq/
------
本文为流量消耗器的使用说明

前言;
这个东西最初产生的原因其实是因为
刚转换了芝麻卡套餐定向流量多大没地儿用,便搭建了这个个玩意儿自用
之前在网上看的的都是一些本地版的，还要消耗服务器的流量，占用服务器的带宽
便扒拉了别人的改了改，页面也增加了一些当时很火的显示元素，如显示IP归属信息等

后面陆续改了很多，增加了一堆测速节点，发现每次切换来切换去都很麻烦，便产生了更换的念头，正好看到@net909的新版工具网，界面更优雅美观，就扒拉了下来，简单了修改了下，已适应多节点切换需要，之后发布到酷安后，爆火，单日IP流量突然800+，还一度以为被打了。。

近来也发现好些个小伙伴们扒拉本站源代码，
为了方便各位动手能力强的大佬们自行部署等个性化需求,
手工扒拉这个站点也费劲儿，暂时托管到了GitHub,方便各位大佬打包下载.
相信大家也很疑惑，为啥这纯HTML的源代码，你丫标记的文件后缀是.php，其实主要是[https://api.vv1234.cn/llxhq/][1]套了cloudflare的CDN，为了避免产生缓存，我一般会重命名下，其实这都用不到PHP，，，

项目下载：
[https://github.com/uu6/llxhq][2]

因：[https://vv1234.cn/archives/881.html][https://vv1234.cn/archives/881.html] 事件，暂移除51啦统计代码并替换Staticfile相关内容等。

部署说明：
打包下载文件: https://github.com/uu6/llxhq/archive/refs/heads/main.zip
部署到你站点目录下，如果服务端环境为纯静态文件托管，如GitHub page,阿里云OSS，腾讯云COS的话，可能需要你动手重命名下文件后缀名，把.php改成.html；
如果部署旧版流量消耗器,即[https://api.vv1234.cn/llxhq/old-index.php][3] 
可参考当前路径下的 old-index.php 文件，自己指定节点的话，需要修改两处
1，指定文件直链链接![指定文件直链链接][4]
2，修改上面指定文件文件大小
(因为每成功循环一次会加上这个大小，不指定正确，会导致测速流量统计不准，
另外因为统计周期是一个文件下载完，所以，即使你设定消耗10MB流量，那如果你指定的下载文件大小为5MB，线程为3，那实际本轮将会消耗15MB流量)
![修改文件大小][5]



Gcod
2022 年 07月 19日    
欢迎各位大佬来[我博客][6]做客，添加友链
[https://vv1234.cn/archives/750.html][7]
当然，如果谁要请我喝罐可乐，我也不会拒绝
![pyjy][8]


  [1]: https://api.vv1234.cn/llxhq/
  [2]: https://github.com/uu6/llxhq
  [3]: https://api.vv1234.cn/llxhq/old-index.php
  [4]: https://wx1.vv1234.cn/2022/07/19/62d6c2690b371.png
  [5]: https://wx1.vv1234.cn/2022/07/19/62d6c38600d6a.png
  [6]: https://vv1234.cn/archives/750.html
  [7]: https://vv1234.cn/archives/750.html
  [8]: https://wx1.vv1234.cn/2022/07/19/62d6cae36db89.jpg