~/资源库/Application Support/Developer/Shared/Xcode/Plug-ins/

~/Library/Developer/Xcode/Plug-ins


defaults read /Applications/Xcode.app/Contents/Info DVTPlugInCompatibilityUUID



find ~/Library/Application\ Support/Developer/Shared/Xcode/Plug-ins -name Info.plist -maxdepth 3 | xargs -I{} defaults write {} DVTPlugInCompatibilityUUIDs -array-add `defaults read /Applications/Xcode_d.app/Contents/Info DVTPlugInCompatibilityUUID`