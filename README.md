## **pocsuite3**

```
pocsuite3 是由Knownsec 404 团队开发的开源远程漏洞测试和概念验证开发框架。它配备了强大的概念验证引擎，为终极渗透测试人员和安全研究人员提供了许多不错的功能。并且该工具被kali收录到系统自带工具
```

## 下载&安装&卸载

项目地址

```
https://github.com/knownsec/pocsuite3
```

环境

```
Python 3.7+
Works on Linux, Windows, Mac OSX, BSD, etc.
```

pip安装

```
pip3 install pocsuite3

# use other pypi mirror
pip3 install -i https://pypi.tuna.tsinghua.edu.cn/simple pocsuite3
```

git clone

```
git clone https://github.com/knownsec/pocsuite3.git
cd pocsuite3

pip3 install -r requirements.txt

# 在源码中修改一下
python3 setup.py install
```

安装好测试

```cmd
D:\maye\常用工具\pocsuite3\pocsuite3-master\pocsuite3>pocsuite --version
,------.                        ,--. ,--.       ,----.   {1.9.2-nongit-20220315}
|  .--. ',---. ,---.,---.,--.,--`--,-'  '-.,---.'.-.  |
|  '--' | .-. | .--(  .-'|  ||  ,--'-.  .-| .-. : .' <
|  | --'' '-' \ `--.-'  `'  ''  |  | |  | \   --/'-'  |
`--'     `---' `---`----' `----'`--' `--'  `----`----'   https://pocsuite.org
usage: pocsuite [options]
Pocsuite3: error: unrecognized arguments: version

Press Enter to continue...
```

## 使用参考

具体使用教程参考

```
https://github.com/knownsec/pocsuite3/blob/master/docs/USAGE.md
```

### 单个url

单个url使用验证模式运行 poc。PoC(s) 将仅用于漏洞扫描。

```shell
pocsuite -r pocs/poc_example.py -u http://www.example.com/ --verify
                       poc文件的路径                  待检测的url
                       
pocsuite -r pocs/thinkphp_rce2.py  -u http://192.168.6.29:8080/ --verify
```

### 批量检测

扫描文本文件中给定的多个目标

```
pocsuite -r pocs/poc_example.py -f url.txt --verify
```
