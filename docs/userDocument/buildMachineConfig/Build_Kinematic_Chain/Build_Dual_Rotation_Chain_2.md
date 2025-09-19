# 新建运动链-第二步:新建配置文件


## 新建配置文件:采用复制->修改的方法

> 注意:显示文件拓展名

1. 打开软件的安装路径,根据机型复制对应的配置文件
      - 双台面：复制DoubleTable.xml并重命名Demo.xml
      - 单台面: 复制SingleTable.xml并重命名Demo.xml
      - 新建文件夹:Demo
      - 把第一步导出的所有STL文件拷贝到Demo文件夹
2. 打开AlphaOptimal软件:菜单栏 设置->重新选择运动模型.在弹出的对话框选择machineSample/Demo.xml 点击`确定` 软件自动重启
3. 开始编辑配置文件     
点击查看 [配置文件编辑器](../ConfigEditorInterface.md)

    - 机器参数 
    - 重点:     点击查看 [运动链和Id](../ChainAndAxisId.md)
        - 理解运动链:X->Z->C->A;Y & X->Z->C->A;U
    - 数控轴参数:
      - 重点:轴Id   点击查看 [运动链和Id](../ChainAndAxisId.md)


