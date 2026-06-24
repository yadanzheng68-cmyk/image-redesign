# 架构图重绘原则 (Diagram Redesign Principles)

将阿里云架构图重绘为干净的 SVG 时，必须严格遵守以下原则：

## 1. 颜色只用模版色 (Template colors only)
- 主色：智能蓝 `#0A3CD9` + 白 `#FFFFFF`
- 辅助色：蓝灰、橙 `#FF6A00`、黑
- 渐变箭头、蓝色星标 ★ 高亮
- **不得**自行使用青色 (cyan) 或任何不在模版里的颜色。

## 2. 保留原图所有箭头 (Preserve all original arrows)
- 箭头方向、连接关系、双向/单向必须与原图完全一致，不增不减。

## 3. 其它固定要求
- 背景纯白 `#FFFFFF`。
- 中文标注全部翻译成英文。
- 输出格式：SVG（矢量）。
- 输出前用 cairosvg 渲染成 PNG 自行审查，不得出现乱码 (mojibake)。
- 与原图保持 ~99% 一致（箭头、文字位置、所有连接），只是更清晰且符合主题色。
- 品牌标识："ALIBABA CLOUD INTELLIGENCE"（INTELLIGENCE 蓝）+ "GROUP"（灰）。

## 4. 工作流程
- 开发分支：`claude/exciting-hamilton-05zh0n`
- commit 信息清晰，push 到 `yadanzheng68-cmyk/image-redesign`。
- 除非明确要求，**不要**创建 PR。
- 预览 PNG 已 gitignore (`*-preview.png`)，不要提交。
