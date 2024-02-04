# AVOID404
本项目主要供程序员使用，收集归纳因为网络原因，下载程序包，模型等失败的解决办法。不定期更新，

## pip下载包加速
```
pip3 config set global.index-url http://mirrors.aliyun.com/pypi/simple/
pip3 config set install.trusted-host mirrors.aliyun.com
pip3 install -U pip
```

## conda下载包加速
```
conda config --add channels https://mirrors.aliyun.com/anaconda/pkgs/main/
conda config --add channels https://mirrors.aliyun.com/anaconda/pkgs/free/
conda config --add channels https://mirrors.aliyun.com/anaconda/pkgs/r/
```

## huggingface模型下载加速
```
export HF_ENDPOINT=https://hf-mirror.com
```

## docker镜像下载加速
编辑/etc/docker/daemon.json，加入如下内容:
```
"registry-mirrors":["https://docker.mirrors.ustc.edu.cn/"]
```
编辑后，daemon.json的内容示例如下：
```
{
    "runtimes": {
        "nvidia": {
            "args": [],
            "path": "nvidia-container-runtime"
        }
    },
    "registry-mirrors":["https://docker.mirrors.ustc.edu.cn/"]
}
```
