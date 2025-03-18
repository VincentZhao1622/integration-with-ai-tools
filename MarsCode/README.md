# MarsCode调查

## 1. MarsCode总览

* 调查时间 ： 2025年3月6日

 | Feature  | Comments |
 | -------- | -------- |
 | 费用     | 免费 |
 | 默认LLM  | DouBao/DeepSeek |
 | IDE支持  | Vscode/idea插件支持 |
 | 编程支持  | 对话/自动补全   |
 | VPN?     | 不需要     |
 | 中文支持  | 好        |  

## 2. 调研Use case 1, JAVA后端 + PayPal javasdk(v2)

* IDE: IntelliJ IDEA 2024.3.4 (Community Edition)
* 插件： IDEA github MarsCode - 1.5.37版本
* JAVA版本： 21
* 代码使用清单：

  | No.  | Name     | Comments |
  | ---- | -------- | -------- |
  | 1    | OrderVO.java | 模拟商户网站原有数据模型 |
  | 2    | OrdersRequest.java | PayPal javasdk中调研CreateOrder接口使用的业务数据模型 |
  | 3    | CreateOrderDetailed.json | PayPal官方提供的CreateOrder示例报文,postman地址<https://www.postman.com/paypal/paypal-public-api-workspace/example/19024122-a7885e7f-4c74-42c2-9dda-e5244bec3e79> |

  ### 2.1 提示词探寻

  使用MarsCode + DeepSeek V3，尝试提供合适的提示词及材料，让工具生成我们想要的代码。

  a. 第一次尝试：
  * 总结：代码生成2分钟 + 代码修复花费70分钟。对提示词的修改3次。
  * 详细调查记录见wiki:   [CreateOrder_实体商品_Try1.md](./CreateOrder_实体商品_Try1.md)

  b. 第二次尝试：
  * 增加了第一次尝试的3个提示词改动。
  * 总结：代码生成2分钟 + 代码修复花费25分钟。对提示词的修改1次。
  * 详细调查记录见wiki:   [CreateOrder_实体商品_Try2.md](./CreateOrder_实体商品_Try2.md)
  
  c. 第三次尝试：
  * 增加了第二次尝试的1个提示词改动。
  * 总结：代码生成2分钟 + 代码修复花费10分钟。
  * 详细调查记录见wiki:   [CreateOrder_实体商品_Try3.md](./CreateOrder_实体商品_Try3.md)

  d. 小结：
  * DeepSeek V3能够正确理解提示词，并生成符合要求的代码。
  * 需要人工干预调整的代码主要是对PayPal SDK中子类实例化的错误。

  ### 2.2 横向对比MarsCode中各模型
  
  | LLM name    | 编译错误数量 | 逻辑错误数量 | 错误修复所需时间 | 备注              |  
  | ----------- | ----------- | ----------- | --------------- | ----------------- | 
  | DeepSeek V3 | 31          | 0           | 10分钟          | 对SDK中实例的子类生成会错误 |
  | DeepSeek R1 | 31          | 0           | 10分钟          | 对SDK中实例的子类生成会错误 |