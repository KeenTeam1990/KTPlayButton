# KTPlayButton


### 爱奇艺播放、暂停按钮动画效果

![image](https://github.com/KeenTeam1990/KTPlayButton/blob/master/GIF/1.gif)

### 优酷播放、暂停按钮动画效果

![image](https://github.com/KeenTeam1990/KTPlayButton/blob/master/GIF/2.gif)

### 实现原理

实现原理是利用贝塞尔曲线和CAShapeLayer绘制出三角、圆弧、直线，然后通过核心动画实现的动态效果。

### 使用方法

* KTPlayButton 是继承UIButton的，只是创建方式和UIButton不同，其他的使用方法均一致。
* 创建方法
```objc
_iQiYiPlayButton = [[iQiYiPlayButton alloc] initWithFrame:CGRectMake(0, 0, 60, 60) state:iQiYiPlayButtonStatePlay];
```
* 唯一属性
```objc
/**
 通过setter方式控制按钮动画
 设置KTPlayButtonStatePlay显示播放按钮
 设置KTPlayButtonStatePause显示暂停按钮
 */
@property (nonatomic, assign) KTPlayButtonState buttonState;
```
* 切换状态方法
```objc
- (void)iQiYiPlayMethod {
    //通过判断当前状态 切换显示状态
    if (_iQiYiPlayButton.buttonState == iQiYiPlayButtonStatePause) {
        _iQiYiPlayButton.buttonState = iQiYiPlayButtonStatePlay;
    }else {
        _iQiYiPlayButton.buttonState = iQiYiPlayButtonStatePause;
    }
}

