# 重新签名Xcode

sudo codesign -f -s XcodeSigner /Applications/Xcode.app

# Xcode重新加载插件

find ~/Library/Application\ Support/Developer/Shared/Xcode/Plug-ins -name Info.plist -maxdepth 3 | xargs -I{} defaults write {} DVTPlugInCompatibilityUUIDs -array-add `defaults read /Applications/Xcode_d.app/Contents/Info DVTPlugInCompatibilityUUID`