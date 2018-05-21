Specs 国内镜像

 1. 清华大学镜像
 ```
https://mirrors.tuna.tsinghua.edu.cn/git/CocoaPods/Specs.git
```

 2. 上海大学镜像
```
https://mirrors.shu.edu.cn/CocoaPods (仅HTTP/HTTPS访问，不支持git拉取)
https://mirrors.shu.edu.cn/mgit/Specs (仅git访问)
https://git.shuosc.org/CocoaPods/Specs (均支持)
```

 3. COCOAPODS SPECS 中国区镜像
```
git://cocoapodscn.com/Specs.git
```

使用方法
----
对于旧版的 CocoaPods 可以使用如下方法使用国内的的镜像(以清华的镜像为例)：
```objC
pod repo remove master
pod repo add master https://mirrors.tuna.tsinghua.edu.cn/git/CocoaPods/Specs.git
pod repo update
```
----
新版的 CocoaPods 不允许用pod repo add直接添加master库了，但是依然可以：
```
cd ~/.cocoapods/repos 
pod repo remove master
git clone https://mirrors.tuna.tsinghua.edu.cn/git/CocoaPods/Specs.git master
```

----
最后进入自己的工程，在自己工程的podFile第一行加上：
> source 'https://mirrors.tuna.tsinghua.edu.cn/git/CocoaPods/Specs.git'

重置为官方上游
```
cd ~/.cocoapods/repos
pod repo remove master
git clone https://github.com/CocoaPods/Specs master

# 最后进入自己的工程，在自己工程的podFile第一行加上
sources 'https://github.com/CocoaPods/Specs'
```


