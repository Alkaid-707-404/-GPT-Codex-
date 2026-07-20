# 路辰GPT/Codex桌宠
适用于GPT/Codex桌面版的二次元Q版桌宠包，角色是时空中的绘旅人的路辰。
桌宠本身不包含独立app，GPT/Codex负责读取 pet.json 和 spritesheet.webp，并根据应用状态播放对应动画，使用前请确认当前 Codex 版本已提供 **Pets** 功能

# 安装
将整个仓库文件夹复制到 %USERPROFILE%\.codex\pets\Alkaid
打开 Codex，依次进入 **Settings → Pets**
点击 **Refresh**，选择 **Alkaid**，再点击 **Wake Pet**

# 动作设置
当前版本是“思考动作锁定版”。为了让 Codex 执行任务时持续显示缓慢翻书的思考动作，默认待机、任务状态和鼠标方向响应均使用了同一套 thinking 动画

| 应用状态 | 帧数 | 当前动作 |
| --- | ---: | --- |
| `idle` | 6 | 坐着翻书思考，缓慢循环 |
| `running-right` | 8 | 向右拖动时的方向动作 |
| `running-left` | 8 | 向左拖动时的方向动作 |
| `waving` | 4 | 微笑挥手 |
| `jumping` | 5 | 已替换为缓慢挥手并微笑，避免悬停时反复上下蹲跳 |
| `failed` | 8 | 委屈、失败状态 |
| `waiting` | 6 | 翻书思考 |
| `running` | 6 | 翻书思考，翻页速度较慢 |
| `review` | 6 | 翻书思考 |
| `lookDirections` | 16 | 当前统一显示翻书思考姿势 |
由于 `idle` 和 16 个鼠标方向格也被锁定为 thinking，这一版在没有任务时也可能继续翻书。这是当前版本的预期效果

# 仓库内容
# 运行必需文件
| 文件 | 用途 |
| --- | --- |
| `pet.json` | 桌宠名称、版本、动画行列及帧数配置 |
| `spritesheet.webp` | Codex 实际读取的透明动画图集 |

# 发布与源文件
| 文件 | 用途 |
| --- | --- |
| `README.md` | 安装和动作说明 |
| `Alkaid_1.zip` | 可直接下载解压的桌宠包 |
| `spritesheet.png` | 无损 PNG 图集，便于检查、修改和重新导出 |
| `look-manifest.json` | 方向动作相关的图集记录 |

# 校验与处理记录

| 文件 | 用途 |
| --- | --- |
| `validation-force-thinking-all-task.json` | 当前版本的主要图集校验结果 |
| `validation-*.json` | 各次调整后的历史校验记录 |
| `despill-*.json` | 透明边缘及去色处理记录 |

# 历史备份

以下文件用于回退旧动作或旧画面，不参与 Codex 日常运行：
- `spritesheet-before-force-thinking-all-task.*`
- `spritesheet-before-task-thinking-lock.*`
- `spritesheet-before-slow-book.*`
- `spritesheet-before-hover-fix.*`
- `spritesheet-clean.*`
- `spritesheet-sharp*.*`

- ## 图集规格
- Pet ID：`alkaid`
- 显示名称：`Alkaid`
- 格式版本：`spriteVersionNumber: 2`
- 图集尺寸：`1536 × 2288`
- 单格尺寸：`192 × 208`
- 图集结构：`8 列 × 11 行

# 说明
这是非官方同人桌宠项目，仅供个人交流与学习使用。角色及原作相关权利归原权利方所有
