一、 Ubuntu 18.04.2安装 2.然后选择典型安装，点击下一步

3.先把安装程序光盘映像文件选择好（尽量不要在中文目录下），然后选择稍后安装操作系统

客户机操作系统选择Linux，版本选择Ubuntu 64位

5.虚拟机名称自己命名，位置选择一个空间足够大的盘符，至少8GB，文件目录不要有中文，不要放在根目录

6.指定磁盘大小，没有建议，默认20GB就够用了，并将虚拟磁盘拆分成多个文件

7.下一步之后不要急着点完成，点击自定义硬件

8.将虚拟机内存改为2GB，因为1GB会很卡，但是不能太大，需要从主机电脑占用内存给虚拟机使用

9.然后进入CD/DVD选项，将启动时连接前面的勾选一定要打开，然后使用ISO映像文件选择刚刚第3步选择的映像文件

10.好了之后点击关闭，会回到第7步的样子，点击完成就行

11.接下来就可以打开ubuntu了，点击开启此虚拟机

12.开机后会出现一段代码，只要不是not found之类的就行了，比如这样的就是可以的

13.等待开机后会出现语言选项，滚动到最下面选择中文简体（如果你喜欢英文我就不管了），点击安装Ubuntu

14.之后是键盘布局，默认汉语就行了，点击继续

15.勾选正常安装和下载更新

16.清除整个磁盘并安装

17.允许将改动写入磁盘，点击继续

18.稍微等待一会儿，虚拟机下面对弹出 对话框，提示“安装tools”，不要点，也不要关闭， 留作参考，如果关闭了也没事，可以在开机之后从 虚拟机打开，如图

19.然后选择地点，默认是shanghai（上海）不用改动，继续就行

20.设置用户名和密码，可以自动登录也可以输入密码登录，后期可以修改，密码不用太复杂

21.出现安装页面就可以等待，时间还是挺久的

22.文件比较多，下载的可能会有些慢，大约有147个文件半个小时左右，快的话十几分钟

23.安装完成，甚是欢喜，不要点击现在重启，直接关闭，然后关机

24.回到之前第9步的设置处，将启动时连接前面的勾选关闭，然后开机

25.提示进入界面，输入密码即可

到此，安装ubuntu教程结束，接下来是进行配置的教程


二、 Ubuntu国内源更新 

【问题】 安装Ubuntu 18.04后，使用国外源太慢了，修改为国内源会快很多。 

【处理】 修改阿里源为Ubuntu 18.04默认的源 备份/etc/apt/sources.list #备份 

cp /etc/apt/sources.list /etc/apt/sources.list.bak 

在/etc/apt/sources.list文件前面添加如下条目 

#添加阿里源 

deb http://mirrors.aliyun.com/ubuntu/ bionic main restricted universe multiverse 

deb http://mirrors.aliyun.com/ubuntu/ bionic-security main restricted universe multiverse 

deb http://mirrors.aliyun.com/ubuntu/ bionic-updates main restricted universe multiverse 

deb http://mirrors.aliyun.com/ubuntu/ bionic-proposed main restricted universe multiverse 

deb http://mirrors.aliyun.com/ubuntu/ bionic-backports main restricted universe multiverse 

deb-src http://mirrors.aliyun.com/ubuntu/ bionic main restricted universe multiverse 

deb-src http://mirrors.aliyun.com/ubuntu/ bionic-security main restricted universe multiverse 

deb-src http://mirrors.aliyun.com/ubuntu/ bionic-updates main restricted universe multiverse 

deb-src http://mirrors.aliyun.com/ubuntu/ bionic-proposed main restricted universe multiverse 

deb-src http://mirrors.aliyun.com/ubuntu/ bionic-backports main restricted universe multiverse 

最后执行如下命令更新源 

##更新 

sudo apt-get update 

sudo apt-get upgrade 

另外其他几个国内源如下： 

中科大源 ##中科大源 

deb https://mirrors.ustc.edu.cn/ubuntu/ bionic main restricted universe multiverse 

deb-src https://mirrors.ustc.edu.cn/ubuntu/ bionic main restricted universe multiverse 

deb https://mirrors.ustc.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse 

deb-src https://mirrors.ustc.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse 

deb https://mirrors.ustc.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse 

deb-src https://mirrors.ustc.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse 

deb https://mirrors.ustc.edu.cn/ubuntu/ bionic-security main restricted universe multiverse 

deb-src https://mirrors.ustc.edu.cn/ubuntu/ bionic-security main restricted universe multiverse 

deb https://mirrors.ustc.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse 

deb-src https://mirrors.ustc.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse 

163源 ##163源 

deb http://mirrors.163.com/ubuntu/ bionic main restricted universe multiverse 

deb http://mirrors.163.com/ubuntu/ bionic-security main restricted universe multiverse 

deb http://mirrors.163.com/ubuntu/ bionic-updates main restricted universe multiverse 

deb http://mirrors.163.com/ubuntu/ bionic-proposed main restricted universe multiverse 

deb http://mirrors.163.com/ubuntu/ bionic-backports main restricted universe multiverse 

deb-src http://mirrors.163.com/ubuntu/ bionic main restricted universe multiverse 

deb-src http://mirrors.163.com/ubuntu/ bionic-security main restricted universe multiverse 

deb-src http://mirrors.163.com/ubuntu/ bionic-updates main restricted universe multiverse 

deb-src http://mirrors.163.com/ubuntu/ bionic-proposed main restricted universe multiverse 

deb-src http://mirrors.163.com/ubuntu/ bionic-backports main restricted universe multiverse 

清华源 ##清华源 

deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic main restricted universe multiverse 

deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic main restricted universe multiverse 

deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse 

deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse 

deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse 

deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse 

deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-security main restricted universe multiverse 

deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-security main restricted universe multiverse 

deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse 

deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse


三、 解决 pip install -r requirement.txt 太慢问题 windows环境： 

1. 位置：用户文件夹中，单独某一个用户文件夹或管理员文件夹 　　

　　2. 创建一个名为：pip.ini的文件，在文件中设置新的镜像源　　　
　　3.  
  [global] index-url = http://mirrors.aliyun.com/pypi/simple/ 
  
  [install] trusted-host=mirrors.aliyun.com 　　
  
  镜像地址推荐： 　　　　
  
  阿里云 http://mirrors.aliyun.com/pypi/simple/ 　　
  
  中国科技大学 https://pypi.mirrors.ustc.edu.cn/simple/ 　
  
  豆瓣(douban) http://pypi.douban.com/simple/ 　　　　
  
  清华大学 https://pypi.tuna.tsinghua.edu.cn/simple/
  

　　3. 操作完成，再去安装依赖
　　4. 
  pip install -r requirements.txt
  

Linux 环境： 　　（未经过测试） 　　

1.新建目录及文件～/.pip/pip.conf 　　

2.内容为： 　　　　

[global] 　　　　index-url = https://pypi.tuna.tsinghua.edu.cn/simple 　　　

[install] 　　　　trusted-host=mirrors.aliyun.com


四、 安装VM-Tool 安装open -vm-tools


sudo apt install open-vm-tools sudo apt install open-vm-tools-desktop


五、 安装CMake 3.12 

1、卸载旧版cmake: $ sudo apt-get autoremove cmake 

2、文件下载：$ wget https://cmake.org/files/v3.12/cmake-3.12.2-Linux-x86_64.tar.gz 

3、解压：$ tar zxvf cmake-3.12.2-Linux-x86_64.tar.gz 

4、创建软连接：先检查解压后的cmake文件路径，我的在home/wml下: $ sudo ln -sf /home/wml/cmake-3.12.2-Linux-x86_64/bin/* /usr/bin/ 

5. 能检查出cmake --version说明cmake安装成功: $ cmake --version
6. 


六、 Milvus安装



源码安装 git clone https://github.com/milvus-io/milvus.git 

指定版本：git clone -b v0.10.2 https://github.com/milvus-io/milvus.git 

Requirements Operating system Ubuntu 18.04 or higher CentOS 7 Note: If your Linux operating system does not meet the requirements, we recommend that you pull a Docker image of Ubuntu 18.04 or CentOS 7 as your compilation environment. GCC 7.0 or higher to support C++ 17 CMake 3.12 or higher Git For GPU-enabled version, you will also need: CUDA 10.0 or higher NVIDIA driver 418 or higher Compilation Step 1 Install dependencies Install in Ubuntu $ cd [Milvus root path]/core $ ./ubuntu_build_deps.sh Install in CentOS $ cd [Milvus root path]/core $ ./centos7_build_deps.sh Step 2 Build $ cd [Milvus root path]/core $ ./build.sh -t Debug or $ ./build.sh -t Release By default, it will build CPU-only version. To build GPU version, add -g option. $ ./build.sh -g If you want to know the complete build options, run the following command. $./build.sh -h When the build is completed, everything that you need in order to run Milvus will be installed under [Milvus root path]/core/milvus. Launch Milvus server $ cd [Milvus root path]/core/milvus Add lib/ directory to LD_LIBRARY_PATH $ export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:[Milvus root path]/core/milvus/lib Then start Milvus server: $ cd scripts $ ./start_server.sh To stop Milvus server, run: $ ./stop_server.sh Compile Milvus on Docker With the following Docker images, you should be able to compile Milvus on any Linux platform that runs Docker. To build a GPU supported Milvus, you need to install NVIDIA Docker first. Step 1 Pull Milvus Docker images Pull CPU-only image: $ docker pull milvusdb/milvus-cpu-build-env:latest Pull GPU-enabled image: $ docker pull milvusdb/milvus-gpu-build-env:latest Step 2 Start the Docker container Start a CPU-only container: $ docker run -it -p 19530:19530 -d milvusdb/milvus-cpu-build-env:latest Start a GPU container: For nvidia docker 2: $ docker run --runtime=nvidia -it -p 19530:19530 -d milvusdb/milvus-gpu-build-env:latest For nvidia container toolkit: docker run --gpus all -it -p 19530:19530 -d milvusdb/milvus-gpu-build-env:latest To enter the container: $ docker exec -it [container_id] bash Step 3 Download Milvus source code Download latest Milvus source code: $ cd /home $ git clone https://github.com/milvus-io/milvus To enter its core directory: $ cd ./milvus/core Step 4 Compile Milvus in the container If you are using a CPU-only image: run build.sh: $ ./build.sh -t Release Start Milvus server： $ ./start_server.sh If you are using a GPU-enabled image: Add cuda library path to LD_LIBRARY_PATH: $ export LD_LIBRARY_PATH=/usr/local/cuda/lib64:$LD_LIBRARY_PATH Add cuda binary path to PATH: $ export PATH=/usr/local/cuda/bin:$PATH Add a -g parameter to run build.sh: $ ./build.sh -g -t Release Start Milvus server： $ ./start_server.sh Troubleshooting Error message: protocol https not supported or disabled in libcurl Follow the steps below to solve this problem: Make sure you have libcurl4-openssl-dev installed in your system. Try reinstalling the latest CMake from source with --system-curl option: $ ./bootstrap --system-curl $ make $ sudo make install If the --system-curl command doesn't work, you can also reinstall CMake in Ubuntu Software on your local computer. Error message: internal compiler error Try increasing the memory allocated to Docker. If this doesn't work, you can reduce the number of threads in CMake build in [Milvus root path]/core/build.sh. make -j 8 install || exit 1 # The default number of threads is 8. Note: You might also need to configure CMake build for faiss in [Milvus root path]/core/src/index/thirdparty/faiss. Error message: error while loading shared libraries: libmysqlpp.so.3 Follow the steps below to solve this problem: Check whether libmysqlpp.so.3 is correctly installed. If libmysqlpp.so.3 is installed, check whether it is added to LD_LIBRARY_PATH. CMake version is not supported Follow the steps below to install a supported version of CMake: Remove the unsupported version of CMake. Get CMake 3.12 or higher. Here we get CMake 3.12. $ wget https://cmake.org/files/v3.12/cmake-3.12.2-Linux-x86_64.tar.gz Extract the file and install CMake. $ tar zxvf cmake-3.12.2-Linux-x86_64.tar.gz $ mv cmake-3.12.2-Linux-x86_64 /opt/cmake-3.12.2 $ ln -sf /opt/cmake-3.12.2/bin/* /usr/bin/
