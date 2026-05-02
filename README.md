# Git 版本控制实践报告

## 一、学习资料来源
- [Git 官方文档](https://git-scm.com/doc)
- 豆包 实操教学
- B站 Git 入门教学视频

## 二、实践流程
### 1. Git 安装与配置
1.  从 Git 官网下载并安装 `Git for Windows` 64位版本。
2.  打开 Git Bash，配置用户名和邮箱：
    ```bash
    git config --global user.name "***"
    git config --global user.email "***"
3.  使用 git config --list 验证配置成功。
### 2. 本地仓库创建
1.  选好文件位置创建文件夹git-practice，并在该文件夹内打开git bash做主仓库。
2.  初始化本地仓库：
    ```bash
    git init
    ```
    终端显示 Initialized empty Git repository，代表创建成功。
### 3.  远程仓库创建
1.  打开Github账户，创建一个新的仓库，仓库名为git-study
2.  复制仓库的 SSH 地址。
3.  在本地仓库中添加远程仓库：
    ```bash
    git remote add origin https://github.com/***（用户名）/***（仓库名）
    ```
4.  使用 git remote -v 验证关联成功
    ```bash
    git remote -v
    ```
### 4.  本地仓库提交代码
1. 第一次创建test.txt文件（空）
touch test.txt
git add .
git commit -m "第一次提交：添加test文件"
2. 第二次提交test.txt文件（添加内容）
echo "我在修改文件" >> test.txt
touch test.txt
git add .
git commit -m "第二次提交：修改test内容"
3. 第三次创建 README.md文件
touch README.md
git add .
git commit -m "第三次提交：添加README文档"
4. 推送到远程仓库
    ```bash
    git push -u origin master
    ```
## 三、提交记录说明
提交 1：创建 test.txt 文件，用于测试基础提交功能。
提交 2：修改 test.txt 内容，验证文件修改后的提交流程。
提交 3：创建并添加 README.md，记录本次实践的完整过程。

## 四、遇到的问题及解决方法
问题 1：执行 git remote add 时报错 fatal: not a git repository
原因：当前终端路径不在 Git 仓库文件夹内。
解决方法：使用 cd 命令进入 git-practice 文件夹，确认终端显示 (master) 后再执行命令。
问题 2：推送时遇到 GitHub 授权按钮无法点击
原因：浏览器插件拦截或页面加载异常。
解决方法：刷新页面后重试，或使用 Git Credential Manager 完成授权，授权成功后推送自动继续。

## 五、Git 学习心得
通过本次实践，我掌握了 Git 的基础使用流程，理解了版本控制的核心概念，包括本地仓库、远程仓库、提交与推送的关系。Git 不仅能帮助我们记录代码修改历史，方便回溯与协作开发。