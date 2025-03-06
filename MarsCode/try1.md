# 尝试一 Marscode + deepseek R1

## 步骤: 第一步,尝试生成代码

1.首先手动在聊天框引入workspace #workspace

2.提示词

基于示例报文"CreateOrderDetailed.json"，
实现从项目实例"OrderVO.java"到目标实例"OrderRequest.java"的字段映射.
代码封装成一个私有方法.

注意:
1. 目标实例中的必填字段需要有值.必填字段有以下字段:
purchaseUnits, amount, currencyCode, value, 
1. 生成代码时不要使用建造者模式
2. 尽可能多的将项目实例的字段映射到目标实例中
3. 映射过程尽可能使用目标实例的枚举值

## 结果
```
