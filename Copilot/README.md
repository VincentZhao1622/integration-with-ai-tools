# Copilot调查
## 1. Copilot总览
* 调查时间 ： 2025年3月5日

 | Feature  | Comments |
 | -------- | -------- |
 | 费用     | 免费plan(30天试用)/Pro($10/月)及以上收费 |
 | 默认LLM  | GPT/Claude/Gemini |
 | IDE支持  | VSCODE插件支持最好，IDEA插件更新慢 |
 | 编程支持  | 自动补全/聊天 两种模式 | 
 | VPN?     | 需要     |
 | 中文文档  | 少       |  

## 2. 调研Use case 1, JAVA后端 + PayPal javasdk(v2)
 - IDE: IntelliJ IDEA 2024.3.4 (Community Edition)
 - 插件： IDEA github copilot - 1.5.37版本
 - JAVA版本： 21
 - 代码使用清单
  | No.  | Name     | Comments |
  | ---- | -------- | -------- |
  | 1    | OrderVO.java | 模拟商户网站原有数据模型 |
  | 2    | OrdersCreateInput.java | PayPal javasdk中调研CreateOrder接口使用的数据模型 |
  | 3    | CreateOrderDetailed.json | PayPal官方提供的CreateOrder示例报文(postman地址https://www.postman.com/paypal/paypal-public-api-workspace/example/19024122-a7885e7f-4c74-42c2-9dda-e5244bec3e79)

  ### 2.1 Copilot + GPT4o
   * 使用Copilot的chat功能，提供合适的提示词及材料，尝试让工具生成我们想要的代码
  1. Try1：
  ```
   提示词： Given request example "CreateOrderDetailed.json", generate the mapping logic from OrderVO.java to OrderCreateInput.java, note the nested columns may have different names.
  ```
  

