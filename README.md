# Install-homebrew-question
This will tell you how to solve `curl: (7) Failed to connect to raw.githubusercontent.com port 443: Connection refused`

**安装homebrew或者其他国外内容时可能遇到的问题**

`curl: (7) Failed to connect to raw.githubusercontent.com port 443: Connection refused`

这是国内墙导致的。

## 解决方案一：

这边直接挂一个梯子，然后执行梯子的代码之后，就可以放心安装了。

这边给的是 `clashx` 的例子： 先复制 `shell command` 然后在终端中执行一下之后下载即可。

<img src="https://img-blog.csdnimg.cn/20210420190319237.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L1dhdGVyX0N5YW4=,size_16,color_FFFFFF,t_70" alt="clashx-set" style="zoom:50%;" />

```shell
# copy shell command 拷贝下来的
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

执行一下上面的代码就可以了。

然后正常安装 [homebrew](https://brew.sh/) 就可以了

```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## 解决方案二：
`oh-my-zsh` 安装时遇到这个问题，可以直接改变文件中指向的 `git` 仓库从 `github` 移到 `gitee`
```shell
sh -c "$(curl -fsSL https://gitee.com/shmhlsy/oh-my-zsh-install.sh/raw/master/install.sh)"
```


