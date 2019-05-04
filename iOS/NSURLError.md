* NSURLErrorUnknown = -1,	未知的错误
* NSURLErrorCancelled = -999,	请求被取消
* NSURLErrorBadURL = -1000,	格式错误的URL阻止了URL请求的启动
* NSURLErrorTimedOut = -1001,	请求超时
* NSURLErrorUnsupportedURL = -1002,	不支持的URL Scheme
* NSURLErrorCannotFindHost = -1003,	无法解析URL的主机名
* NSURLErrorCannotConnectToHost = -1004,	连接host失败
* NSURLErrorNetworkConnectionLost = -1005,	连接过程中被中断
* NSURLErrorDNSLookupFailed = -1006,	无法通过DNS查找找到主机地址
* NSURLErrorHTTPTooManyRedirects = -1007,	重定向次数超过限制
* NSURLErrorResourceUnavailable = -1008,	无法获取所请求的资源
* NSURLErrorNotConnectedToInternet = -1009,	断网状态
* NSURLErrorRedirectToNonExistentLocation = -1010,	重定向到一个不存在的位置
* NSURLErrorBadServerResponse = -1011,	URL加载系统从服务器收到错误数据
* NSURLErrorUserCancelledAuthentication = -1012,	身份验证请求被用户取消
* NSURLErrorUserAuthenticationRequired = -1013,	访问资源需要身份验证
* NSURLErrorZeroByteResource = -1014,	服务器报告URL数据不为空，却未返回任何数据
* NSURLErrorCannotDecodeRawData = -1015,	响应数据无法解码为已知内容编码
* NSURLErrorCannotDecodeContentData = -1016,	请求数据存在未知内容编码
* NSURLErrorCannotParseResponse = -1017,	响应数据无法解析
* NSURLErrorAppTransportSecurityRequiresSecureConnection = -1022,	App Transport Security禁止连接，因为没有安全的网络连接 (info.plist 添加App Transport Security Settings 更改Allow Arbitrary Loads 属性为YES)
* NSURLErrorFileDoesNotExist = -1100,	请求的文件路径上文件不存在
* NSURLErrorFileIsDirectory = -1101,	请求的文件只是一个目录，而非文件
* NSURLErrorNoPermissionsToReadFile = -1102,	缺少权限无法读取文件
* NSURLErrorDataLengthExceedsMaximum = -1103,	资源数据的长度超过了允许的最大值

### SSL errors
* NSURLErrorSecureConnectionFailed = -1200,	安全连接失败
* NSURLErrorServerCertificateHasBadDate = -1201,	服务器证书过期
* NSURLErrorServerCertificateUntrusted = -1202,	不受信任的根服务器签名证书
* NSURLErrorServerCertificateHasUnknownRoot = -1203,	服务器证书没有任何根服务器签名
* NSURLErrorServerCertificateNotYetValid = -1204,	服务器证书还未生效
* NSURLErrorClientCertificateRejected = -1205,	服务器证书被拒绝
* NSURLErrorClientCertificateRequired = -1206,	需要客户端证书来验证SSL连接
* NSURLErrorCannotLoadFromNetwork = -2000,	请求只能加载缓存中的数据，无法加载网络数据

### Download and file I/O errors
* NSURLErrorCannotCreateFile = -3000,	下载操作无法创建文件
* NSURLErrorCannotOpenFile = -3001,	下载操作无法打开文件
* NSURLErrorCannotCloseFile = -3002,	下载操作无法关闭文件
* NSURLErrorCannotWriteToFile = -3003,	下载操作无法写文件
* NSURLErrorCannotRemoveFile = -3004,	下载操作无法删除文件
* NSURLErrorCannotMoveFile = -3005,	下载操作无法移动文件
* NSURLErrorDownloadDecodingFailedMidStream = -3006,	下载过程中下载任务无法解码编码文件
* NSURLErrorDownloadDecodingFailedToComplete = -3007,	下载后，下载任务无法解码编码文件

* NSURLErrorInternationalRoamingOff = -1018,	漫游时请求数据，但是漫游开关已关闭
* NSURLErrorCallIsActive = -1019,	EDGE、GPRS等网络不支持电话和流量同时进行，当正在通话过程中，请求失败错误码
* NSURLErrorDataNotAllowed = -1020,	蜂窝网络不允许连接。
* NSURLErrorRequestBodyStreamExhausted = -1021,	请求的body流被耗尽

* NSURLErrorBackgroundSessionRequiresSharedContainer = -995,	后台会话需要共享容器
* NSURLErrorBackgroundSessionInUseByAnotherProcess = -996,	应用或应用扩展程序尝试连接到已连接到进程的后台会话
* NSURLErrorBackgroundSessionWasDisconnected = -997	在处理后台数据任务时，应用程序将暂停或退出