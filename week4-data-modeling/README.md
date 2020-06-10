## Week 4 - Data Modeling and Project 1

### Video Download - 坚果云
[Data Modeling](https://www.jianguoyun.com/p/DfoIaDYQzpi5CBjwy6AD)

[Project 1] (https://www.jianguoyun.com/p/Dd1lUAwQzpi5CBjxy6AD)


### Project - Class 1
```
请看
https://github.com/stargrep/crypto-crawler/tree/class-2020-spring

学习project结构, 基本文件如下
- design.md         (设计文档)
- LICENCE           (授权)
- .gitignore        (可忽略文件列表)
- README.md         (读我)
- requirement.txt   (pip 安装文件)
- setup.py          (build python project)
- crypto_crawler    (源代码)
    - __init__.py
    - ... 
- tests             (测试代码)


运行步骤
0. 确定运行的folder
$ pwd
${your system dir}/crypto-crawler

1. 设置virtual environment
$ python -m venv env
这行命令将会创建 env/ 包含这个env中引入的包

2. 使用 env
$ source env/bin/activate

$ pip list
Package        Version
-------------- -------
pip            20.1.1
setuptools     41.2.0
证明在此env下的 pip 是新生成的。

$ pip install -r requirement.txt
$ pip list
Package        Version
-------------- -------
click          7.1.2
Flask          1.1.2
itsdangerous   1.1.0
Jinja2         2.11.2
MarkupSafe     1.1.1
pip            20.1.1
setuptools     41.2.0
Werkzeug       1.0.1

按照 requirement.txt 安装了 Flask

3. build project
$ python setup.py sdist
生成 sdist/ 里面会有当前版本(v0.2)的tar.gz文件

$ ls dist
crypto_crawler-0.2.tar.gz

4. pip 安装
$ pip install dist/crypto_crawler-0.2.tar.gz

5. pip list 查看crypto_crawler安装
$ pip list
Package        Version
-------------- -------
click          7.1.2
crypto-crawler 0.2
Flask          1.1.2
itsdangerous   1.1.0
Jinja2         2.11.2
MarkupSafe     1.1.1
pip            20.1.1
setuptools     41.2.0
Werkzeug       1.0.1
(env) 

新添加了crypto-crawler包

6. 运行crypto-cralwer包，会执行 crypto_crawler/__main__.py
$ python -m crypto_crawler
hello,  https://coinmarketcap.com/currencies/bitcoin/markets
(env) 

7. 运行测试
右键点击 tests/ 执行 "Run 'Unittest in tests'"

```
