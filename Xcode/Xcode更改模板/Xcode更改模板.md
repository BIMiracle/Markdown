##iOS自定义Xcode模板
[移除 NS_ASSUME_NONNULL_BEGIN  和 NS_ASSUME_NONNULL_END](https://stackoverflow.com/questions/53443330/prevent-xcode-from-creating-ns-assume-nonnull-begin-and-ns-assume-nonnull-end-on)

当前文件下的
___FILEBASENAME___.h
拖拽到 /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/Library/Xcode/Templates/File\ Templates/Source/Cocoa\ Touch\ Class.xctemplate/NSObjectObjective-C

目录下替换

或者手动编辑


~/资源库/Developer/Xcode/Templates/File Template/
如果没有手动创建 File Template 文件夹
把本目录下 My Class.xctemplate 文件夹添加进去
创建自己的Xcode模板


##更改Xcode注释
###以前:
/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/Library/Xcode/Templates/File Templates/Source/Cocoa Touch Class.xctemplate/NSObjectObjective-C

###现在:

快捷方法:

	导入IDETemplateMacros.plist 到 ~/Library/Developer/Xcode/UserData

前往目录
~/Library/Developer/Xcode/UserData

然后创建IDETemplateMacros.plist
FILEHEADER
String类型

value值里面填写
```
//
//  ___FILENAME___
//  ___PROJECTNAME___
//
//  Created by BIMiracle on ___DATE___.
//  ___COPYRIGHT___
//
```