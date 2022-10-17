# YDSVProgressHUD 加载组件库使用

YDSVProgressHUD是对SVProgressHUD的二次封装，相较原SVProgressHUD库支持Lottie动画，以及新增UIViewController分类方便快速调用

## 集成方式

单独使用`YDSVProgressHUD`库可以通过如下方式集成：

``` cocoapods
pod 'YDFoundation/YDSVProgressHUD'
```

## 使用方式

``` Objective-C
// 引用YDProgressHUD.h 即可使用相关方法
// YDSVProgressHUD相关配置可以在工程中通过对YDProgressHUDConfig进行分类覆盖的方式进行自定义配置，如无配置则使用默认。
import <YDFoundation/YDProgressHUD.h>

// UIViewController+Toast.h
// 显示文本提示
- (void)showText:(NSString *)aText;


```
