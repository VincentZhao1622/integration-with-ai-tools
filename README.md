# 使用AI编程工具对接PP API调查
## 1.背景概要

* 1. 目的
  - 使用外部AI工具来自动生成PP对接代码，以加速技术对接的过程。

* 2. 调查方向
  - 通过市场上的AI编程工具，结合PayPal为开发者提供的对接文档/工具/Sample代码等，能够使商户能够快速完成技术对接。
  - 目前调查市场上AI编程工具有如下几类。
  
  | Vendor Category | Tools           | Highlights                            |
  | --------------- | --------------- | ------------------------------------- |
  | Independent vendors | Github Copilot, Continue.dev, Cursor AI | 独立厂商，可接入大部分主流LLM |
  | Global 1st Party vendors | ChatGPT Coding assistant, Claude Code, Gemini Code Assistant | 一方厂商，对自己的LLM兼容好 |
  | China 1st Party vendors | DeepSeek coder, Trae ai(ByteDance), Baidu Comate | 国内一方厂商，提供中文论坛支持，方便国内技术人员使用 |

* 3. 调查方案
    - 目前设定3个use cases,
    1. Auto-generate CreateOrder API mappings,(自动生成CreateOrder API的代码转换逻辑)。
    2. Auto-complete coding with PayPal sample codes（基于PayPal的sample代码，自动补全代码）
    3. Auto-testing with PayPal sample requests （自动生成测试代码）
    
* 4. 开始调查
  * 4.1 首先进行第一个use case的调查。
    * 4.1.1 选择CreateOrder API的原因，
      - API是传输业务数据的主要API；
      - 其中的格式是相对固定，且包含了较多的业务校验；
      - <b>商户端需要较多时间对接该API。</b>
    * 4.1.2 前提准备
      - 用户对接PayPal一般都有自建网站，拥有自己的数据结构，包阔人的信息，商品信息，物流信息等。此处模拟用户网站预设置好这些信息。
      - API数据转换一般都在服务器端发生。测试使用java语言，原因一为我自己本身对该语言较熟悉，二在国内环境下java作为后端代码也较为普遍，具有相对普适性。
      - PayPal相关的数据均从PayPal官方developer Portal获取，无额外加工。
    
