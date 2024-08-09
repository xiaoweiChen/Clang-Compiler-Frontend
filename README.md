# Clang Compiler Frontend
Get to grips with the internals of a C/C++ compiler frontend and create your own tools  <a href=""><img src="cover.png" height="256px" align="right"></a>

* 作者：Ivan Murashko
* 译者：陈晓伟
* Packt Publishing Ltd. (首次出版于: 2024年3月)

> [!IMPORTANT]
> 翻译是译者用自己的思想，换一种语言，对原作者想法的重新阐释。鉴于我的学识所限，误解和错译在所难免。如果你能买到本书的原版，且有能力阅读英文，请直接去读原文。因为与之相较，我的译文可能根本不值得一读。
>
> <p align="right"> — 云风，程序员修炼之道第2版译者</p>

## 本书概述

**Low Level Virtual Machine** (LLVM)是一套模块化和可重用的编译器及工具链技术，用于开发编译器和编译器工具，例如:代码检查器和重构工具。LLVM用C++编写，一个结构良好的项目。它使用了一些有趣的技术，旨在使其可重用且高效。该项目也可视为编译器架构的杰出示例，深入研究，将了解编译器的组织方式和功能，这有助于理解使用模式并应用。

LLVM的关键组件是名为Clang的C/C++编译器。这款编译器在多家公司中得到了广泛使用，并指定为某些开发环境中的默认编译器，尤其是在macOS开发中。Clang将是我们在本书中的主要研究对象，特别关注其前端——即与C/C++编程语言最接近的部分。具体来说，书中将包括示例，展示C++标准如何在编译器中实现。

LLVM设计的核心要素是其模块性，这便于创建利用编译器全面能力的定制工具。书中一个示例是Clang-Tidy代码检查框架，旨在识别不良的代码模式并更正。尽管它包含了数百项检查，但可能找不到特定于自己项目需求的检查，所以这本书将提供从头开始开发此类检查所需的基础知识。

LLVM是一个积极发展的项目，每年会有两个主要版本发布。撰写本书时，最新的稳定版本是17版。与此同时，18版的发布候选版本已于2024年1月推出，预计其正式发布将与本书的出版同步。本书的内容已经针对最新的编译器版本18进行了验证，确保内容是基于当前最新编译器实现的见解。



## 作者简介

**Ivan Murashko**是一位C++软件工程师，在彼得大帝圣彼得堡国立理工大学获得了物理学博士学位，并拥有超过20年的C++编程经验，主要在Linux平台上。自2020年以来，他一直与LLVM编译器合作，并自2021年起成为LLVM的提交者。兴趣领域包括Clang编译器前端、Clang工具（如Clang-Tidy和Clangd），以及编译器和编译器工具的性能优化。



## 本书相关

* github翻译地址：https://github.com/xiaoweiChen/Clang-Compiler-Frontend

* 译文的LaTeX 环境配置：https://www.cnblogs.com/1625--H/p/11524968.html

  * 禁用拼写检查：https://blog.csdn.net/weixin_39278265/article/details/87931348

  * 使用xelatex编译时需要添加`-shell-escape`和`-8bit`选项，例如：

    `xelatex -synctex=1 -interaction=nonstopmode -shell-escape -8bit "C++-Standard-Library".tex`

  * 为了内容中表格和目录索引能正常生成，至少需要连续编译两次

  * Latex中的中文字体([思源宋体](https://github.com/adobe-fonts/source-han-serif/releases))和英文字体([Hack](https://github.com/source-foundry/Hack-windows-installer/releases/tag/v1.6.0))，需要安装后自行配置。如何配置请参考主.tex顶部关于字体的信息。

* vscode中配置LaTeX：https://blog.csdn.net/Ruins_LEE/article/details/123555016

