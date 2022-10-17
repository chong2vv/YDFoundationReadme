# YDUIKit UI工具库使用

YDUIKit是针对系统UIKit库通过分类方式添加的一个补充方法库，在使用上通过引用对应的头文件即可直接使用对应方法。

## 集成方式

单独使用`YDUIKit`UI工具库可以通过如下方式集成：

``` cocoapods
pod 'YDFoundation/YDUIKit'
```

## 使用方式

``` Objective-C

// 引入头文件YDUIKitCategory.h即可使用，具体方法可查看对应注释
#import <YDFoundation/YDUIKitCategory.h>

```

具体包含的扩展：

``` Objective-C
#import "UIImage+YDCommon.h"
#import "UIView+YDCommon.h"
#import "UITextField+YDCommon.h"
#import "UITableView+YDCommon.h"
#import "UIScrollView+YDCommon.h"
#import "UIControl+YDCommon.h"
#import "UIDevice+YDCommon.h"
#import "UIColor+YDCommon.h"
#import "UIWindow+YDScreenShot.h"
#import "UIView+YDWhenTappedBlocks.h"
#import "UIView+YDQRCode.h"
#import "UITextView+YDPlaceholder.h"
#import "NSString+YDLabelHeigh.h"
#import "UILabel+YDAddtion.h"
#import "UITapGestureRecognizer+YDAddtion.h"
```
