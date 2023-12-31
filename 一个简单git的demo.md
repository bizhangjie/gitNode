好的，下面是一个简单的Git demo，用来演示创建代码库、添加文件、提交更改和查看提交历史：

**步骤1：创建代码库**
在你想要创建代码库的文件夹中执行以下命令：
```
git init
```

**步骤2：添加文件**
在该代码库中添加一个新文件，例如命名为`hello.txt`，并写入一些内容。

**步骤3：将文件添加到暂存区**
将新增的文件添加到暂存区，使用以下命令：
```
git add hello.txt
```

**步骤4：提交更改**
将暂存区的更改提交到代码库，添加提交信息：
```
git commit -m "Add hello.txt"
```

**步骤5：查看提交历史**
查看代码库的提交历史，使用以下命令：
```
git log
```

这样就完成了一个简单的Git demo。现在你已经创建了一个Git代码库，添加了一个文件，并提交了更改。你可以通过`git log`命令查看提交历史，以及使用其他Git命令来管理你的代码库。随着使用Git的经验增加，你将掌握更多高级的Git功能，如分支管理、合并、标签等。



```
上面是只是上传到本地git仓库，如需要上传到github等远程托管平台上，
可以继续接下来的操作。
```

在GitHub上看不到你本地代码库的提交内容是因为本地代码库与GitHub上的远程仓库是分开的，它们之间并不自动同步。

为了将你本地的代码提交内容上传到GitHub上的远程仓库，你需要进行以下步骤：

**步骤1：在GitHub上创建一个新的远程仓库**
登录GitHub账号，在页面上创建一个新的仓库，并获取该仓库的URL。

**步骤2：将本地代码库与远程仓库关联**
在本地的代码库目录中，使用以下命令将本地代码库与远程仓库关联：
```
git remote add origin <远程仓库URL>
```
其中，`origin`是远程仓库的别名，你可以自定义它，通常默认为`origin`。

**步骤3：将本地代码推送到远程仓库**
使用以下命令将本地的代码提交推送到GitHub上的远程仓库：
```
git push -u origin <分支名>
```
这里`<分支名>`是你想要推送的分支名，通常是`main`或`master`。

完成以上步骤后，你的本地代码库的提交内容就会上传到GitHub上的远程仓库，其他人也就能在GitHub上看到你的提交内容了。