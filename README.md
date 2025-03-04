# 使用AI编程工具对接PP API调查
## 1.背景概要

* 1. 目的
  - 使用外部AI工具来自动生成PP对接代码，以加速技术对接的过程。

* 2. 调查方向
  - 本质上AI编程工具的能力还是依赖于背后大模型的能力，故对工具的调查主要方向暂定为：
    1. 是否免费
    2. 与IDE的兼容性（公司电脑安装方便）
    3. 多语言支持（是否支持中文）
    4. 最后再对功能进行使用调查。
  
  | No. | Name           | Price                            | IDE Compatibility  | Support Chinese | Comment |
  | --- | -------------- | ---------------------------------| ---------------    | --------------- | ------- |
  | 1   | Github Copilot | 内置模型，有免费plan, pro($10/M)及商用版收费 | VScode plugin      |  N              | plugin 29.1M下载，评分3.5/5 |
  | 2   | Continue.dev   | 免费有次数限制，open source，额外需自行接入模型 | VScode, JetBrains plugin   |  N              | plugin 808K下载, 4.5/5
  | 3   | CursorAI       | 免费2周试用，之后$20/month        | 独立安装包，支持Mac/Win | 中文官网，论坛英文居多 | 评论区好评如潮
  | 4   | Amazon Q Developer | Free tier/pro($19/M)        | VScode, JetBrains plugins   |  N              |
  | 5   | Trae | 免费   | 独立安装包             |  中英文文档              |
  | 6   | ... | 

  调查顺序暂定 copilot - continue - trae - cursorAI - Amazon - ...

* 3. 调查方案
    - 目前设定3个use cases,
    1. Auto-generate CreateOrder API mappings,(自动生成CreateOrder API的代码转换逻辑)。
    2. Auto-complete coding with PayPal sample codes（基于PayPal的sample代码，自动补全代码）
    3. Auto-testing with PayPal sample requests （自动生成测试代码）
    
    
* 4. 开始调查
    * 4.1 首先进行第一个use case的调查。
    
