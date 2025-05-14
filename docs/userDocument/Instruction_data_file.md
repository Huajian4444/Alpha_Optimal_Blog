# data.ini文件详解

>文件路径:软件安装路径下.它负责定义软件的默认操作

```
文件内容如下:

[StatusPreProcessing]
PreLaunchTime=10.0     
IsPreLaunch=true
PostProcessor=UserPostProcessor/QCM-AC.xml
IsAdaptiveEnabled=false
AdaptiveThreshold=50000

[MainInterface]
BackGroundColor=0.67 0.67 0.50
TabPosition=North
DockWidgetArea=0x1
IsDockWidgetFloatting=false
Language=Chinese
DefaultPath=E:/\x9752\x57ce\x673a\x68b0/\x4eff\x771f/\x7a0b\x5e8f\x6d4b\x8bd5
IsNewToolDialog=true
IsShow3DViewerDecoration=false

[UserData]
TemplatePath=

[Config]
UsedConfig=machineSample/DX_Demo.xml

[MotionNode]
StopWhenTheSpindleStatusChanges=false
IsRepeatNodesEnable=false
AxisNodeRepeatTransformations=1000 0 0
AxisNodeRepeatCount=1 1 1 1
AxisNodeRepeatNames=X Z C A

[DebugFunction]
IsAllowReadIsoCode=false
IsShowAxisInfo=false


```
## StatusPreProcessing 标签详解

[StatusPreProcessing]
PreLaunchTime=10.0      # 主轴预启动时间 10s    
IsPreLaunch=true        # 是否开启主轴预启动    
PostProcessor=UserPostProcessor/QCM-AC.xml      # 定义当前使用的后处理器路径    
IsAdaptiveEnabled=false     #默认设置   
AdaptiveThreshold=50000     #默认设置   



##  MainInterface 标签详解

- [MainInterface]
- BackGroundColor=0.67 0.67 0.50  #3D视口的背景颜色   
- TabPosition=North  
  - 取值范围:
    - North
    - South
    - West
    - East  
    - ![Tab默认的位置](../image/data_images/TabWidget默认的位置.png)


- DockWidgetArea=0x1  #默认设置   
- IsDockWidgetFloatting=false #默认设置   

- Language=Chinese    #界面语言 
  - 取值范围
      - Chineses
      - English
      - Russia
      - 可以在软件内设定 一般不在这里修改。`设置->设置界面语言`


- DefaultPath=E:/\x9752\x57ce\x673a\x68b0/\x4eff\x771f/\x7a0b\x5e8f\x6d4b\x8bd5
  - 默认打开路径
  - 在软件内设定,`设置->UserDir`
  
- IsNewToolDialog=true
  - true：
  - false:

- IsShow3DViewerDecoration=false
  - true：
  - false:

##  Config 标签详解
- [Config]
- UsedConfig=machineSample/DX_Demo.xml #当前使用的配置文件