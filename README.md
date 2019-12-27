## Django2.2之CMDB资产管理系统-教学学习项目
## 项目基于Django3.0、Adminlet-2.4.10、Python3.7、Pycharm2019、windows10
## 该项目教程发布在www.liujiangblog.com,本项目参照学习修改

## 简单的使用方法：


创建虚拟环境
使用pip安装第三方依赖(根据requirements.txt)
运行migrate命令，创建数据库和数据表
python manage.py makemigrations
python manage.py migrate
python mang.py createsuperuser
查看本机内网IP，修改为接收服务器IP
运行python manage.py runserver 0.0.0.0:8000启动服务器
在Client/bin/中运行python main.py collect_data收集数据和python main.py report_data发送数据


路由设置：


from django.contrib import admin
from django.urls import path
from django.urls import include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('assets/', include("assets.urls"))
]
