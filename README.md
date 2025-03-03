# COPT_init 在window和linux远程服务器中部署杉树科技的COPT优化器
---
## 一. 在本地 windows 中部署 COPT优化器
#### 1. 软件安装
- 推荐 下载可执行安装程序 （下载链接名称中含有 "installer"）
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


## 在linux远程服务器中部署 COPT优化器
#### 1. 在选定好的虚拟环境中下载COPT
```
pip install coptpy
```
#### 2. 软件安装
- 将CardinalOptimizer-7.2.1-lnx64.tar.gz 文件解压到用户目录（/home/mmy），则会在用户目录下出现copt72这个文件夹
```
tar -xzf CardinalOptimizer-7.2.1-lnx64.tar.gz
```

#### 环境变量
- 在终端执行下述命令切换到用户目录（/home/mmy）
```
cd  ~/
```
- 再执行下述命令查看是否存在 '.bashrc' 隐藏文件：
```
ls -a
```
- 若不存在该文件，则在终端上执行下述命令创建空的 '.bashrc' 文件：
```
touch ~/.bashrc
```
- 若已存在该文件，则用户可以使用任意文本编辑器编辑现有 '.bashrc' 文件，并添加如下内容,注意: 等号两边不能有空格。
```
export COPT_HOME=/home/mmy/copt72
export COPT_LICENSE_DIR=/home/mmy/copt72
export PATH=$COPT_HOME/bin:$PATH
export LD_LIBRARY_PATH=$COPT_HOME/lib:$LD_LIBRARY_PATH
```
- 保存上述修改并退出，用户可以在终端执行下述命令查看修改后的 '.bashrc' 文件：
```
cat ~/.bashrc
```
- 在终端输入下述命令使得上述环境变量修改生效。
```
source ~/.bashrc
```
- 最后分别输入下述命令检查COPT相关环境变量是否设置成功：
```
echo $COPT_HOME
echo $COPT_LICENSE_DIR
echo $PATH
echo $LD_LIBRARY_PATH
```
注：我并没有完全显示出来，但是程序能够运行



