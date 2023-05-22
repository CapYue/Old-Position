## 向GitHub远程仓库提交文件的两种方式：

### Github存在仓库，需要拉到本地，修改再提交

```C++
git clone ssh
```

![image-20230522223900709](mdImage/image-20230522223900709.png)

git bush中的粘贴按键为 shift + insert

使用git clont拉到本地的仓库，已经完成了仓库的初始化，也完成了远程仓库的关联。下一步

1.添加文件

首先在windows文件夹中添加需要增加的文件，例如a.md

然后：

```c++
添加文件到暂存区
提交文件
将文件提交给远程仓库
```

指令如下：

```C++
	git add a.md
	git commit -m '添加文件'
    git push -u origin master
```

