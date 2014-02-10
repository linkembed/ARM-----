## github的基本使用

初次使用git以及github，由于git在linux的命令行下使用，因此先大概做些操作上的记录，以后随着自己的使用，再来逐渐深入探讨操作。  

1. 工程（Project）的建立。  
要在github上托管项目，首先要注册一个帐号。帐号有收费的和免费的两种，对于我们只创建public项目（即所有人都能看到的开源项目）的人来说，免费帐户就够用了。如果你想将自己的个人私有项目也托管到github上，那就花点小钱弄个收费帐户了。  
 
**网页版创建新工程**
创建新项目可以通过浏览器进入[https://github.com](https://github.com)，登录个人帐号，然后在浏览器中创建工程。

登录你的个人帐户后，可以在其中创建自己的项目（repo）。如下图中的绿色底子的New图标，点击即可进入创建新托管项目的页面。   

![new repo](http://i.imgur.com/PVy2nLA.png)  
进入新项目创建页面后，填入新项目的名称，基本介绍，点击最下方的Create按钮即可完成新项目的创建。如下图所示，我创建了一个名为digit_album的新项目。

![](http://i.imgur.com/J0ZHJ1n.png)

该项目的访问，可以通过http和ssh两种协议。两种协议访问的地址分别如下：  
http访问地址： [https://github.com/linkembed/digital_album.git](https://github.com/linkembed/digital_album.git)
ssh访问地址： [git@github.com:linkembed/digital_album.git](git@github.com:linkembed/digital_album.git)

**命令行创建新工程**

命令行中按照以下步骤，完全从新建立一个新工程，并且可以commit到github上。  
```cmdline
touch README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:linkembed/digital_album.git
git push -u origin master
```

当然，如果你已经有了一个本地的git管理的工程，仅仅只是需要将其推送到github上托管，那只需要执行以下两步即可。
```cmdline
git remote add origin git@github.com:linkembed/digital_album.git
git push -u origin master
```