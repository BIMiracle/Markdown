# 通过'MJExtension'修改模型,当类型为NSSTring时,如果没有数据返回空字符串

修改NSObject+MJKeyValue.m
112行

```
// 如果没有值，就直接返回
            if (!value || value == [NSNull null]) return;
```
改为

```
// 如果没有值，就直接返回
            if (!value || value == [NSNull null]) {
                if ([property.type.code isEqualToString:@"NSString"]) {
                    [property setValue:@"" forObject:self];
                }
                return;
            }
```