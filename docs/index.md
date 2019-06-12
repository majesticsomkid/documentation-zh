
# 文档简介

+ 关于波场概览，请查看[波场概览](Tron-overview.md)
+ 关于波场虚拟机，请查看[波场虚拟机](Tron-VM.md)
+ 关于波场HTTP接口，请查看[波场HTTP接口](Tron-http.md)
+ 关于波场RPC接口，请查看[波场RPC接口](Tron-rpc.md)
+ 关于波场官方公共节点IP地址，请查看[波场官方公共节点IP地址](official-public-nodes.md)
+ 关于波场节点部署，请查看[波场节点部署](Tron-deployment.md)

# Tips简介
+ [波场钱包提议](https://github.com/tronprotocol/TIPs/blob/master/tip-01.md)  
+ [波场通证标准](https://github.com/tronprotocol/TIPs/blob/master/tip-10.md)  
+ [波场事件订阅模型](https://github.com/tronprotocol/TIPs/blob/master/tip-12.md)  
+ [波场账户设计](https://github.com/tronprotocol/TIPs/blob/master/tip-13.md)    
+ [波场多重签名](https://github.com/tronprotocol/TIPs/blob/master/tip-16.md)  
+ [波场资源限制调整模型](https://github.com/tronprotocol/TIPs/blob/master/tip-17.md)  
+ [TRC-20通证标准](https://github.com/tronprotocol/TIPs/blob/master/tip-20.md)  
+ [用RocksDB实现DB存储](https://github.com/tronprotocol/TIPs/blob/master/tip-24.md)  
+ [时间订阅中的内置消息队列](https://github.com/tronprotocol/TIPs/blob/master/tip-28.md)  
+ [时间订阅模型支持无ABI的合约](https://github.com/tronprotocol/TIPs/blob/master/tip-34.md)

# 成为波场社区开发者

波场是个全球的，开源的去中心化应用的平台。

非常感谢你帮助我们开发源代码！我们欢迎和感激来自互联网的任何人的贡献，即使是很小的漏洞修复！

GitHub是用来追踪议题，贡献代码、建议、特性请求、文档等。

如果你想参与波场开发，请遵循流程：fork，fix，commit，send a pull request (PR)，以供波场主要维护者审查并且合并到主分支。如果你想提交更复杂的改动，为了保证你的改动符合我们的项目需求或者使你的改动更有效，请先通过我们的通信频道与我们的核心开发者确认。

我们鼓励尽早提交PR，这样可以让其他社区开发者知道你在开发的议题。未开发完成的PR需要被标注“进行中”状态。

** 社区开发者频道 **

* [Discord](https://discord.gg/GsRgsTD)   
* [Gitter](https://gitter.im/tronprotocol/allcoredev)   

## 如何参与波场文档的书写

我们有两个文档仓库：  
[英文文档](https://github.com/tronprotocol/documentation-EN)     
[中文文档](https://github.com/tronprotocol/documentation-ZH)     

我们使用MkDocs框架来构建我们的文档项目。文档使用Markdown语言书写，通过在YAML配置文件中配置文档路径。

你可以在/docs/文件夹下，修改、添加文档。

## 如何参与TIP书写

波场优化提议(TIPs) 描述了波场平台的标准，包括协议说明、客户端接口、合约标准等等。

TIPS仓库路径是：[https://github.com/tronprotocol/TIPs](https://github.com/tronprotocol/TIPs)

你提交的第一个TIP PR应该是最终TIP的一个草案，必须要符合我们要求的格式。我们会审核你提交的TIP，并且会为之分配一个编号。请确保在TIP页头中附上论坛的地址或者一个公开的GitHub议题地址来让用户进行讨论。    
请参考：[TIP模板](https://github.com/tronprotocol/TIPs/blob/master/template.md)


## 如何参与java-tron代码书写

**分支介绍：**

``master``分支：  
这个分支包含最近发布到生成环境的代码，并通过Tag进行标注release版本号，这个分支只能从其他分支合并，不能在这个分支直接修改。

``develop``分支：  
这个分支是我们的主开发分支，包含所有要发布到下一个release的代码，这个分支只能从其他分支合并，不能在这个分支直接修改。

``feature``分支：  
这个分支主要是用来开发一个新的功能，基于``develop``分支创建，一旦开发完成，就会将其合并回``develop``分支，并将其删除。

``release``分支：
预发布分支，当你需要发布的时候，基于``develop``分支创建一个release分支，允许小修复和最终版本元数据（版本号等）修改，从``develop``分支到``release``分支的关键点是开发完成反映新版本的期望状态。至少合并了所有针对要发布的功能，针对未来版本的所有功能不会被合并-他们必须等到Release分支创建完成后才可以被合并。完成release后，将其合并到``master``分支（需要打Tag）和``develop``分支，并将其删除。上线前最后的测试将在这个分支进行。

``hotfix``分支：
当我们在``master``分支发现bug的时候，需要基于``master``分支创建一个hotfix分支，完成hotfix后，将其合并到``master``分支（当做一个新的release）和``develop``分支，并将其删除。

**开发一个新功能**  
  
当你开始开发新功能时，从``develop``分支创建一个feature分支，分支需要位于``origin/feature``下。  

**修复线上漏洞**  
     
当你发现一个发布版的Bug时，从``master``分支（此时应该是最新release代码）创建一个hotfix分支，分支需要位于``origin/hotfix``下。

最后，请提交一个PR。

补充说明：如果你开发了新功能，请确保你在``/src/test``目录中添加了测试用例。