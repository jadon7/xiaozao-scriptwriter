# 🍳 xiaozao-scriptwriter

「大师的AI小灶」视频脚本写作 Skill —— 基于 33 期真实脚本提炼的风格指南、结构模板和范文库。

## 这是什么

一个 [OpenClaw](https://github.com/openclaw/openclaw) Agent Skill，让 AI 能够以「大师」的个人风格撰写视频脚本。

当你对 AI 说"帮我写个脚本"、"出个稿"、"用大师风格润色一下"时，这个 skill 会自动加载，指导 AI：

- 用大师的语气写作（口语化、自嘲、"巧了"、"说人话"）
- 按标准结构搭建脚本（钩子→教学→收尾）
- 自然植入广告（教程即广告）
- 完成后自动检查质量（是否有标志性句式、结构是否完整）

## 文件结构

```
xiaozao-scriptwriter/
├── SKILL.md                           # 核心指令：触发条件、写作流程、质量检查清单
├── references/
│   ├── style-guide.md                 # 语气基调、信息传递原则、节奏控制
│   ├── structure-templates.md         # 4 套结构模板（教程/评测/观点/广告）
│   ├── vocabulary.md                  # 标志性词汇、固定句式、造词比喻库
│   └── examples/                      # 范文（OCR 提取自真实脚本 PDF）
│       ├── A05-tutorial.txt           # 经典教程（非广告）
│       ├── A15-review.txt             # 深度评测（非广告）
│       ├── A38-ad.txt                 # 广告植入标杆
│       └── A50-opinion.txt            # 观点输出（非广告）
```

## 安装方式

### 方式一：直接 clone（推荐）

```bash
git clone https://github.com/jadon7/xiaozao-scriptwriter.git ~/.agents/skills/xiaozao-scriptwriter
```

重启 OpenClaw 后，skill 会自动出现在可用列表中。

### 方式二：安装 .skill 包

如果你拿到了 `xiaozao-scriptwriter.skill` 文件：

```bash
# 解压到 skills 目录
unzip xiaozao-scriptwriter.skill -d ~/.agents/skills/
```

### 方式三：手动放置

把整个 `xiaozao-scriptwriter/` 文件夹复制到以下任一位置：

- `~/.agents/skills/`（用户级）
- `<workspace>/.agents/skills/`（项目级）

## 使用方式

安装后无需额外配置。直接跟 AI 说：

- "帮我写一个关于 XX 的视频脚本"
- "这个选题出个脚本初稿"
- "用大师的风格润色一下这段文案"
- "帮我写个广告脚本，品牌是 XX，卖点是 YY"

AI 会自动加载 skill，按照大师的风格和结构完成脚本。

## 适用场景

| 场景 | 说明 |
|------|------|
| 新脚本撰写 | 从选题到完整脚本 |
| 脚本润色 | 把普通文案改成大师风格 |
| 广告脚本 | 自然植入品牌，保持教学价值 |
| 局部生成 | 只写开场钩子、只写收尾、只写广告过渡段 |

## 数据来源

基于「大师的AI小灶」A05-A76 共 33 期视频脚本 PDF，经 OCR 提取全文后进行系统性分析。覆盖教程、评测、观点、广告四种类型。

## License

仅供「大师的AI小灶」团队内部使用。
