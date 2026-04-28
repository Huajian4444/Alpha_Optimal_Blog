# 如何定位用户坐标系

## 前提:所有参数已经正确设定

## 如何获取**用户坐标系**的值
1. 测量到正确的刀具长度.![测量刀具长度](../../image/On-siteImages/MeasureToolLength.jpg)

2. 正确设置刀具.详见[正确设置刀具](../UserDocument/ToolManager_ZH.md)

3. 把工件固定在机器上面 ![固定工件](../../image/On-siteImages/WorkPieceFixed-1.jpg)

4. 将T1的刀尖移动到CAM编程时,对应的坐标系零点位置
      - ![编程时的坐标系位置](../../image/machine/编程原点.png)
      - ![工件坐标位置](../../image/On-siteImages/MCS-3.jpg)
      - ![刀尖在编程原点](../../image/On-siteImages/TipAlignedOrigin-3.jpg)
5. 记录轴坐标![机械轴位置](../../image/On-siteImages/AxisCoordinateValue-3.jpg)
6. 点击工具栏 → 通讯 ![通讯](../../image/communication.png)
7. 通讯界面 ![通讯界面](../../image/CommunicationWidget.png)
8. 确认工件坐标系
      - 左台面勾选 G54 ![G54](../../image/G54.png)
      - 右台面勾选 G55 ![G55](../../image/G55.png)
9.  确认:第4&5轴的角度为0(A0 C0)
      - ![Ax4](../../image/Ax_4.png)
      - ![Ax5](../../image/Ax_5.png)
10. 抄录机械坐标 将数控系统上的 **X Y Z** 坐标抄录到机械坐标系：`Ax_1 Ax_2 Ax_3` ![机械坐标系](../../image/CopyValueFromControlToSoftware.png)
    
11. 同步用户坐标系并选择要操作的用户坐标系Id
    - ![同步用户坐标系和选择id](../../image/sync_select_ucs.png)

12. 转用户坐标系 并 应用数值 
    - ![toUcsAndApply](../../image/to_ucs_btn.png)

