# ``YDFoundation``

> `写在前面的话`
> YDFoundation

## YDFoundation 组件库介绍

YDFoundation 主要由以下组件库组成：

### 防崩溃组件

- [YDAvoidCrashKit](YDFoundation/YDAvoidCrash.md)
  - [YDAvoidCrash](YDFoundation/YDAvoidCrash.md)
  - YDSafeThread
  - YDLogger
  - YDLoggerUI
  
### 日志组件

- [YDLogger](YDFoundation/YDLogger.md)
- [YDLoggerUI](YDFoundation/YDLogger.md)
  -[YDLogger](YDFoundation/YDLogger.md)

### 基本工具组件

- YDUtilKit
  - YDFuncKit
  - YDBaseUI
  - YDUIKit
  - YDTools
- YDImageService
- YDNetworkManager
- YDJPush
- YDBlockKit
- YDAuthorizationUtil
- YDEmptyView
- YDPreLoader
- YDSVProgressHUD
- YDFileManager
- YDMonitor
- YDAlertAction
- YDMediato
- YDClearCacheService
- YDRouter
- YDWebp

相较于原库，YDAvoidCrash新增了以下功能及优化：

## 安装及使用方式

### 使用CocoaPods导入

使用时可以全量导入

``` cocoapods
pod 'YDFoundation'
```

也可以按需导入避免冗余组件过多，例如：

``` cocoapods
pod 'YDFoundation/YDSafeThread'
```

## 更新

#### v0.1.2

1. 新增YDTimer计时器

## 写在最后的话

一个人的精力是有限的，如果您在YDFoundation组件使用过程中发现BUG或者有更好的解决方法欢迎你能issue，我将万分感谢！
