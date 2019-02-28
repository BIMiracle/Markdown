#UITableView

##1. 清除多余的分割线

```objc
self.tableView.tableFooterView = [[UIView alloc]init];
```

##2. UITableView的分割线顶格显示

```objc
/**
*  分割线顶头
*/
-(void)viewDidLayoutSubviews
{
  if ([self.tableView respondsToSelector:@selector(setSeparatorInset:)]) {
      [self.tableView setSeparatorInset:UIEdgeInsetsMake(0,0,0,0)];
  }

  if ([self.tableView respondsToSelector:@selector(setLayoutMargins:)]) {
      [self.tableView setLayoutMargins:UIEdgeInsetsMake(0,0,0,0)];
  }
}
-(void)tableView:(UITableView *)tableView willDisplayCell:(UITableViewCell *)cell forRowAtIndexPath:(NSIndexPath *)indexPath
{
  if ([cell respondsToSelector:@selector(setSeparatorInset:)]) {
      [cell setSeparatorInset:UIEdgeInsetsZero];
  }
  if ([cell respondsToSelector:@selector(setLayoutMargins:)]) {
      [cell setLayoutMargins:UIEdgeInsetsZero];
  }
}
```

## 3.UITableViewCell的动态高度
```objc
self.tableView.estimatedRowHeight = 44.0;
self.tableView.rowHeight = UITableViewAutomaticDimension;
```
配合xib自动布局使用

