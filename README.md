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

# 操作指南
----------
可能很多人第一次接触dojo，我给大家讲解一下具体的操作步骤，要添加查看一个漏洞我们得先为他添加产品（例如：微信、腾讯QQ属于不同的产品，或者阿里娱乐、阿里教育、淘宝天猫这样子），下图是添加产品后在进入任务列表内的页面。
![enter description here][2]
我们先点击其中一个产品，进入具体的产品页面，可以看到有具体的任务和扫描。要查看或添加漏洞，我们需要进入具体的任务。小团队推荐只需要建立一个全年测试活动。
![enter description here][3]
点击进入2月份电商活动测试，我们会发现测试可以再次细分，这里的分类就是具体的测试类型分类了，我们可以区分为扫描器扫描，burpsuit扫描，具体的功能测试。
![enter description here][4]
点击进入具体的功能测试，我们就可以添加和查看这些漏洞了。
![enter description here][5]
到此dojo最基础的漏洞记录功能就给大家叙述完了，但是这仅仅是dojo的一部分，大部分功能大家还需要自己了解，或者查看官方文档。关于中文版的dojo，欢迎大家和我一起交流，邮箱：**kcjiazu@qq.com**
# 更新记录
----------


 - 2018年2月
1).完成任务页面的汉化与具体测试页面汉化
 


  [1]: ./doc/img/screenshot.png
  [2]: ./doc/img/screenshot1.png
  [3]: ./doc/img/screenshot2.png
  [4]: ./doc/img/screenshot3.png
  [5]: ./doc/img/screenshot4.png