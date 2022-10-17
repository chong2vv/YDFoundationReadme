# ``YDFoundation``

> `写在前面的话`
> 我们在开发一个新项目时，除业务需求外大多数时候可能都是在做一些重复性的组件开发工作，由此根据这些年的开发总结制作了这套YDFoundation的组件库，以便于快速集成开发，避免重复造轮子。
> 在YDFoundation库之前其实内部所包含的组件已经单独做过开源，之所以现在统合到YDFoundation库一方面是进一步方便快速集成，只需要执行``pod YDFoundation``即可，另一方面也是作者为了方便维护（重点），毕竟统一管理可以大幅度节省维护成本。所以YDFoundation所包含的组件库不再单独维护，会统一放到YDFoundation下进行维护。
> 不过实际项目中YDFoundation中所包含的组件可能很多都用不到，所以为了防止冗余度高，还是建议按需引用。
> 最后，YDFoundation可能会存在或多或少的一些问题，您在使用中如果发现任何问题欢迎您能issue，或通过邮件<chong2vv@gmail.com>联系我，我将万分感谢！

## YDFoundation 组件库介绍

YDFoundation 主要由以下组件库组成：

### 线程组件

- YDSafeThread
- YDTimer

### 日志组件

- [YDLogger](YDFoundationReadMe/YDLogger.md)
- [YDLoggerUI](YDFoundationReadMe/YDLogger.md#YDLoggerUI)
  -[YDLogger](YDFoundationReadMe/YDLogger.md)

### 防崩溃组件

- [YDAvoidCrashKit](YDFoundationReadMe/YDAvoidCrash.md)
  - [YDAvoidCrash](YDFoundationReadMe/YDAvoidCrash.md)
  - [YDSafeThread](YDFoundationReadMe/YDSafeThread.md)
  - [YDLogger](YDFoundationReadMe/YDLogger.md)
  - [YDLoggerUI](YDFoundationReadMe/YDLogger.md#YDLoggerUI)

### 基本工具组件

- [YDUtilKit](YDFoundationReadMe/YDUtilKit.md)
  - [YDFuncKit](YDFoundationReadMe/YDFuncKit.md)
  - [YDBaseUI](YDFoundationReadMe/YDBaseUI.md)
  - [YDUIKit](YDFoundationReadMe/YDUIKit.md)
  - [YDTools](YDFoundationReadMe/YDTools.md)
- [YDImageService](YDFoundationReadMe/YDImageService.md)
- [YDNetworkManager](YDFoundationReadMe/YDNetworkManager.md)
- [YDJPush](YDFoundationReadMe/YDJPush.md)
- [YDBlockKit](YDFoundationReadMe/YDBlockKit.md)
- [YDAuthorizationUtil](YDFoundationReadMe/YDAuthorizationUtil.md)
- [YDEmptyView](YDFoundationReadMe/YDEmptyView.md)
- [YDPreLoader](YDFoundationReadMe/YDPreLoader.md)
- [YDSVProgressHUD](YDFoundationReadMe/YDSVProgressHUD.md)
- [YDFileManager](YDFoundationReadMe/YDFileManager.md)
- [YDMonitor](YDFoundationReadMe/YDMonitor.md)
- [YDAlertAction](YDFoundationReadMe/YDAlertAction.md)
- [YDMediato](YDFoundationReadMe/YDMediator.md)
- [YDClearCacheService](YDFoundationReadMe/YDClearCacheService.md)
- [YDRouter](YDFoundationReadMe/YDRouter.md)
- [YDWebp](YDFoundationReadMe/YDWebp.md)

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
