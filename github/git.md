## github 使用方式
	克隆 git clone 路径
	
	添加 git add .

	//只有添加后才能提交
	git commit -m '这里面写你提交的信息'
	
	//只有推送别人才能看到你的代码
	git push origin master

	//拉去
	git pull

## 版本回滚
	现实之前的log
	$ git log -3

	回滚到指定的版本
	git reset --hard e377f60e28c8b84158

	强制提交
	git push -f origin master

	
