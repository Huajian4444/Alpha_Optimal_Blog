# 从旧版本配置文件提取后处理器设定

本指南介绍如何从 3.3.0.5 或之前版本的配置文件中提取加工模式的设定。

## 操作步骤

1. **启动程序**  
   双击 `GeneratePostProcessorByConfigFile.exe`  
   ![启动程序](../image/ExtractByConfig/启动可执行文件.png)

2. **选择配置文件**  
   在弹出的选择框中选择旧的机床配置文件  
   ![选择机床配置文件](../image/ExtractByConfig/选择机床配置文件.png)

3. **转换提示**  
   等待程序提示 **转换成功**  
   ![转换成功提示](../image/ExtractByConfig/转换成功.png)

4. **查找生成的文件**  
   打开 `GenerateFiles` 文件夹，找到生成的后处理文件  
   ![生成文件的路径](../image/ExtractByConfig/生成文件的路径.png)

5. **编辑后处理器文件**  
   使用记事本打开后处理器文件。  
   根据 **[用户后处理](../userDocument/PostProcessor.md)** 文档中 **详解: Regulation** 的说明，对文件中的标定进行修改。

6. **完成设置**  
   修改完成后，将文件拷贝到 `UserPostProcessor` 文件夹内。

7. **调用后处理器**  
   最后，根据 **[用户后处理](../userDocument/PostProcessor.md)** 文档中的 **调用** 部分调用后处理器。
