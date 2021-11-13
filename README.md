# 如何写电子书
> 陈希章 2021-11-13

## 先决条件
- 安装NodeJS稳定版
- 安装VS Code
    - 安装 Markdown Paste 这个插件，并设置默认目录（Markdown Paste: Path）为 `${workspaceRoot}/images`， 设置（Markdown Paste：Slience）为 `true`

## 创建项目和初始化

```
mkdir book
cd book
npm init -y
npm install honkit --save-dev
npx honkit init
git init
code .
```

创建 .gitignore文件，内容如下

```
node_modules
_book
```

创建book.json文件，内容如下
```
{
    "title": "我的书籍标题",
    "author": "作者名称",
    "description": "书籍的描述信息，可用于SEO",
    "language": "zh"
}
```
## 撰写书籍

- SUMMARY.md 定义目录
- 其他就是按照需求编写markdown文件即可，建议不同章节用文件夹分开
- 图片粘贴，请用 CTRL+ALT+V 即可，会自动在根目录下面的images目录

## 发布到Github pages

- 创建一个public的仓库
- 创建远程仓库链接 `git remote add origin 你的仓库地址`
- 提交更新到Github `git add .`, 然后 `git commit -m '初始化'`, 最后 `git push origin master`