
### 日志文件
- ​**路径**: 安装目录下的 `log.txt`
- ​**作用**: 记录软件运行状态和错误信息，异常时需优先检查此文件。

---

### 名词解释及注意事项

#### 字符编码
- ​**要求**: 所有文件必须采用 `UTF-8` 编码，异常时需首先检查编码格式。

#### 运动链
- ​**标准定义**: 两个及以上构件通过运动副联接的可动系统。
- ​**软件定义**:
  - ​**串联结构**: 用 `->` 连接，节点运动会影响后续节点（如 `X->Z->C->A`）。
  - ​**并联结构**: 用 `;` 连接，节点运动独立（如 `Y;V`）。
  - ​**组合结构**: 可混合使用（如 `Y和X->Z->C->A;V`）。

#### 轴ID
- ​**作用**: 数控系统通过ID区分机械轴。
- ​**对照表**:

| 机械轴名称 | X   | Y/V | Z   | C   | A   |
|------------|-----|-----|-----|-----|-----|
| ID         | 1   | 2   | 3   | 4   | 5   |

---

### 输入G代码格式
- ​**正确格式**:  
  `X1.123 Y0.53 Z-0.551 A15.320 C-0.32`（保留前导0，无空格）
- ​**错误格式**:  
  `X1.123 Y 53 Z-551 A15.320 C-32`（坐标值格式错误）

---

### 程序段处理
1. ​**标识符设置**:
   - 在 `data/uniquelyIdentifies.json` 中定义 `"section":";SECTION"`，软件根据此标识分割程序段。
2. ​**程序段格式**:
   - ​**第1行**: 必须包含刀具信息，如 `(TD=10.00 TR=5.0...)`。
   - ​**第2行**: 必须输出全坐标值，如 `G0 X100 Y-200 Z-0.35 C-51.56 A11.15`。

---

### 坐标系
- ​**类型**:
  - 世界坐标系 (WCS)：绝对基准，位于AC轴交叉点。
  - 工件坐标系 (MCS)：对应G54~G59。
  - 用户坐标系 (UCS)：用户自定义。
  - 机械坐标系 (MCS)：机床固有坐标系。

---

### 配置文件说明（节选）
#### 机器参数
- ​**运动链**: 定义轴结构（如 `X->Z->C->A;Y`）。
- ​**NC轴参数**:
  - ​**名称**：需与机械轴名称一致。
  - ​**ID**：参考轴ID对照表。
  - ​**位置**：用于AC轴机型的世界坐标系补偿。

#### 插补参数
| 参数名         | 值      | 说明                  |
|----------------|---------|-----------------------|
| 插补周期       | 4ms     | 时间间隔，建议≤10ms   |
| 快速阈值       | 70000   | G0最大允许速度(mm/s)  |

---

## 用户篇

### 操作流程
1. ​**用户坐标系设定**  
   - 修改值或导入模型（STL格式需对齐MCS）。
2. ​**夹具设定**  
   - 导入夹具并自动调整位置，生成ISO代码验证。
3. ​**刀具设定**  
   - 新建/编辑刀具，匹配程序中的刀具参数。
4. ​**导入程序**  
   - 选择NC文件，检查刀具匹配和坐标系。
5. ​**微调与模拟**  
   - 镜像、平移、偏置调整，碰撞检测。
6. ​**生成ISO**  
   - 输出代码并验证，符合要求后执行加工。

---

### 注意事项
- ​**提高G代码加载速度**: 采用主程序调用子程序方式，减少预读时间。
- ​**坐标系补偿**: AC轴机型的WCS补偿需写入A轴初始位置。

（注：由于篇幅限制，部分内容已简化。完整配置参数、视频链接及示例代码请参考原始文档。）