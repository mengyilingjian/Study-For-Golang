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
    export GOPATH=$HOME/GoProjects/go
    ```
    配置生效：`source /etc/profile`

3. 安装vscode插件
   ```bash
   cd GOPATH/src/golang.org/x
   git clone https://github.com/golang/tools.git tools
   git clone https://github.com/golang/lint.git
   ```
   克隆完成后，调起命令面板，在弹出的窗口中全选，并再次执行：`Go: Install/Update Tools`

4. vscode Debug配置文件如下：
   ```json
    {
         "name": "Go Launch",
         "type": "go",
         "request": "launch",
         "mode": "auto",
         "remotePath": "",
         "port": 5546,
         "host": "127.0.0.1",
         "program": "${fileDirname}",
         "env": {
             "GOPATH": "/home/eric-matebook/GoProjects/go",
             "GOROOT": "/opt/go"
         },
         "args": [],
         //"showLog": true
     }
   ```


### 参考学习资料：

- [李文周讲师博客]( https://www.liwenzhou.com/ )

- [笔记来源视频]( https://www.bilibili.com/video/av73381776?p=3 )