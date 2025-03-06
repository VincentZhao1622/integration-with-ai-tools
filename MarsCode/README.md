# MarsCode调查

## 1. MarsCode总览

* 调查时间 ： 2025年3月6日

 | Feature  | Comments |
 | -------- | -------- |
 | 费用     | 免费 |
 | 默认LLM  | DouBao/DeepSeek |
 | IDE支持  | Vscode/idea插件支持 |
 | 编程支持  | 对话      | 
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
  | 2    | OrdersCreateInput.java | PayPal javasdk中调研CreateOrder接口使用的数据模型 |
  | 3    | CreateOrderDetailed.json | PayPal官方提供的CreateOrder示例报文(postman地址https://www.postman.com/paypal/paypal-public-api-workspace/example/19024122-a7885e7f-4c74-42c2-9dda-e5244bec3e79)

  ### 2.1 MarsCode + DeepSeek
   * 使用MarsCode的chat功能，提供合适的提示词及材料，尝试让工具生成我们想要的代码
  1. 场景一：
  

  

