# YDAuthorizationUtil 权限库使用

YDAuthorizationUtil是一个系统权限的请求库，方便快速查询、申请需要的权限（相机、相册等）

## 集成方式

单独使用`YDAuthorizationUtil`库可以通过如下方式集成：

``` cocoapods
pod 'YDFoundation/YDAuthorizationUtil'
```

## 使用方式

``` Objective-C
+ (EYDAuthorizationStatus)authorizedStatusWithType:(EYDAuthorization)authorizationType;

+ (BOOL)authorizedWithType:(EYDAuthorization)authorizationType;

+ (void)authorizeWithType:(EYDAuthorization)type completion:(void(^)(BOOL authorized))completion;

////拍照并存储相册 需要请求相机、相册两个权限
+ (void)authorizedForTakePhotoAndSaveWithCompletion:(void(^)(BOOL authorized))completion;

//录制视频 需要相机、相册、麦克风三个权限 其中只要有一个权限无法获取，都会导致录制出错
+ (void)authorizedForRecordVideoWithCompletion:(void(^)(BOOL authorized))completion;

//语音
+ (void)authorizedForRecordWithCompletion:(void(^)(BOOL authorized))completion;

//相册
+ (void)authorizedForPhotoWithCompletion:(void(^)(BOOL authorized))completion;

//相机
+ (void)authorizedForCameraWithCompletion:(void(^)(BOOL authorized))completion;

//相机，是否弹窗
+ (void)authorizedForCameraWithCompletion:(void(^)(BOOL authorized))completion needAlert:(BOOL)needAlert;

//去授权
+ (void)gotoSetting;
```
