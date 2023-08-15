# 🎉 哔哩哔哩漫画下载器 💖

![GitHub Pipenv locked Python version](https://img.shields.io/github/pipenv/locked/python-version/Zeal-L/BiliBili-Manga-Downloader)
![GitHub top language](https://img.shields.io/github/languages/top/Zeal-L/BiliBili-Manga-Downloader)
![GitHub Lines of code](https://img.shields.io/tokei/lines/github/Zeal-L/BiliBili-Manga-Downloader)
![GitHub repo size](https://img.shields.io/github/repo-size/Zeal-L/BiliBili-Manga-Downloader)
![GitHub - License](https://img.shields.io/github/license/Zeal-L/BiliBili-Manga-Downloader)

![platform](https://img.shields.io/badge/platform-windows10-blue)
![GitHub commit activity](https://img.shields.io/github/commit-activity/y/Zeal-L/BiliBili-Manga-Downloader)
![GitHub last commit](https://img.shields.io/github/last-commit/Zeal-L/BiliBili-Manga-Downloader)
![GitHub all releases - Download](https://img.shields.io/github/downloads/Zeal-L/BiliBili-Manga-Downloader/total)


## 💬 简介
**由于作者某天实在是受不了B漫网页版的观看体验 ~~(时而混入漫画中的广告，无法便捷快速的放大图片，进度栏作死一样的反复横跳挡视线等等...)~~，再加上作者的仓鼠属性 😛**

**因此 将将将~ 🎉 一个好用的哔哩哔哩漫画下载器就此诞生！**

## :sparkles: 主要功能 / 特性
- **已打包成单个可执行文件，双击即用！**
- **易操作的图形界面！~~(不用再费劲的部署环境跑命令行)~~**
- **无需漫画ID，可直接关键词搜索漫画！并附带搜索词高亮！**
- **支持B站和BiliPlus两种解析方式！**
- **可配置的多线程下载，速度拉满！**
- **实现了应对网络波动等情况的异常重试，以及应用了指数级退让来避免在短时间大量重试被拉黑名单**
- **丰富的漫画详情信息，本地漫画管理功能，一键检查更新！**
- **通过正则匹配过滤重复的章节名称内容，以及过滤非法字符！**
- **提供多种可选的保存格式：**
  - PDF
  - 7z压缩包
  - 文件夹-图片形式
- **贴心的在保存文件属性中附加了漫画名，章节名以及作者信息，以免单章传播时不知道来源**
- **可视化的多任务下载进度条以及下载速度和剩余时间预计信息！**
- **漫画保存地址和用户Cookie等用户设置的本地缓存，不需要每次重启软件就重新输入！**
- **丰富的错误信息日志，可按照日期滚动储存，不会浪费内存**
- **一键清空用户数据，妈妈再也不用担心我删不干净软件了！~~(bushi)~~**
- **多种主题选择**

## 📸 相关截图
**使用哔站解析**
<div align=center>
<img src="https://github.com/Zeal-L/BiliBili-Manga-Downloader/assets/72005386/39f4e66f-50f1-410b-8761-971eeb9cf30e" width=90%>
</div>

**使用BiliPlus解析**
<div align=center>
<img src="https://github.com/Zeal-L/BiliBili-Manga-Downloader/assets/72005386/4686f08b-2e88-4070-8d90-661c0a4392b6" width=90%>
</div>

**下载进度界面**
<div align=center>
<img src="https://github.com/Zeal-L/BiliBili-Manga-Downloader/assets/72005386/9c99e3c8-4283-4b0d-a5cd-23dab08b78b6" width=90%>
</div>

## 📝 使用指南
- **本软件有两种下载解析方法：**
  - **B站解析**
    - 只能下载免费章节和用户已解锁的章节
    - **首先获得你的Cookie**
      - 方法一 - B漫手机客户端扫码登入
      - 方法二 - 手动获取Cookie:
      1. 以谷歌浏览器为例，打开B漫首页并且登入
      2. 点击 `F12` 打开开发者工具
      3. 点击 `应用` 标签
      4. 在边栏中找到 `Cookie` ，点击 `https://manga.bilibili.com`
      5. 在右侧的详情中找到 `SESSDATA`，复制 `值` 粘贴到程序设置选项中的 `我的Cookie` ，回车确认
      6. 如果提示 `Cookie有效！` 那么就成功了！
      7. 否则请再次确认上述步骤，检查是否正确复制内容不含空格，还有疑问的话欢迎联系作者或提 `Issues`
  - **BiliPlus解析**
    - 利用 [biliplus](https://www.biliplus.com/) 提供的 [ComicWebReader](https://www.biliplus.com/manga/) 在线漫画平台的api来尝试获取更多的可下载章节
    - 该网站现有 4w+ 已关联 `Bilibili` 帐号的访客，也就是说很有概率你想看的漫画已经有人购买了，所以可以尝试一下
    - **特别提示: 毕竟是要提供 Cookie 给第三方网站托管，因此可能会有潜在的安全风险。敏感人群请不要使用自己主账号的 Cookie**
    - `BiliPlus` 的 `Cookie` 获取方法跟上述一致，在 [ComicWebReader](https://www.biliplus.com/manga/) 登入后在开发者工具中找到 `access_key` 粘贴到程序设置选项中的 `BiliPlus Cookie` 即可

- **兼容性：目前只在64位的Winodw 10上测试通过，不过其他>=windows 10的版本应该都能运行，发现问题的欢迎提Issues**
- **搜索 / 选择章节 / 下载 的功能介绍我想已经不言而喻了，这就是图形化界面的好处！**
- **值得注意的是：本软件不支持断点续传和下载任务缓存的功能 ~~(毕竟一章漫画太小了，好像也没什么必要，断了不如重下)~~，所以请确保不要在下载中途关闭！**
  - 如果程序意外中断，可以选择把下了一半的文件都删掉(一般在目标漫画文件夹的根目录下)，重新下载
- **程序缓存和日志历史文件存在 `C:\Users\AppData\Roaming\BiliBili-Manga-Downloader\` 目录下，可以通过"清空用户数据"功能一键删除**
- **如果想用"本地库存"功能，需要注意的是：下载好的漫画章节名以及保存的 `元数据.json` 都不能更改，否则将会无法正确读取漫画数据**
- **🔥 下面我要隆重的推荐一款搭配本软件使用的漫画浏览器 ~~(可以说就是为了这点儿醋 我才包的这顿饺子)~~**
  - <div align=center><img src="https://user-images.githubusercontent.com/72005386/222974497-18b568e7-5b2e-416f-8d14-22ec68323570.png" width=100%></div>
  - **NeeView** 是一款 Windows 下开源的图片浏览器，其特色是可以像翻书一样同时浏览两张照片，还支持压缩包看图、鼠标手势、触摸操作、多线程和超前查看、支持 PDF / 视频。 原生支持中文
  - 下载地址: [Microsoft Store](https://www.microsoft.com/en-us/p/neeview/9p24z53hc1jr)
  - 上面是官方介绍，要我说优势就下面几点
    - 自动切页，双页浏览
    - 左右或者右左的阅读顺序一键切换
    - 鼠标左键长摁放大，自由移动放大聚焦点，滚轮调整放大倍数， 这点超爽的好嘛，吊打所有网页浏览体验 ~~(尤其是某些地方需要放大好好品鉴的时候，嗯嗯，我说的就是背景人物！)~~
    - 优秀的资源浏览器以及简明的操作逻辑和界面
    - 总之是电脑端看漫画的不二之选~
  - 唯一的缺点好像就是对条漫不太支持，也有可能是我没找到选项，有知道的小伙伴可以联系我，谢啦~

## 💡 TODO List ~~(在可见的未来...)~~
- **PS: 也欢迎小伙伴们多多的在Issues里提意见，不管是Bug还是操作逻辑，界面优化等等作者统统笑纳~**
  - 🟦 缓存更多资源，减少网络请求
  - 🟦 添加一个启动程序加载进度条
  - 🟦 添加我的追漫界面，以及追漫功能
  - 🟦 对于有特典的漫画，提供特典下载界面
- **已解决**
  - ✅ ~~添加二维码扫码登入功能~~
  - ✅ ~~添加不同的界面主题~~
  - ✅ ~~添加检测cookie无效或者过期功能，并且弹窗~~
  - ✅ ~~鼠标移动到漫画封面改变鼠标图标，提示用户可以点击跳转~~
  - ✅ ~~一键检查软件更新功能~~
  - ✅ ~~除pdf以外添加不同的保存选项如 7z 或者 基本的文件夹图片~~
  - ✅ ~~启动程序时多线程加载本地库存，避免用户等待太久~~
  - ✅ ~~给打包好的程序添加版本号版权等属性信息~~

## 🏗️ 本地构建 / 编译
- **首先确保你安装了 Python >= 3.11 和 git**
- **本项目使用了 pipenv 依靠虚拟环境进行依赖项管理，所以不必担心影响自己的本地环境**
- **作者已经贴心的帮后来者们准备好了两个集成脚本~**
- **接下来的操作都在项目的根目录运行命令行指令**
- **构建项目**
  1. 执行 `git clone https://github.com/Zeal-L/BiliBili-Manga-Downloader.git`
  2. 执行 `cd BiliBili-Manga-Downloader/`
  3. 执行 `sh setup.sh` 等待项目构建完成
  4. 执行 `pipenv shell` 进入虚拟环境
  5. 执行 `python3 app.py` 即可运行程序
- **打包编译**
  1. 执行 `sh build.sh` 等待项目打包完成
  2. 这一步可能会花费一定时间，中途需要手动确认安全漏洞检查
  2. 打包好的程序会被移动到项目的根目录 "哔哩哔哩漫画下载器.exe"
- **彻底清除项目 ~~(删库跑路)~~**
  1. 执行 `pipenv --rm `
  2. 执行 `cd .. && rm -rf BiliBili-Manga-Downloader/`

## 🔨 PR 格式
- 遵循项目已有代码的 python doc 格式
- 明确的注释信息
- 正确的函数类型声明
- 在可能出错的IO/网络申请等部分都加上retry装饰器
- 在需要的地方写入logger日志，格式参考已有代码
- 更改 / 新增 的功能说明，理由
- 是否 更改 / 新增 依赖项

## ⚰️ 更新记录

![Alt](https://repobeats.axiom.co/api/embed/cc62fded834eb06fc9b30cf7ffd54eeb53d700fc.svg "Repobeats analytics image")

### v1.3.0 - *2022-08-11*
- 新增功能:
  - 二维码登入
  - 利用 [biliplus](https://www.biliplus.com/) 提供的 [ComicWebReader](https://www.biliplus.com/manga/) 在线漫画平台的api来尝试获取未解锁的漫画章节
- 优化配置:
  - 移除保存文件夹名里的漫画ID信息；元数据现在默认保存，并且以此来初始化我的库存
  - 老用户需要重新下载一章漫画，然后把以前下载好的移动到新文件夹中
- 修复bug:
  - 修复个别`png`保存为`jpg`的情况
  - 修复`BiliPlus Cookie`检测可能出现的隐藏`bug` ([#61][i61])
  - 修复`BiliPlus`可以看未解锁的漫画章节，软件无法下载 ([#52][i52])

[i52]: https://github.com/Zeal-L/BiliBili-Manga-Downloader/issues/52
[i61]: https://github.com/Zeal-L/BiliBili-Manga-Downloader/issues/61

### v1.2.0 - *2022-06-20*
- 新增功能: 现在可以一键保存漫画的元数据了，包括漫画封面，漫画信息, 等等 (json格式) ([#39][i39])
- 重大优化: 对于 `文件夹-图片形式` 和 `7z压缩包` 的保存方式取消了对漫画原图像的二次压缩，现在图像保存的质量和原图一致。~~（虽然用肉眼看不出来）~~ 由于 `PDF` 保存格式的特殊性，仍然会进行二次压缩和信道转换

[i39]: https://github.com/Zeal-L/BiliBili-Manga-Downloader/issues/39


### v1.1.0 - *2022-05-19*
- 新增功能: 添加了多种主题选择
- 新增功能: 一键检查软件更新
- 修复bug: 修复了一个可能会导致启动失败的保存路径设置；现在如果保存的路径意外失效会初始化为默认路径（cwd）

### v1.0.4 - *2022-04-24*
- 优化使用体验: 我的库存列表现在按照漫画名排序
- 优化项目结构: 重新分类了原始UI文件和资源文件，并更新了打包脚本
- 更新依赖项：更新了过去一个月积攒的 pyside6，pillow 等 python 库的新版本

### v1.0.3 - *2022-03-12*
- 修复bug: 使用7z保存时可能会因为文件名特殊字符引起报错；添加针对“.”的正则过滤
- 优化配置: 全局网络请求的 timeout 以及 max retry 值增大一倍

### v1.0.2 - *2022-03-11*
- 修复bug: 总进度条数值错误更新为0
- 优化设置选项: 以防在网络不好的情况下高线程数导致的频繁重试警告，最大线程数现在设为32

### v1.0.1 - *2022-03-9*
- 优化UI视觉: 因为网络错误跳过任务后，更新总进度条的进度，速度和剩余时间信息
- 更新关于界面: 添加了作者的联系方式

### v1.0.0 - *2022-03-6*
- 第一个正式版本
- 所有基本功能都测试可用

## 🍻 联系方式
欢迎进群讨论程序，漫画，资源分享, 提交问题等等
- Q群号：244029317

## 🙈 PS
- **做项目不易，求星星！求赞助！如果本项目对你有帮助，请作者喝杯☕吧~**

<img src="https://user-images.githubusercontent.com/72005386/223096480-8d57ceef-0b33-4653-86bf-55e6094fcb9b.jpg" width=20%> <img src="https://user-images.githubusercontent.com/72005386/223096520-e5d95ac8-044d-4644-8500-3770e5ad81f8.jpg" width=18.5%>

## 🔒️ 许可协议
- 本项目在遵循 [**GNU Affero General Public License v3.0**](https://www.gnu.org/licenses/agpl-3.0.en.html) 许可协议下进行发布
- 若对代码进行了修改，请务必遵循许可协议的规定进行发布
- **特别提醒，未经合法授权，擅自使用本项目的内容可能涉及侵权行为，我们保留追究相应法律责任的权利**

## ⚠️ 免责申明
- **本软件提供的所有内容，仅可用作学习交流使用，未经版权方以及原作者授权，禁止用于商业目的以及其他用途。请在下载24小时内删除。为尊重版权，请前往资源的原始发布网站观看，支持原创，谢谢**
- 本软件只提供漫画解析，不提供任何个人信息上传、存储到服务器的功能
- 本软件解析得到的所有内容均来自哔哩哔哩漫画官方上传、分享，其版权均归原作者以及哔哩哔哩漫画所有。内容提供者、上传者应对其提供、上传的内容承担全部责任
- 因使用本软件产生的版权问题，软件作者概不负责
- 我们强烈建议您详细阅读并遵守许可协议的规定，以保障您与他人的权益和合法使用
## 🌟 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=Zeal-L/BiliBili-Manga-Downloader&type=Date)](https://star-history.com/#Zeal-L/BiliBili-Manga-Downloader)


