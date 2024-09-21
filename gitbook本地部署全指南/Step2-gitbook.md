# 2.🎯gitbook使用
本文简要介绍用法，创建项目及进行编辑操作
## 2.1 创建一个 gitbook 项目

文件资源管理器在本地磁盘中尽量选择一个空目录，创建你的 gitbook folder  
进入项目文件夹  
右键→在终端中打开  
你会发现命令行操作的目录即为当前打开的文件目录，当然也可以手动 cd 到此目录下进行操作  
命令行：
```
gitbook init
# 执行项目初始化，gitbook 会自动创建需要的文件
```
```
gitbook build
# 根据现有的文件创建 gitbook 页面
```
```
gitbook serve
# 启动本地端口快速进行网页预览
```
Gitbook serve 启动后会先将网页构建，之后会自动监听文件变化，实时生成更新页面，可在浏览器中预览效果
按住 Ctrl 和鼠标左键点击链接可在浏览器新标签页快速打开链接
Ctrl+C 可以终止 serve 命令  

此为一个项目结构示例：
>my-gitbook/  
>├── book.json(配置文件，可能没有自动生成，需要手动创建)  
>├── README.md（gitbook 首页）  
>|── SUMMARY.md（gitbook 遵循此文件内容进行网页生成）  
>└── _book（gitbook 生成的静态页面文件夹）

你需要在根目录中建立你文件夹目录，然后在 SUMMARY.md 根据示例中添加目录链接，gitbook 会根据此文件生成目录结构  
链接语法遵循 markdown 语法，可参考 [markdown 语法](https://www.runoob.com/markdown/md-tutorial.html)

相对链接示例：
```
- [自定义标题名称](根目录下自创建的文件夹名称\文件名.md)
```