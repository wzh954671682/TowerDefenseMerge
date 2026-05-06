

***

# 通用休闲游戏美术 AI 批量生图 Prompt 规范文档

## 一、 全局视觉基调 (Global Art Direction)
*所有生图 Prompt 均需包含的基础前缀，用于统一核心的美术画风与质感。*

*   **核心美术风格:** `Casual mobile game style, stylized 2D, soft 3D rendering feel, cute chibi aesthetic, high quality, clean and vibrant.` (休闲手游风格，风格化2D，柔和的3D渲染感，Q版可爱美学，高质量，干净鲜艳)
*   **色彩倾向:** `Vibrant color palette, high saturation, clear color blocking, bright and cheerful.` (高饱和度鲜艳色彩，清晰的色块划分，明亮欢快)
*   **光影与材质:** `Soft global illumination, smooth gradient shading, rounded corners everywhere, glossy and gummy UI texture, no harsh shadows, soft ambient occlusion.` (全局柔和光照，平滑渐变阴影，全圆角设计，具有光泽的软糖UI质感，无生硬阴影，柔和的环境光遮蔽)
*   **通用负面词 (Negative Prompt):** `photorealistic, messy lines, sharp edges, dark and gritty, cyberpunk, realistic proportions, complex textures, grunge, noise.` (写实，杂乱线条，锐利边缘，暗黑写实，赛博朋克，写实比例，复杂纹理，脏污，噪点)

---

## 二、 局内实体视觉 (In-Game Entities)
*适用于生成游戏战斗或探索场景中的实际可交互模型与环境。*

*   **2.1 环境与地块:** `Top-down perspective game level, clean stylized 3D environment, dark muted background, soft global lighting, clean geometry, clear grid logic.` (纯正俯视角，色彩压暗的背景以突出核心实体)
*   **2.2 我方单位/友方角色:** `Chibi character design, big head, simplified body proportions, thick outline for visibility, standing pose, plain white background.` (Q版两头身比例，适当加粗轮廓以提升辨识度)
*   **2.3 敌对单位/怪物:** `Cute monster design, distinct silhouette, aggressive but cute expression, color-coded by elemental type.` (可爱的怪物设计，轮廓分明，色彩具有阵营或元素区分度)

---

## 三、 UI 与系统界面：基于功能定位的四大分支
*根据界面交互的实际目的进行排版与材质划分，确保视觉服务于功能。*

### 3.1 类型 A：局内高频交互 (战斗HUD、实时操作区)
*   **设计定位:** 极简、沉浸、低视觉阻挡，确保核心操作区清晰可见。
*   **Prompt 关键词:** `Minimalist combat HUD, transparent dark glass panel, bottom docked skill bar, rounded square slots, unobstructed center view, flat game UI.`

### 3.2 类型 B：局外资产与陈列 (背包、图鉴、角色列表)
*   **设计定位:** 突出实体资产，采用高对比度的整齐网格排版。
*   **Prompt 关键词:** `Inventory grid layout UI, dark purple solid background, well-organized repeating square slots, colorful thick borders indicating rarity, clear and structured mobile game UI.`

### 3.3 类型 C：常规系统与通用弹窗 (日常任务、设置、说明面板)
*   **设计定位:** 统一的圆角底板，清晰的列表层级与操作按钮。
*   **Prompt 关键词:** `Pop-up window UI, light purple/grey inner background, colorful ribbon header, flat vertical list layout, alternating row colors, pill-shaped action buttons in green and yellow, prominent red close button.`

### 3.4 类型 D：强反馈与高光展示 (抽卡、结算、稀有物品获取)
*   **设计定位:** 强视觉冲击，中心构图，伴随夸张的粒子光效与立体空间感。
*   **Prompt 关键词:** `Gacha screen UI, celebratory visual style, 3D circular display pedestal, glowing starburst background effects, dramatic rim lighting on central character, golden UI accents, modal dark overlay.`

---

## 四、 细小部件与图标 (Icons & Components)
*适用于生成各类零散的视觉组件。*

*   **4.1 物品/资源图标:** `Game item icon, rounded square shape, vibrant solid color background, flat stylized object inside with subtle glossy highlights, clean vector style.`
*   **4.2 通用交互按钮:** `Pill-shaped button UI, chunky and thick, glossy finish, soft drop shadow for depth, white bold text inside.`
*   **4.3 状态开关 (如设置选项):** `Toggle switch UI element, bright green for active state, grey for inactive, rounded pill shape, soft inner shadow.`

---

## 五、 AI 批量生图 Prompt 组合公式

在日常批量生图时，直接拼接以下公式模板，并替换中括号 `[ ]` 内的具体对象描述即可：

**1. 场景/地图公式：**
> `[全局视觉基调] + [2.1 环境与地块] + [具体地形描述，例如：A magical forest path with glowing mushrooms] + Isometric top-down view`

**2. 单位/角色公式：**
> `[全局视觉基调] + [2.2/2.3 单位特征] + [具体角色描述，例如：A cute warrior holding a wooden sword and wearing a red cape] + character design sheet, front view, white background`

**3. 常规弹窗 UI 公式：**
> `[全局视觉基调] + [3.3 常规系统弹窗] + [具体界面描述，例如：Daily login reward panel with progress bars and treasure chests] + flat front view layout, UI design`

**4. 高光展示 UI 公式：**
> `[全局视觉基调] + [3.4 高光展示] + [具体界面描述，例如：Victory settlement screen with a golden crown and ribbons] + dramatic UI design`

**5. 物品图标公式：**
> `[全局视觉基调] + [4.1 物品图标] + [具体物品描述，例如：A shiny blue sapphire gem] + game icon asset, simple plain background`