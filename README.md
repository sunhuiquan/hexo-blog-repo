# 博客备份

1. 安装 nodejs 和 npm [官网链接](https://nodejs.org/zh-cn/download/)
2. 安装 hexo
	```bash
	npm install -g hexo
	```
3. 创建博客
	```bash
	hexo init # 初始化项目
	hexo new post <title> # 创建post
	```
4. 部署博客
	```bash
	hexo g # 产生文件
	hexo s # 本机访问 http://localhost:4000/
	hexo d # 部署(需要先hexo g产生文件)
	```
5. 配置文件
	1. _config.yml   内部有部署的服务器和一些网站内容设置
	2. source/_posts 博文
6. 出现 node_modules 相关的问题
	```bash
	rm -rf node_modules
	npm install --force
	```
7. 插入图片
	要在 source 下创建一个 images 文件夹，然后 !\[IMG\]\(/images/xx.png\) 的方式引用，hexo 部署后的根目录就是 source，所以 / 代表 source 目录，我们要用绝对路径，因为非首页的情况下同样文章的所在路径不同。另外必须在 source 目录下，原因同上，source 外不会被算入。
