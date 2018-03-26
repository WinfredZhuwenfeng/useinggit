# hexo

1. 安装hexo
npm install hexo-cli -g

2. 创建一个博客文件夹
在文件夹中执行    hexo init

3. 在文件夹中直接执行 hexo s  在本地测试网页效果


## 新建文章
hexo new "文章名称"

这句命令执行完毕之后，会在source/_posts/ 中生成以文章名为文件名的markdown文件

## 编辑文章
找到对应的markdown文件，编辑内容即可

## 生成html
hexo g

执行这条命令之后，会在public目录下生成所有的静态页面，只要将该目录下所有的文件进行发布，发布到github上，就可以通过github的静态页面托管服务来访问页面了



## 如何使用hexo d 来发布网站呢

1. 安装 hexo-deployer-git 
	npm install hexo-deployer-git --save

2. 配置网站根目录下面的_config.yml
	配置最下面的deloy节点
	deploy:
		- type: git
		  repo: github静态页面托管项目的地址

2.1 在public目录下执行 git init 并进行一次提交

3. 按照正常流程创建博客， 编辑博客

4. 执行hexo g

5. 在 public 目录下去执行 hexo d