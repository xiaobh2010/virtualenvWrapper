# virtualenvWrapper
virtualenvWrapper 虚拟环境管理工具
1 作用
    第三方的管理工具，能够快读、高效而且方便的管理虚拟环境
2 安装虚拟环境管理工具
    sudo pip3 install virtualenvwrapper
3 配置virtualenvwrapper
    在~目录下，有一个终端管理文件    .bashrc(在~目录下，输入ll)
    配置 .bashrc 以便在启动终端时，就自动启动虚拟环境管理工具
    修改.bashrc  ：sudo vi .bashrc
    在.bashrc最底部增加以下内容
    1 export WORKON_HOME=~/my_env
    将~/my_env作为虚拟环境的管理目录，所有使用virtualenvwrapper创建的虚拟环境都默认保存于此
    2 如果系统中包含多个python执行环境的话，则添加以下内容
    export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3
    3 source /usr/local/bin/virtulenvwrapper.sh
    4 在~目录下，执行一遍.bashrc
    source .bashrc
4 使用虚拟环境管理工具
    1 创建并进入虚拟环境    
        1 mkvirtualenv 虚拟环境名称  （直接进入虚拟环境，虚拟环境默认保存在my_env中）
            mkvirtualenv default
        2 mkvirtualenv --python=/usr/bin/python2.7 虚拟环境名称
    2 查看当前所维护的所有虚拟环境(在my_env路径下输入)
        workon
例子：
(env2.7) tarena@tedu:~/my_env$ workon
default
env2.7
env3.5

    3 切换虚拟环境
        workon 虚拟环境名称
        
    4 退出虚拟环境
        deactivate
    5 删除虚拟环境
        rmvirtualenv 虚拟环境名称
