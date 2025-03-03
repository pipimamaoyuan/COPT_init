# COPT_init 在window和linux远程服务器中部署杉树科技的COPT优化器
## 在本地 windows 中部署 COPT优化器
#### 1. 推荐 下载可执行安装程序 （下载链接名称中含有 "installer"）
- 默认设置下，杉数求解器安装路径为： C:\Program Files\copt72，用户可以修改为 任意路径。
- 安装过程中将自动配置必要的环境变量。安装完成后，请按照要求重启计算机。
#### 2. 配置许可文件
- 对于Windows系统，用户目录形如："C:\Users\username" ， 用户可手动将2个授权文档 license.dat 和 license.key 移动至目录 "C:\Users\username\copt" 中。
#### 3. 环境变量方式 
- 对于Windows系统， 执行下述命令查看环境变量 COPT_LICENSE_DIR 指向的路径：
```
echo %COPT_LICENSE_DIR%
```
- 若终端无输出，则表示COPT相关环境变量还未配置好
- 授权文档 license.dat 和 license.key 移动到 COPT_LICENSE_DIR 指向的路径下
