# 授权与注册

## 操作步骤

1. **确认已安装 AlphaOptimal 软件**
2. **关闭 AlphaOptimal 软件**
3. **打开安装路径**
   - 一般路径为：`C:\Program Files\AlphaOptimal_v3`
4. **进入 `bin\UserIdGenerator` 文件夹**
   - ![授权文件生成器](../../image/授权文件生成器.png)
   - 运行 `GetUserData.exe`（以管理员身份运行），生成 `HostName.txt` 文件
   - 运行 `UserIdGenerator.exe`（以管理员身份运行），生成 `userId.txt` 文件
5. **发送文件**
   - 将 `HostName.txt` 和 `userId.txt` 文件发送给 `瑞凡软件公司` 制作授权
6. **接收授权文件**
   - `瑞凡软件公司` 会提供以下两个文件：
     - `HostName.lic` 授权文件
     - `AlphaOptimal...txt` 文件
7. **拷贝授权文件**
   - 将上述两个文件拷贝到软件安装路径下，与 `AlphaOptimal.exe` 文件保持同一路径（通常为 `C:\Program Files\AlphaOptimal_v3\bin`）
8. **打开 AlphaOptimal 软件**
   - 如果提示授权错误：
     1. ![授权错误](../../image/未授权错误.png)
     2. ![授权错误](../../image/选择授权文件.png)
9. **完成授权**

---

## 常见错误处理

### 错误 1: Windows 权限不足

**表现：**
- 选择授权文件后，软件再次打开时重复弹出选择授权文件窗口。
  - ![授权错误](../../image/未授权错误.png)

**解决方法：**
1. 找到软件安装路径（一般为 `C:\Program Files\AlphaOptimal_v3`），返回上一层。
2. 右键点击 `AlphaOptimal_v3` 文件夹。
   - ![授权错误](../../image/注册错误/AlphaOptimal_V3_属性.png)
3. 选择 `属性 -> 安全 -> 编辑`。
   - ![授权错误](../../image/注册错误/安全-编辑-勾选所有.png)
4. 勾选以下选项的“完全控制”：
   - ALL APPLICATION PACKAGES
   - 所有受限制的应用程序包
   - CREATOR OWNER
   - SYSTEM
   - Administrators
   - Users
   - TrustedInstaller
5. 点击“确定”。
   - ![授权错误](../../image/注册错误/权限-全部勾选.png)
   - ![授权错误](../../image/注册错误/权限-全部勾选-1.png)
6. 再次打开 AlphaOptimal 软件并选择授权文件，问题解决。

---

### 错误 2: PC 有多个 MAC 地址

**表现：**
- 软件闪退。
- 查看日志文件（路径：`C:\Program Files\AlphaOptimal_v3\bin\log.txt`），最后一行显示：`hasp not found`。

**解决方法：**
1. 获取网络信息：
   - ![网络界面](../../image/注册错误/网络界面.png)
   - ![网络界面](../../image/注册错误/网络界面2.png)
   - ![网络界面](../../image/注册错误/网络界面3.png)
   - ![网络界面](../../image/注册错误/网络界面4.png)
2. 将获取到的网络信息发送给 `瑞凡软件公司`。
3. `瑞凡软件公司` 会将信息添加到 `HostName.lic` 文件中。
4. 收到新的 `HostName.lic` 文件后，将其拷贝到 `C:\Program Files\AlphaOptimal_v3\bin` 进行替换。
5. 软件成功打开。
