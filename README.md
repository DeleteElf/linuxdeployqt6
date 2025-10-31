### 使用说明
```shell
#安装必须的软件
sudo apt -y install patchelf
#设置环境
export QT_ROOT=~/Qt/6.9.3/gcc_64
export PATH=$QT_ROOT/bin:$PATH
export LD_LIBRARY_PATH=$QT_ROOT/lib:$LD_LIBRARY_PATH
export QT_PLUGIN_PATH=$QT_ROOT/plugins:$QT_PLUGIN_PATH
export QML2_IMPORT_PATH=$QT_ROOT/qml:$QML2_IMPORT_PATH
#执行程序  案例
linuxdeployqt app target.AppRun -qmldir=$PWD/../../app/gui

linuxdeployqt app -qmldir=$PWD/../../app/gui

linuxdeployqt app -qmldir=$PWD/../../app/gui -no-plugins

linuxdeployqt CgTeamworkRD -qmldir=$PWD/../../app/gui -exclude-libs=libqsqlmimer,libqsqlmysql,libqsqlite,libqsqlodbc,libqsqlpsql
```

### 版本变更记录

#### 1.0.25.103101
1. 修改主入口，支持linux glibc版本到2.39。
2. 修改cmake版本到3.10。
3. 不再生成快捷方式。