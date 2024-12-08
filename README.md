

> Json Assistant 是基于 IntelliJ IDEs 的 JSON 工具插件，让 JSON 处理变得更轻松！


# 主要功能


* 完全支持 [JSON5](https://github.com)
* JSON 窗口（多选项卡）
	+ 选项卡更名
	+ 移动至主编辑器
	+ 用新窗口打开选项卡内容
	+ JSONPath 查询
	+ 历史记录
	+ JSON 导出
* JSON 格式化
* JSON 压缩
* JSON 结构化（树视图）
* JavaBean 转换为 JSON
* JSON 转换为 JavaBean
* Kotlin 属性转为 JSON
* JSON 文本比对
* JSON 转义
* Java 常量提取为 JSON
* 格式转换
	+ JSON \<\-\> XML
	+ JSON \<\-\> YAML
	+ JSON \<\-\> TOML
	+ JSON \<\-\> Properties
	+ JSON \<\-\> URL Param


# 使用



> 在此简单介绍功能的使用，详情请查看 [插件文档](https://github.com)。


## Json 格式化、压缩


1. 当编辑器中 仅包含 JSON 文本或 选中了 有效的 JSON 文本。
2. 单击鼠标右键，并选择 **Json Assistant**（或按下快捷键 `Alt+K`）。
3. 接着选择 `Json Beautify` 或 `Json Minify…`，对应格式化与压缩。


* `在可编辑的文件中` ：格式化（压缩）结果将直接插入到当前光标位置。
* `在不可编辑的文件中` ：格式化（压缩）结果将展现在右侧 JSON 窗口中。


![](https://img2024.cnblogs.com/blog/3464480/202412/3464480-20241206215237771-1597868148.gif)
## Json 结构化（树视图）



> 将 JSON 文本转换为 **树状结构**，并提供属性、数量等信息。


1. 当编辑器中 仅包含 JSON 文本或 选中了 有效的 JSON 文本。
2. 单击鼠标右键，并选择 **Json Assistant**（或按下快捷键 `Alt+K`）。
3. 接着选择 `Json Tree Structure`，将弹出一个 JSON 树结构的窗口。


![](https://img2024.cnblogs.com/blog/3464480/202412/3464480-20241206215252306-1665005119.png)
### 文本检索



> JSON 树支持文本检索，能够快速查找键名、值及嵌套对象中的内容。


**使用：** 按下 `Ctrl+F` 或直接键入字符。


![](https://img2024.cnblogs.com/blog/3464480/202412/3464480-20241206215341926-1522261156.png)
## JavaBean 转换为 Json



> 将 JavaBean 序列化为 JSON ，支持 **嵌套属性** ，支持 **FastJson**、 **Jackson** 注解。


**使用：** 在 **Java** 类中，单击鼠标右键，并选择 `Convert to JSON`（或快捷键 `Alt+N`）


* `当鼠标光标位于主类的范围时`：将解析主类的属性为 JSON。
* `当鼠标光标位于内部类的范围时`：将解析该内部类的属性为 JSON。


![](https://img2024.cnblogs.com/blog/3464480/202412/3464480-20241206215402293-1327840336.png)
## Json 转换为 JavaBean



> 将 JSON / JSON5 反序列化为 JavaBean，支持嵌套 Array 、 Object 属性。


**使用：** 选择一个 **Java** 包，单击鼠标右键，并选择 `New` \> `Java Class from Json`。


![](https://img2024.cnblogs.com/blog/3464480/202412/3464480-20241206215413158-1838947047.gif)
## Json 窗口



> 用于展示及处理 JSON 的侧边窗口，支持多选项卡、历史记录、JSONPath 查询等多项能力。


**使用：** 在 IDE 主界面的右侧，找到 `Json Assistant` 窗口，点击打开。


### 多选项卡


在多选项卡的情况下，能同时记录和处理不同的 JSON 数据。


![](https://img2024.cnblogs.com/blog/3464480/202412/3464480-20241206215433129-2082880778.png)
### 新窗口打开选项卡内容


在 IDE 新窗口中处理 JSON 数据，不受 IDE 原本窗口的限制，更便于调试。


### JSONPath 查询


支持 [JSONPath](https://github.com) ，实现精准的元素定位与高效的数据过滤。


![](https://img2024.cnblogs.com/blog/3464480/202412/3464480-20241206215440982-1926119058.png)
### 历史记录


记录编辑器中的 JSON 数据，用于查看和恢复。



> 默认使用 **树状视图** （按时间分组）展示历史记录。
> 
> 
> 可在 `Settings/Preferences` \> `Tools` \> `Json Assistant` 配置项中切换为 **列表视图**。


![](https://img2024.cnblogs.com/blog/3464480/202412/3464480-20241206215449031-1494701299.png)
### 识别剪贴板内其他格式文本


进入窗口时，编辑器会自动检测剪贴板中的文本是否符合以下任一格式。


若符合，则将其转换为 JSON 格式并填充到编辑器中（**只限于初始选项卡**）。



> 可在 `Settings/Preferences` \> `Tools` \> `Json Assistant` 配置项中指定开关。




| 格式名称 | 是否支持 |
| --- | --- |
| **XML** | √ |
| **YAML** | √ |
| **TOML** | √ |
| **URL Param** | √ |


### 外观调整


自定义 JSON 编辑器的外观设置，包括启用或禁用行号显示、代码折叠功能，以及选择背景颜色。



> 在 `Settings/Preferences` \> `Tools` \> `Json Assistant` 配置项中指定开关。


![](https://img2024.cnblogs.com/blog/3464480/202412/3464480-20241206215506038-669108475.png)
## Json 文本比对



> 对比两份 JSON 文本的差异，高亮显示不同之处。


![](https://img2024.cnblogs.com/blog/3464480/202412/3464480-20241206215521387-2145393057.png)
## Json 转义



> 对 JSON / JSON5 进行转义处理，且插件已默认提供自动去除转义的能力。
> 
> 
> *转义后，默认会将转义结果复制到剪贴板，并在窗口中显示保留换行符的转义结果，便于查看*。


1. 当编辑器中 仅包含 JSON 文本或 选中了 有效的 JSON 文本。
2. 单击鼠标右键，并选择 **Json Assistant**（或按下快捷键 `Alt+K`）。
3. 接着选择 `Json Escape…`，对 JSON 进行转义处理。


![](https://img2024.cnblogs.com/blog/3464480/202412/3464480-20241206215527247-1531952522.gif)
## 格式转换



> 提供 JSON / JSON5 与多种其他格式之间的转换功能。




| 格式 | 是否支持 |
| --- | --- |
| **JSON5** | √ |
| **XML** | √ |
| **YAML** | √ |
| **TOML** | √ |
| **Properties** | √ |
| **URL Param** | √ |


### JSON 转为其他格式


1. 当编辑器中仅包含 JSON 文本或选中了有效的 JSON 文本。
2. 单击鼠标右键，并选择 **Json Assistant**（或按下快捷键 `Alt+K`）。
3. 接着选择 `Convert to…`，选择要转换的格式。



> 图为 JSON5 转换为其他格式。


![](https://img2024.cnblogs.com/blog/3464480/202412/3464480-20241206215542448-1443706902.png)
### 其他格式转为 JSON


1. 当编辑器中仅包含 **有效的格式内容** 或选中了 **有效的有效的格式内容**。
2. 单击鼠标右键，并选择 **Convert xxx to JSON**（或按下快捷键 `Alt+P`）。


![](https://img2024.cnblogs.com/blog/3464480/202412/3464480-20241206215549276-820284089.png)

> 当 YAML 中存在多文档，则需要选择一份文档进行转换。


![](https://img2024.cnblogs.com/blog/3464480/202412/3464480-20241206215553949-1829869596.gif)
# 安装


## 使用 IDE 内置插件系统安装（推荐）


进入 `Settings/Preferences` \> `Plugins` \> `Marketplace` \> 搜索 `Json Assistant` \> `Install`


![](https://img2024.cnblogs.com/blog/3464480/202412/3464480-20241206215600877-500787595.png)
## 手动下载插件安装


* 在 [JetBrains Marketplace](https://github.com):[FlowerCloud机场节点订阅](https://dahelaoshi.com)  或  [GitHub Releases](https://github.com) 下载与你 IDE 版本兼容的插件包
* 进入 IDE，打开 `Settings` \> `Plugins` \> `⚙` \> `Install Plugin from Disk...` ，选择刚才下载的插件包并安装即可（无需解压压缩包）


![](https://img2024.cnblogs.com/blog/3464480/202412/3464480-20241206215605649-1525785789.png)
# 项目地址


* Github：[https://github.com/MemoryZy/Json\-Assistant](https://github.com)
* 插件文档：[https://json.memoryzy.cn/overview](https://github.com)


# 兼容产品


* Android Studio — Arctic Fox \| 2020\.3\.1\+
* AppCode — 2020\.3\+
* Aqua — 2024\.1\.1\+
* CLion — 2020\.3\+
* Code With Me Guest — 1\.0\+
* DataGrip — 2020\.3\+
* DataSpell — 2021\.3\+
* GoLand — 2020\.3\+
* IntelliJ IDEA Community — 2020\.3\+
* IntelliJ IDEA Ultimate — 2020\.3\+
* JetBrains Client — 1\.0\+
* JetBrains Gateway — 2022\.2\+
* MPS — 2020\.3\+
* PhpStorm — 2020\.3\+
* PyCharm Community — 2020\.3\+
* PyCharm Professional — 2020\.3\+
* Rider — 2020\.3\+
* RubyMine — 2020\.3\+
* RustRover — 2024\.1\+
* WebStorm — 2020\.3\+
* Writerside — 2024\.1\+


