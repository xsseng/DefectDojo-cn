# DefectDojo-cn
----------
DefectDojo-cn是对DefectDojo资源文件进行汉化的版本，你需要先安装原版的DefectDojo。
![enter description here][1]
# 文档


----------


 1. 安装Mysql与Virtualenv
``` bash
$ apt-get install mysql-server
$ pip install virtualenv
$ virtualenv dojo
$ source dojo/bin/activate
```
2.安装DefectDojo
``` bash
$ git clone https://github.com/DefectDojo/django-DefectDojo
$ cd django-DefectDojo
$ ./setup.bash
$ ./run_dojo.bash
```
3.安装Uwsgi
``` bash
$ pip install uwsgi
```
4.setiings.py添加本机为信任IP
``` python
ALLOWED_HOSTS = [u'IP']
```
5.settings.py和/etc/python2.7/sitecustomize.py中添加如下代码

``` python
import sys
reload(sys)
sys.setdefaultencoding('utf8')
```
6.进入mysql的dojo数据库中执行sql文件，然后替换/template/目录下的所有文件


  [1]: ./doc/img/screenshot.png