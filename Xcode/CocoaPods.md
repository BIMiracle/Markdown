##Cocoapods基本框架
```
platform :ios, '9.0'

target 'IntelligentMedical' do
  use_frameworks!
  inhibit_all_warnings!

  pod 'Alamofire', '~> 4.0'
  pod 'SwiftyJSON'
  pod 'SDWebImage', '~> 4.0'
  pod 'IQKeyboardManagerSwift'
  pod 'MBProgressHUD', '~> 1.1.0'
  pod 'MJRefresh'
  pod 'MJExtension'
  pod 'Segmentio', '~> 3.0'
  pod 'Charts', '3.1.1'
  pod 'SnapKit'
  
  pod 'mob_sharesdk'
  pod 'mob_sharesdk/ShareSDKUI'
  pod 'mob_sharesdk/ShareSDKPlatforms/QQ'
  pod 'mob_sharesdk/ShareSDKPlatforms/SinaWeibo'
  pod 'mob_sharesdk/ShareSDKPlatforms/WeChat'
  
  pod 'Reveal-SDK','17',:configurations => ['Debug']

end
```
