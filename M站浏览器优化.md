## 网络加载类
- 首屏数据请求提前，避免 JavaScript 文件加载后才请求数据
- 首屏加载和按需加载，非首屏内容滚动加载，保证首屏内容最小化
    一般推荐移动端页面首屏数据展示延时最长不超过3秒。首屏所有资源大小不超过1014KB，即大约不超过1MB。
- 模块化资源并行加载
    在移动端资源加载中，尽量保证JavaScript资源并行加载，主要指的是模块化JavaScript资源的异步加载，例如AMD的异步模块，使用并行的加载方式能够缩短多个文件资源的加载时间。
- inline 首屏必须的 css 和 js
- meta dns prefetch设置DNS预解析
    设置文件资源的DNS预解析，让浏览器提前解析获取静态资源的主机IP，避免等到请求时才发起DNS解析请求。通常在移动端HTML中可以采用如下方式完成。
```
<!-- cdn域名预解析 -->
<meta http-equiv="x-dns-prefetch-control" content="on">
<link rel="dns-prefetch" href="//cdn.domain.com">
```

