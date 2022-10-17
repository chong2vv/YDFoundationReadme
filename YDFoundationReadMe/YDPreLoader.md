# YDPreLoader 视频预加载库使用

`YDPreLoader`是对[KTVHTTPCache](https://github.com/ChangbaDevs/KTVHTTPCache)库的一个封装库，KTVHTTPCache是一个功能强大的媒体缓存框架，它可以缓存HTTP请求，非常适合媒体资源，具体用法可查看官方文档。YDPreLoader针对KTVHTTPCache的封装主要是方便进行资源的批量预加载，同时支持设置预下载的百分比。

注意：由于KTVHTTPCache目前不支持m3u8等格式，所以本库目前也暂不支持，且KTVHTTPCache当前也不在维护更新，所以选择该库时需要谨慎使用。

## 集成方式

单独使用`YDPreLoader`预加载库可以通过如下方式集成：

``` cocoapods
pod 'YDFoundation/YDPreLoader'
```

## 使用方式

主要方法：

``` Objective-C
//开启本地代理
+ (void)startProxy;

//设置下载百分比
+ (void)setPrecentCacheValue:(CGFloat) value;

//预下载
+ (void)preDownLoadData:(NSArray <NSString *> *) preloadArr delegate:(id<YDPreLoaderDelegate>) delegate;

//取消所有下载任务
+ (void)cancelAllDownLoad;

```
