# LaTex skill

这里介绍很多常用的 LaTex 技巧

根据 latex 生成 pdf

## 基本编译语法

```cmd
latexmk -pdf .\zh-cn.tex
```

清除临时文件

```cmd
latexmk -pdf -c .\zh-cn.tex
```

## latex 中使用中文等其他非常规字符

LaTex 默认是不支持英文之外的字符的，其中包括了中文，所以增加 ctex 的包，设置`UTF-8`参数就可以完成.

[code](zh-cn.tex)

[pdf](zh-cn.pdf)

## 自定义命令

我们可以自定义命了完成很多特殊的操作

[code](new-cmd.tex)

[pdf](new-cmd.pdf)

## 自定义包裹命令

很多命令是用的 begin 作为开始，end 作为结束，包裹的内容，主要应对多行

[code](new-cmd-tag.tex)

[pdf](new-cmd-tag.pdf)

## 条件

可以设置条件来完成整体论文的变化

[code](condition.tex)

[pdf](condition.pdf)

## 样例

可以专门修改参数来测试效果

```tex
\documentclass{article}
\usepackage[UTF8]{ctex}
\usepackage{xcolor}
\usepackage{mdframed}
\usepackage{algorithm2e}

% ====== 条件开关设置 ======
\newif\ifshowrevised
\showrevisedtrue  % 打开：显示红色标记和红框
%\showrevisedfalse % 关闭：正常显示
```

红色标记的版本如下设置

```tex
\showrevisedtrue  % 打开：显示红色标记和红框
%\showrevisedfalse % 关闭：正常显示
```

干净的版本如下设置

```tex
%\showrevisedtrue  % 打开：显示红色标记和红框
\showrevisedfalse % 关闭：正常显示
```

[code](sample.tex)

[pdf](sample.pdf)
