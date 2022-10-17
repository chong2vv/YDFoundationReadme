# ``YDAvoidCrashKit`` 防崩溃库使用

YDAvoidCrashKit主要借鉴了[@chenfanfang](https://github.com/chenfanfang)大神开源的 [AvoidCrash](https://github.com/chenfanfang/AvoidCrash)。由于AvoidCrash不再维护更新，同时鉴于实际业务开发中所使用的类逐渐增加，因此YDAvoidCrash在原AvoidCrash上重新开发。毕竟，一个已经发布到AppStore上的App，最忌讳的就是崩溃问题，相信作为开发者对于所产出项目的崩溃率要求都极为严格，因此YDAvoidCrash库就是为此存在。

相较于原库，YDAvoidCrash新增了以下功能及优化：

- 新增了其他系统类的防崩溃，目前约支持17个系统类（逐步迭代更新）;
- 支持回调设置，方便应用上报；
- 新增YDLogger日志采集系统，用以捕捉崩溃等日志（如操作日志、错误日志、请求日志等），同时YDLogger自带YDLoggerUI可以方便可视化查询日志；
- 新增卡顿检测组件YDMonitor辅助优化项目;
- 新增安全线程及数据操作组件YDSafeThread;
- 新增线程池管理;
- YDLogger日志是通过每次启动APP即可生成当前的日志文件，可以通过获取全部文件后进行压缩等形式上次服务端，同时可以下载后通过YDLoggerUI进行快速查看;
- 增加UI刷新防护，防止异步线程刷新UI导致的问题。
  
## 集成方式

按需安装pod库：

``` cocoapods
pod 'YDFoundation/YDAvoidCrashKit'
```

完整的YDAvoidCrashKit处自身和必要的[YDLogger](YDLogger.md)库、[YDSafeThread](YDSafeThread.md)库外还包含了[YDLoggerUI](YDFoundationReadMe/YDLogger.md#YDLoggerUI)库以方便查看日志，使用时引入头文件：

``` Objective-C
#import "YDAvoidCrashKit.h"
```

之后在AppDelegate的didFinishLaunchingWithOptions方法中的最初始位置添加如下代码，让YDAvoidCrash生效

``` Objective-C
- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
    //设置允许防崩溃类前缀
    [YDAvoidCrash setAvoidCrashEnableMethodPrefixList:@[@"NS",@"YD"]];
    
    //接收异常的回调处理，可以用来上报等
    [YDAvoidCrash setupBlock:^(NSException *exception, NSString *defaultToDo, BOOL upload) {
            
    }];
    //开启全部类拦截，同时开启日志收集（日志默认保存10天，可以在开启前通过[[YDLogService shared] clearLogWithDayTime:5]设置）
    [YDAvoidCrash becomeAllEffectiveWithLogger:YES];
    
    return YES;
}
```

如果不需要YDLoggerUI库查看日志则可选择使用**[YDAvoidCrash](YDAvoidCrash.md)**库:

``` cocoapods
pod 'YDFoundation/YDAvoidCrash'
```
