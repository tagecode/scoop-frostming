# scoop-frostming [![Build status](https://ci.appveyor.com/api/projects/status/029wg97af9l3f3v0?svg=true)](https://ci.appveyor.com/project/frostming/scoop-frostming)

My personal bucket for [Scoop](http://scoop.sh), which contains apps developed by myself

To make it easier to install apps from this bucket, run

    scoop bucket add frostming https://github.com/frostming/scoop-frostming.git

Application list:

-   [pdm](https://pdm.fming.dev)


---
### 1.为什么要 fork `scoop-frostming` 这个仓库？
上面的方式是安装最新版本的 PDM

因为一些原因，比如支持 python 3.7

我希望安装指定版本的 PDM，比如 2.17.2 版本，而不是最新版本。

所以我 fork 了这个仓库，然后修改了 bucket 文件夹下的 pdm.json 文件

将 version 字段的值改为 2.17.2

将 url 字段的值改为 2.17.2 的 URL

将 hash 字段的值改为 2.17.2 的 hash 值

这三个字段的值可以在： https://pypi.org/project/pdm/2.17.2/#modal-close 中找到

同理，要安装其他版本的 PDM 也是一样的修改，然后重新上传到 GitHub。

### 2.该怎么使用呢？

    scoop bucket add pdm2.17.2 https://github.com/tagecode/scoop-frostming.git

    scoop install pdm

pdm2.17.2 这个名字可以自己定义。

如果已经添加了 frostming 这个 bucket，那么要先删除它，然后再添加 pdm2.17.2 这个 bucket。

    scoop bucket rm frostming

    scoop bucket add pdm2.17.2 https://github.com/tagecode/scoop-frostming.git

    scoop install pdm
