# YDSafeThread 安全线程库使用

YDSafeThread主要提供两个功能，一个是SafeThreadPool所提供的安全线程池，以及封装的 `YDThreadSafeMutableSet`、`YDThreadSafeMutableArray`、`YDThreadSafeMutableDictionary` 用来在YDSafeThread 多线程下替换系统的：
 `NSMutableSet`、`NSMutableArray`、`NSMutableDictionary`来进行数据安全操作

## 集成方式

单独使用`YDSafeThread`线程库可以通过如下方式集成：

``` cocoapods
pod 'YDFoundation/YDSafeThread'
```

## 使用方式

YDSafeThreadPool:

``` Objective-C
+ (instancetype)shared;

/**
默认常驻线程执行任务
这里的block是尾随闭包,不用担心强引用
*/

- (BOOL)creatThread:(NSString *)threadName;

/**
创建一个常驻线程，并执行task任务
*/
- (BOOL)creatThread:(NSString *)threadName Task:(YDLoopTask) task;

/**
创建一个常驻线程，并执行task任务，有回调
*/
- (BOOL)creatThread:(NSString *)threadName Task:(YDLoopTask) task Complete:(YDCompleteTask)Complete;

/**
指定一个常驻线程任务执行
*/
- (BOOL)executeTask:(YDLoopTask)task withThreadName:(NSString *)threadName;

/**
指定一个常驻线程任务执行，  有回调
*/
- (BOOL)executeTask:(YDLoopTask)task withThreadName:(NSString *)threadName Complete:(YDCompleteTask)Complete;

/**
 销毁常驻线程
*/
- (BOOL)deleteThreadWithName:(NSString *)threadName;

/**
寻求一个空闲线程去执行任务  flase表示使用了gcd  哈哈
*/
- (BOOL)executeTaskToFreeThread:(YDLoopTask)task;
```

