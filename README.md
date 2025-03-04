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
    - 
    
