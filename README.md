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
    - Frontend:给定一前端js的单页cart代码，和一个对接手册里提供的sample代码。看工具能否通过某种方式自动生成对接完成代码。
      - 第一阶段，BCDC方案
      - 第二阶段，ACDC方案
      - 第三阶段，GP/AP方案
    - Backend: 给定pp developer生成的sample代码，以及字段的具体描述，看能否完成对接代码生成。
      - 第一阶段：java
      - 第二阶段：nodejs
      - 第三阶段：其他支持的语言
    - 目标API： 
      - 第一阶段，测试order API的capture
      - 第二阶段，测试完整one time pay相关API流程
      - 第三阶段，其他相关的API陆续接入
    - 前后端Object Scope定义：
      - 第一(mvp)阶段提供minimum可通过API验证的必要信息，验证是否能够完成代码生成；
      - 第二阶段提供更多的常用信息，如商品信息，shipping信息及其他信息，验证是否能够完成代码；
      - 第三阶段，真实案例中的case字段

* 4. 开始验证
    * 4.1 Github Copilot
