# TongjiThesis
同济大学硕博士论文LaTeX模板
斗胆将其称为TongjiThesis v2.0
不过目前仍有很多地方和学校的word版本不一致，我还在继续改。
## 主要改动
相较于老版tongjithesis，我这个版本融合了thuthesis （ThuThesis 2017/12/24 5.4.3）的很多新改动，个人认为比较大的改动如下:
1. 加入更详尽的注释。我甚至将很多宏的用法用例子进行阐述，当然详细的注释主要集中在“宏展开”的部分。这就极大地方便了模板的阅读和理解，期待校友们更多地参与到对此模板的改进。
1. 老版基于book制作，新版基于ctexbook
1. 老版字体基于xeCJK（adobe的字体），新版采用ctex宏集(我现在看的是2018/01/28 v2.4.12《ctex宏集手册)自带的字体配置，比如在新版windows操作系统上，采用的是中易字库+ 微软雅黑
1. 页面设置采用geometry宏包。
1. 使用kvoptions宏包，从而可以使用key-value input的方式设置class的option
1. 使用fancyhdr宏包设置页眉页脚
1. 修改了老版的许多错误参数（当年也许是对的。
1. 章节标题的设置使用ctex宏集提供的`\ctexset`进行设置。
1. 使用较新的性能更强的宏包替代老宏包。如etoolbox引入了LATEX kernel commands的不同实现，但功能一样，xparse提供了更强的\NewDocumentCommand，以替代\newcommand。使用subcaption替代subfig，并使用subcaption进行浮动体参数的设定等。

## 运行
本人使用Texlive2017发行版，xelatex 可以编译通过。

注：
1. 我照抄了清华版的Makefile，因此可以直接在命令行使用`make thesis`进行全自动编译（默认使用 latexmk 的方式生成 pdf，latexmk仍然调用xelatex）。在类Unix系统上很容易安装make命令。在windows系统上可以安装MinGW（装好之后，打开并安装最简明核心的`msys-base`，然后将其bin目录加到path中，如我的bin目录是 `C:\tools\mingw\msys\1.0\bi`n，这样就能在 `cmd` 中使用 `make` 了
1. 如果提示缺少某字体，请自行下载安装（如果你用的是windows系统，可以搜索中易的对应字体下载，如中易隶书）。
1. 原则上pdflatex,lualatex都可以编译，但目测由于字体问题无法编译通过。暂时不管这个问题了，反正xelatex用着很爽。

