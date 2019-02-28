##1. 当没有左右箭头时,在控件共同的父类view添加class

```objc
IQPreviousNextView
```

##2. 如果发现顶部移动距离不对
```objc
self.navigationController.navigationBar.translucent = YES;
```