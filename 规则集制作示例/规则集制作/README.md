# 智能家居规则集制作规则
---------------------
## 规则集建立须知
  > 1. 规则集制作类型为*.vsdx
  > 2. 模板为“公有资料\/EPN构建模具.vssx”和“公有资料\/EPA构建模具.vssx”
  > 3. 涉及传感器更改的变更于“公有资料\/传感器定位.vsdx”
  > 4. 涉及事件聚合的变更于“规则集制作\/EPN.vsdx”
  > 5. 涉及规则集的变更于“规则集制作\/\*.vsdx”，使用的UML语言为状态机
## 步骤
  > 1. 更新自己所在分支
  > 2. 变更“传感器定位.vsdx”
  > > * 添加传感器与传感器注释（位置与编号）
  > > * 编号规则：传感器类型+房间号\[+‘-’+第几个\]，例如：D3  W2-3
  > 3. 变更“EPN.vsdx”
  > > * 加入EPA，连接所需的输入输出事件
  > > * 如果需要新的传感器变量，则在“规则集制作\/EPN.vsdx”于特定传感器页加入数据类型
  > > * 如果所需传感器页不存在，则在“规则集制作\/EPN.vsdx”加入特定传感器页
  > > * 如果生成新的事件，则添加到特定中间件层
  > > * 如果需要新建中间件层，则添加并给出中间件层标号
  > > * 如果生成事件包含新的变量，则加入到“公有资料\/数据定义.accdb”
  > > * 如果生成新的指令，则在“规则集制作\/EPN.vsdx”于可控单元页加入数据类型
  > > * 如果所需可控单元页不存在，则在“规则集制作\/EPN.vsdx”加入特定可控单元页
  > 4. 变更规则集
  > > 1. 不同EPA的编辑在不同文件进行
  > > 2. 如果EPA需要新建，则在规则集制作目录下新建文件，命名格式为：
  > > > * 所对应中间件编号数\-EPA\-EPA序号，例如：某EPA位于3号中间件下方，位于第4位，则有：3\-EPA\-4
  > 5. 制作完成后，查看master分支更新状态，如果master没有在你制作规则集的过程中变化，则直接并入master，如果有人在期间更新master，则需再次更新自己的分支重新编辑文件上传
