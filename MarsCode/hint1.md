# 在已有的工程添加支付
 
## 需求
 
-   本项目工程是一个购物车的结算页面，需要在结算页面中添加 PayPal 支付
-   使用 PayPal 的 JS SDK 来渲染 PayPal 支付按钮
 
## 代码细节
 
-   在`src/compoenents/paymentMethod/`目录下添加`PayPal.tsx`文件
-   在`CartPage.tsx`的支付插槽(相关代码在第 94 到第 99 行)中使用`PayPal.tsx`文件的内容来渲染 PayPal 支付按钮, 不要改动其他部分的代码
    -   把
-   ```tsx
        <Button variant="contained" color="primary" fullWidth>
          立即支付（¥{total}）
        </Button>
    ```
    替换成
    ```tsx
    <PayPal />
    ```
-   要求使用 PayPal JavaScript SDK（5.0+）
-   动态加载 PayPal JS SDK, 其中`clientId`为`test`, 请不要使用第三方依赖来实现动态加载, 使用动态加载script标签的方式来完成
   
-   请把购物车中的商品信息在创建订单的时候传递给后端,requestBody 的属性请从`@/store/cartStore.ts`的`CartState`中获取
-   模块的引入路径请使用`@`
 
## 后端接口
 
后端调用参考如下:
 
```javascript
paypal
    .Buttons({
        createOrder: () => {
            /* 调用 localhost:5004/api/orders */
        },
        onApprove: () => {
            /* 调用 localhost:5004//api/orders/:orderId/capture 接口 */
        },
    })
    .render("#paypal-button-container");
```
 
请按照上述接口来实现 PayPal 支付