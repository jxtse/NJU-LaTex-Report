<h1 align="center">
  南京大学课程大作业LaTeX模板
</h1>

<p align="center">
  NJU Course Report LaTeX Template
</p>

<p align="center">
  <img src="https://img.shields.io/badge/LaTeX-Template-blue" alt="LaTeX Template">
  <img src="https://img.shields.io/badge/License-MIT-green" alt="MIT License">
  <img src="https://img.shields.io/badge/University-NJU-purple" alt="Nanjing University">
</p>

## 📖 简介

这是一个专为南京大学（NJU）课程大作业/结课报告设计的LaTeX模板。模板具有以下特点：

- ✨ **简洁美观**：采用现代化的排版设计，符合学术报告规范
- 🎯 **开箱即用**：预配置常用宏包和环境，无需复杂设置
- 📚 **功能完整**：支持封面、摘要、目录、正文、参考文献等完整结构
- 🔧 **易于定制**：模块化设计，方便根据具体课程要求调整
- 🌐 **多平台支持**：兼容Overleaf、TexPage等在线平台

## 🚀 快速开始

### 在线使用（推荐）

1. **Overleaf**: 直接下载zip文件，在Overleaf中导入即可，需要在File-Settings中选择Compiler为`XeLaTex`
2. **TexPage**: 推荐南大学生使用[e-Science中心部署的TexPage版本](https://tex.nju.edu.cn/)，包含协作和不限量的AI功能（仅限南大学生使用），使用方法与Overleaf相同

### 本地使用

1. 下载模板文件
```bash
git clone https://github.com/jxtse/NJU-LaTeX-Report.git
cd NJU-LaTeX-Report
```

2. 使用XeLaTeX编译
```bash
xelatex main.tex
bibtex main
xelatex main.tex
xelatex main.tex
```

## 📁 文件结构

```
NJU-LaTeX-Report/
├── main.tex           # 主文档文件
├── reference.bib      # 参考文献数据库
├── NJUReport.cls      # 文档类定义文件
├── figures/           # 图片文件夹
│   ├── nju-emblem-purple.pdf
│   └── nju-name-purple.pdf
├── README.md          # 说明文档
└── LICENSE            # 许可证文件
```

## ⚙️ 使用方法

### 1. 个人信息设置

在 `main.tex` 文件开头修改个人信息：

```latex
\headl{2025春}              % 学期
\headc{课程名称}            % 课程名称
\headr{姓名 学号}           % 姓名和学号
\lessonTitle{课程名称课程报告}  % 课程标题
\reportTitle{报告标题}       % 报告标题
\stuname{姓名}              % 学生姓名
\stuid{学号}                % 学号
\inst{学院名称}             % 学院
\major{专业名称}            % 专业
```

### 2. 编写内容

- **摘要**：在 `\begin{abstract}...\end{abstract}` 中编写
- **正文**：使用标准的LaTeX章节命令 `\section{}`、`\subsection{}` 等
- **参考文献**：在 `reference.bib` 中添加文献条目，使用 `\cite{}` 引用

### 3. 添加图片

将图片文件放在 `figures/` 文件夹中，使用以下方式插入：

```latex
\begin{figure}[h]
\centering
\includegraphics[width=0.8\textwidth]{figures/your-image.pdf}
\caption{图片标题}
\label{fig:your-label}
\end{figure}
```

### 4. 数学公式

支持完整的数学环境：

```latex
\begin{equation}
E = mc^2
\label{eq:einstein}
\end{equation}
```

## 🎨 自定义功能

### 预定义环境

模板预定义了常用的数学环境：

```latex
\begin{definition}[定义名称]
定义内容...
\end{definition}

\begin{theorem}[定理名称]
定理内容...
\end{theorem}

\begin{proposition}[命题名称]
命题内容...
\end{proposition}
```

### 自定义命令

可以根据需要添加自定义命令：

```latex
\newcommand{\mycommand}{\mathrm{MyCommand}}
```

## 📋 参考文献格式

模板使用IEEE格式的参考文献样式。在 `reference.bib` 中添加文献：

```bibtex
@article{example2024,
  author  = {Author Name},
  title   = {Article Title},
  journal = {Journal Name},
  volume  = {1},
  number  = {1},
  pages   = {1--10},
  year    = {2024}
}
```

## 🔧 常见问题

### Q: 编译时出现字体错误？
A: 确保系统安装了中文字体，或使用在线平台编译。

### Q: 如何修改页面布局？
A: 在 `NJUReport.cls` 文件中修改相关设置。

### Q: 如何添加更多数学符号？
A: 在导言区添加相应的宏包，如 `\usepackage{amssymb}`。

### Q: 参考文献格式如何修改？
A: 修改 `\bibliographystyle{}` 命令中的样式名称。

## 🙏 致谢

- 基于 [国科大模板](https://github.com/jweihe/UCAS_Latex_Template) 修改
- 感谢南京大学e-Science中心提供的 [TexPage](https://tex.nju.edu.cn/) 平台

<p align="center">
  Made with ❤️ for NJU students
</p>
