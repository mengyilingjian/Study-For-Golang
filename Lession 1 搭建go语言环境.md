### 安装go语言开发包
1. 下载并解压安装包
     ```bash
     cd ~/Downloads
     wget https://dl.google.com/go/go1.14.1.linux-amd64.tar.gz
     tar -zxvf go1.14.1.linux-amd64.tar.gz
     cp go /opt
     ```
2. 配置环境变量
    ```bash
    sudo vim /etc/profile
    ```
    写入以下内容
    ```bash
    export GOROOT=/opt/go
    export PATH=$GOROOT/bin:$PATH
    export GOPATH=$HOME/GoProjects/
    ```
    配置生效：`source /etc/profile`

### 参考学习资料：

- [李文周讲师博客]( https://www.liwenzhou.com/ )

- [笔记来源视频]( https://www.bilibili.com/video/av73381776?p=3 )