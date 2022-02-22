## adb命令

查看所有禁用列表

```shell
adb shell pm list packages -d
```



禁用服务

```shell
adb shell pm disable-user com.xxx.xxx
```



启用服务

```shell
adb shell pm enable com.xxx.xxx
```



查看开放的端口

```
adb shell ss -tlpn
```



查看设备安装包名

```
adb shell pm list packages
```



点击app获取包名

```
adb shell am monitor
```



从日志中过滤出当前打开的App

```
adb logcat | grep Displayed
```



日志导出

```
adb logcat>/Users/mac/Downloads/log.txt
```



http://c.tieba.baidu.com/p/6349791520



当前vivo禁用包名

```
package:com.bbk.updater
package:com.vivo.upnpserver
package:com.bbk.cloud
package:com.bbk.theme
package:com.bbk.iqoo.feedback
package:com.vlife.vivo.wallpaper
package:com.vivo.daemonService // 手电筒
package:com.vivo.Tips
package:com.vivo.game
package:com.bbk.iqoo.logsystem
package:com.google.android.syncadapters.contacts // google联系人同步无法禁止启用
package:com.android.bbklog
package:com.vivo.magazine
package:com.android.VideoPlayer
package:com.vivo.wallet
package:com.vivo.upslide // 侧滑返回
package:com.vivo.email
package:com.vivo.gamewatch
package:com.vivo.space
package:com.vivo.aiservice
package:com.vivo.favorite
package:com.vivo.browser
package:com.bbk.account
package:com.bbk.appstore
package:com.vivo.gametrain
```

