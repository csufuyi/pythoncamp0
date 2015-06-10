## Python环境搭建-巧妇也得有个好厨房

假如你只使用一个python环境, 比如python 2.7.9，假如你使用的模块比较少，都是系统模块，可能你觉得挺安逸。

但一旦开始做一个实际的项目，要使用到诸多第三方模块。环境问题就变得不可避免。这个时候，就要用到pyenv或者virtualenv了。

我起初也不在乎这个问题，后来遇到python版本问题和模块版本冲突，才回来补这一块。理解python生态环境，是任性折腾的基础。

这个介绍能帮助理解：
https://github.com/dccrazyboy/pyeco/blob/master/pyeco.rst

大妈在邮件列表中曾生动形象的解释：pyenv 和 virtualenv

>
- 一般一个系统中默认已经安装了一个 Python 环境
- 但是,我们进行开发时,可能需要另外版本的 Python 运行环境
- 这时,就有两个选择:
    + 安装新版本 Python 环境,替代系统的
    + 安装新版本 Python 环境,和系统平行使用
- 问题就在:
    + 前者, 可能引发系统不稳定
    + 后者, 调用以及安装对应模块时,会有名称冲突
- 所以,程序猿们给出了很多解决方案,比如说:
    + virtualenv ~ 安装一个和我们项目代码绑定的虚拟 Python 环境
    + pyenv ~ 安装/管理任意 Python 环境,需要时绑定任意目录

>要进行比喻的话:
>
- 系统环境 ~ 住房
- Python 环境 ~ 厨房
    + 依赖/加载的模块 ~ 厨具/作料
- 替代系统的 Python 环境
    + 相当于,每去别人家,就将人家厨房整个儿装修成和自个儿家一样的
- virtualenv 管理的 Python 环境
    + 相当于, 无论去哪儿,每作一道菜
    + 要先从类似小叮当的口袋中
    + 取出有整个对应专用 厨具/作料 的厨房来用
- pyenv 管理的 Python 环境
    + 相当于,无论你去哪家
    + 都有一个任意门
    + 随时可以进入任意一种包含某道菜 专用 厨具/作料 的厨房来用


助教们的总结:
>
用virtualenv做python虚拟环境
https://github.com/OpenMindClub/OMOOC.py/wiki/build_pyen
>
pyenv virtualenv  
https://github.com/OpenMindClub/OMOOC.py/wiki/pyenv-virtualenv

参考资料：
>
这个是说python包管理最清楚的：
http://udonmai.com/work/about_python_version_and_environment_mangement.html

>
http://www.it165.net/pro/html/201405/13603.html

总结：  
简单的说，pyenv 和 virtualenv ，前者是纯粹的 Python 版本管理工具，而后者，则用于分割、管理 Python （开发）环境。两者结合起来就可以，就可以自如的使用了。

步骤：  

- 安装pyenv
https://github.com/yyuu/pyenv

- 安装pyenv-virtualenv
https://github.com/yyuu/pyenv-virtualenv

- 使用过程
注意virtualenv是作为pyenv的插件而存在的，所以使用时，下面的命令创建依赖的版本，必须是verisons目录存在的版本，所以versions目录要先安装python版本。

$ pyenv virtualenv 2.7.7 my-virtual-env-2.7.7

will create a virtualenv based on Python 2.7.7 under ~/.pyenv/versions in a folder called my-virtual-env-2.7.7.









	

