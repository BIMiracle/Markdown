# 滚动式隐藏键盘 IQKeyboardManager模式下

手动滑动调用
![](./pictures/7751A4E6-CA02-40DA-85F2-E025FF0A1609.png)
IQKeyboard滑动调用![](./pictures/16AA9219-33C4-4687-BD58-CACB28289FD0.png)

```
- (void)scrollViewWillBeginDragging:(UIScrollView *)scrollView{
    [self.view endEditing:YES];
}
```