# 常见问题解答

## 主轴预启动逻辑

---

 ```ini
 [StatusPreProcessing]
 PreLaunchTime=10.0        ; 主轴预启动时间
 IsPreLaunch=true          ; 是否开启主轴预启动
 PostProcessor=UserPostProcessor/Post_Processor.xml  ; 后处理器定义标签
 TrajAlgorithem=0
 TrajAlgorithemOptimal=3
 ToleranceBlend=2.0
 ToleranceBlendOptimal=100.0
 CollisionObject=0.99
 ``` 

 ---