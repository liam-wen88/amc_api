# AMC 接口与数据表

Amazon Marketing Cloud（AMC）常用接口与数据表的中文整理，纯静态 HTML，可直接用 GitHub Pages 发布。

## 页面

只有一个页面 `index.html`，顶部 8 个页签：

| 页签 | 内容 |
|---|---|
| AMC实例管理接口 | AMC 实例管理接口（Instance management，10 个接口） |
| AMC模型schema | 总览（全部分析表、分组、SA / DSP 数据归属、官方链接）+ 每张分析表的字段、类型、聚合阈值 |
| AMC模型指标集schema | 3 个应用模型（广告重合度、转化路径、转化时间）的维度与指标：单位、定义、计算规则、过滤条件、数据源 |
| AMC模型接口 | AMC 报表接口（Workflow Management Service，17 个接口）：工作流、执行、定时任务、数据源 |
| AMC受众schema | 基础受众与受众表对照、全部 23 张官方 `_for_audiences` 受众表（含官方链接）及字段 |
| AMC受众转化事件映射 | 26 个转化事件 → 适用基础受众、广告类型、关联数据表、字段 |
| AMC受众条件项映射 | 79 个条件项 → 基础受众、转化事件、广告类型、关联数据表、字段 |
| AMC受众接口 | AMC 受众接口（Rule-based audiences，6 个接口） |

前四个页签（实例、模型）为一组颜色，后四个页签（受众）为另一组颜色。

## 发布到 GitHub Pages

1. 新建仓库，把本目录全部文件（含 `.nojekyll`）推到 `main` 分支根目录。
2. 仓库 **Settings → Pages**，Source 选 **Deploy from a branch**，分支选 `main`、目录选 `/ (root)`。
3. 几分钟后访问 `https://<用户名>.github.io/<仓库名>/`。

页面不依赖外部脚本或构建步骤，本地直接双击 `index.html` 也能打开。

## 数据来源与说明

- 字段、类型、约束：Amazon Ads 官方 OpenAPI 规范与开发者指南（Amazon Marketing Cloud · Data sources、Rule-based audiences、Instance management）。
- 中文说明为转述；标注「推断」「待确认」的内容不是官方原文。
- 非官方文档，内容以 Amazon 官方为准。
