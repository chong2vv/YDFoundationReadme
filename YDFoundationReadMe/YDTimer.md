# YDTimer 计时器库使用

YDTimer 是基于GCD封装的一个计时器组件。

## 集成方式

单独使用`YDTimer`库可以通过如下方式集成：

``` cocoapods
pod 'YDFoundation/YDTimer'
```

## 使用方式

``` Objective-C

// 引入头文件 YDTimer.h

/**
 *
 *  单例模式获取YDTimer
 *
 *  @return YDTimer计时器
 */
+(nullable instancetype)sharedTimer;

/**
 *
 *  开启计时器
 *
 *  @param timerName 计时器名称（通过名称可缓存在内存中）
 *  @param type      计时器类型（手动释放，则计时器缓存在内存中；或自动释放）
 *  @param queue     计时器执行的队列（如果是nil，则采用默认的队列）
 *  @param interval  计时器执行任务的时间间隔
 *  @param seconds   计时器精确度的包容度（单位：秒，为0时，最精确）
 *  @param handler   计时器到达时间点执行的任务
 */
-(void)scheduledTimerWithName:(nonnull NSString *)timerName
                    timerType:(YDTimerType)type
                        queue:(nullable dispatch_queue_t)queue
                 timeInterval:(NSTimeInterval)interval
              leewayInseconds:(NSTimeInterval)seconds
                      handler:(nullable YDTimerHandler)handler;

/**
 *
 *  注销计时器（手动释放timer所占内存，可以在dealloc中调用）
 *
 *  @param timerName 需注销的计时器的名字
 */
-(void)invalidateWithTimerName:(nonnull NSString *)timerName;

```
