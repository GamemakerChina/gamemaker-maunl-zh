# Game Maker 文档翻译器



GameMaker文档翻译器,是为了方便的翻译文档而根据文档本身特别订制的工具,目的是解决一些痛点

具有以下特点

- 所见即所得,打开文档,对着你想翻译的元素点击鼠标右键就可以很方便的进行翻译,(讨厌的CAT)
- 基于字典进行翻译,不依赖于特定的文档版本,也不会修改文档本身,你可以很方便的替换文档进行升级
- 内嵌标签的简易化处理,将{}做为替代符,还可以使用数字重新排序,例如{2}{3}{0}{1},用来解决不同语言中的语序问题
- 因为字典是json文件,适合git协作(但仍需偶尔处理冲突)
- 一键编译字典到静态文件中,使其回到 GameMaker F1 (因为有跨域问题)

该工具基于webview2开发,据我所知,win10较高版本皆内置该环境,我讨厌生成electron那种动辄100M+的东西

## 你来自中国

请在 `这里` 下载汉化文档

如果你发现了翻译疏漏,或漏翻等问题,欢迎来 `这里` 反馈

如果你也想贡献自己的一份力,还是来 `这里`

### 汉化组名单

- yunzl
- 红色激情
- LiarOnce

## 如何开始

-----

### 1.克隆项目

https://github.com/GamemakerChina/gamemaker-maunl-zh.git

克隆该仓库,或派生或下载zip随你

### 2.准备要翻译的文档

解压文档压缩包到  `GMS2-Robohelp-en`  目录下

如果你有安装 `GameMaker` 那么你可以在以下目录找到文档压缩包

````
C:\ProgramData\GameMakerStudio2\Manual\GMS2-Robohelp-en.zip
C:\ProgramData\GameMakerStudio2-Beta\Manual\GMS2-Robohelp-en.zip
C:\ProgramData\GameMaker\Manual\GMS2-Robohelp-en.zip
C:\ProgramData\GameMaker-LTS\Manual\GMS2-Robohelp-en.zip
````

如果你没有安装,那你可以从rss订阅链接进行下载(为什么)
https://gms.yoyogames.com/update-manual.rss
https://gms.yoyogames.com/update-manual-beta.rss

### 3.设置group信息和申请获得翻译接口token

首先你需要打开 `setting.struct` 文件,修改group值到你们的语言缩写,它起到设置路径的作用



我在软件里集成了两个接口供我们组员使用,`彩云`与`languagex`,你需要打开`token.struct`设置token

下面是这两个接口的申请网址

https://dashboard.caiyunapp.com/user/sign_in/

http://app.languagex.com/ (注意,该接口的token需要从cookie获取,具体请按F12)



如果你所在的地区使用十分缓慢,建议在前端实现类似google之类的翻译接口

前端主要逻辑代码在`patch/main.js`,代码很简单,实现额外功能十分简单

### 4.开始翻译

打开 `GameMakerManualTranslator.exe` 对着想要翻译的元素右键即可

### 5,编译导出

打开 `GameMakerManualTranslatorBuild.exe` 会将json注入到文件生成在`build`目录中

你可以将文件替换到原文档并压缩成zip替换`GameMaker`原文档zip文件,具体目录请看上面

## 正式介绍



## 许可协议

------

我能支配的那部分骄傲的使用 *WTFPL*(Do What The Fuck You Want To Public License)



## 
