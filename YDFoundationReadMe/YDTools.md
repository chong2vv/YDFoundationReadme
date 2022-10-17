# YDTools 工具库使用

YDTools是一个简单的小工具组件库，主要包含本地发号器生成工具、堆栈工具以及视频工具等组成

## 集成方式

单独使用`YDTools`工具库可以通过如下方式集成：

``` cocoapods
pod 'YDFoundation/YDTools'
```

## 使用方式

``` Objective-C

// 发号器
#import <YDFoundation/YDNumberSender.h>
// 获取本地生成id
+ (NSString *)getSenderNumber;
```

``` Objective-C
// 堆栈
#import <YDFoundation/YDStack.h>
/** 入栈 @param obj 指定入栈对象 */
- (void)push:(id)obj;

/** 出栈 */
- (id)popObj;

/** 是否为空 */
- (BOOL)isEmpty;

/** 栈的长度 */
- (NSInteger)stackLength;

/** 从栈底开始遍历 @param block 回调遍历的结果 */
-(void)enumerateObjectsFromBottom:(StackBlock)block;

/** 从顶部开始遍历 */
-(void)enumerateObjectsFromtop:(StackBlock)block;

/** 所有元素出栈，一边出栈一边返回元素 */
-(void)enumerateObjectsPopStack:(StackBlock)block;

/** 清空 */
-(void)removeAllObjects;

/** 返回栈顶元素 */
-(id)topObj;
```

``` Objective-C
// 视频工具
#import <YDFoundation/YDVideoTools.h>
//获取封面图
+ (UIImage*) thumbnailImageForVideo:(NSURL *)videoURL atTime:(NSTimeInterval)time;
//获取视频大小
+ (CGFloat) getFileSize:(NSString *)path;
//获取视频大小
+ (CGFloat) getVideoLength:(NSURL *)URL;

```
