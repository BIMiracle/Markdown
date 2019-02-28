##iOS自定义Xcode模板
###以前:
/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/Library/Xcode/Templates/File Templates/Source/Cocoa Touch Class.xctemplate/NSObjectObjective-C

###现在:

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