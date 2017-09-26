create a new repository on the command line

echo "# ******" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/2hz4917/******.git
git push -u origin master

忽略需要上传的文件/文件夹
创建一个.gitignore文件
win7下创建".gitignore."文件 自动转化为".gitignore"
"#"开头的一行为注释
#过滤数据库文件、sln解决方案文件、配置文件  
*.mdb  
*.ldb  
*.sln  
*.config  

#过滤文件夹Debug,Release,obj  
Debug/  
Release/  
obj/  
#然后调用git add. ，执行 git commit即可。

// 不需要上传的东西
/mtk/ 过滤整个文件夹

*.zip 过滤所有.zip文件

/mtk/do.c 过滤某个具体文件

// 需要上传的某些特定对象
!*.zip

!/mtk/one.txt

唯一的区别就是规则开头多了一个感叹号，Git会将满足这类规则的文件添加到版本管理中。

本地仓库完成的时间已经很久了，需要上传代码
将原来的 git pull origin master
改为 git pull origin master --allow-unrelated-histories
