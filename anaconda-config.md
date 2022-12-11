conda config --set show_channel_urls yes

conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main

conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r

conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/msys2

conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud

conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud

conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud

conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud

conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud

conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud

conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud


conda create -n your_env_name python=x.x 创建虚拟环境，your_env_name为你给虚拟环境起的名字，x.x为指定的python的版本。

conda create --name python36 python=3.6


1、查看

查看虚拟环境列表

conda env list


2、激活

conda activate <环境名称>

例如，激活tensorflow_env环境

conda activate tensorflow_env


3、退出

退出虚拟环境

conda deactivate



4、删除环境

conda remove -n <环境名称> --all

或者

conda env remove -n <环境名称>


5、安装包

conda install <包名称>

例如：

conda install numpy


6、查看包列表

conda list


7、更新包

conda update <包名称>

例如：

conda update numpy

更新所有包

conda update --all


8、删除包

conda remove <包名称>

