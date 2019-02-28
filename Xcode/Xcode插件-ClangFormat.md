##1. 系统设置键盘快捷键
Format File in Focus ⇧⌘A  
Format Selected Text ⌥⇧⌘A


##2. 工程下创建.clang-format文件
```
# 基于LLVM样式
BasedOnStyle: LLVM

# 连续的赋值操作按=对齐，看自己喜好打开。
AlignConsecutiveAssignments: true

# 把连续行的变量名对齐，看自己喜好打开。
AlignConsecutiveDeclarations: true

# 对齐尾部注释
AlignTrailingComments: true

# 每行字符的宽度不限制
ColumnLimit: 0

# 缩进宽度设置为4
IndentWidth: 4

# switch的case缩进宽度
IndentCaseLabels: true

# 不保留block里面开始的空行们
#KeepEmptyLinesAtTheStartOfBlocks: false

# 最多只能有连续1行空行
MaxEmptyLinesToKeep: 3

# OC的block里面的缩进宽度，默认为4。
ObjCBlockIndentWidth: 4

# 在@property后加空格
ObjCSpaceAfterProperty: true

# 尾部//注释前面加1个空格
SpacesBeforeTrailingComments: 1

# 在<后边和>前边插入空格
SpacesInAngles: false

# OC里面，是否在@property后加空格。默认为false
ObjCSpaceAfterProperty: true

# 允许一行的if
AllowShortIfStatementsOnASingleLine: true
```

##3. 让一段代码不受格式化影响
// clang-format off

// clang-format on