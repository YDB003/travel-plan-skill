# OpenClaw / 通用 Agent 使用说明

本仓库是一个国内旅游攻略规划 Skill，原生面向 Codex。若当前 Agent 不支持 Codex Skill 自动触发，请手动读取 `SKILL.md` 并按其中流程执行。

## 入口文件

- 主流程：`SKILL.md`
- 数据源策略：`references/source_strategy.md`
- 输出模板：`references/output_templates.md`
- 可视化出图：`references/visual_output.md`

## 能力范围

只做中国国内旅行规划，包含港澳台，不处理出境游。

支持：

- 快速版攻略
- 深度版攻略
- 目的地推荐
- 小红书点位入口
- 酒店主来源推荐
- 城际交通对比
- 完整行程规划
- HTML / PNG / PDF 可视化攻略

## 执行原则

1. 不编造动态数据。
2. 酒店价格、余房、车票、机票、预约规则必须标注「已核验 / 搜索线索 / 需确认」。
3. 涉及平台数据时，先做一次平台登录预检，后续不要反复打断用户。
4. 点位发现、拍照机位、避雷反馈优先使用小红书搜索结果页。
5. 酒店推荐只输出一个主来源链接和推荐理由；用户要求比价时才查多平台。
6. 交通必须从价格、余票、门到门时间、风险角度做对比。
7. 可视化输出必须保留来源和风险提示。

## 小红书链接格式

默认使用：

```text
https://www.xiaohongshu.com/search_result_ai?keyword={URL编码后的关键词}&source=web_explore_feed
```

如果不可用，降级为：

```text
http://www.xiaohongshu.com/search_result/?keyword={URL编码后的关键词}
```

## 可视化输出

如果用户要求出图、网页、海报、PNG 或 PDF：

1. 先生成文字攻略。
2. 再生成本地 HTML。
3. 使用真实图、用户图或明确标注的 AI 氛围图。
4. 截图前检查桌面和手机宽度，避免文字溢出。
5. 返回 HTML 和截图路径。
