# 脚本管理role(ansible)
- 安装使用
- 脚本迭代说明

## 安装使用
```
ansible-playbook script.yml
```

#### 安装ansible ansible-playbook
mac下使用brew可直接安装，不建议在windows下使用

## 脚本迭代

#### 脚本维护

1、脚本在```roles/scripts/templates```目录下维护 
2、脚本要以.j2为后缀，通过```{{ 变量名 }}```方式设置脚本一些可变参数(常用的如服务器IP，一些脚本路径等)  
3、脚本写好之后在```roles/scripts/tasks```下找到对应的yml配置文件，如要在cloud服务器上改脚本就调整```cloud_scripts.yml```文件，这样执行ansible就能直接将脚本放置到服务器对应位置

#### 变量维护
变量在```roles/scripts/vars/main.yml```内维护  



