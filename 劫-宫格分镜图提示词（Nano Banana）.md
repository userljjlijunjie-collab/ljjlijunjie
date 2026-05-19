# 《**劫》宫格分镜图提示词（Nano Banana）

> ★ 本文档产出的宫格分镜图将作为 Seedance 2.0 的 style_reference 上传
> ★ 每张宫格图对应一个 SEG（4-15秒），由 2-4 格关键帧组成
> ★ 宫格图 + 时间轴提示词 = 双重约束投喂 Seedance
> ★ 工具：Nano Banana（Flux / MidJourney）
> ★ 宫格排列：从左到右 = 时间顺序（格1→格2→格3→格4）
> ★ 景别切换原则：相邻格景别跨度≤2级（如全景→中景✓ 全景→特写✗）

---

## 宫格设计总原则

```
┌──────────────────────────────────────────────────────┐
│  宫格分镜图设计铁律                                    │
│                                                        │
│  ① 每格 = 该Clip内一个关键时间节点的静态画面           │
│  ② 格与格之间必须有视觉连贯性（同场景/同角色/同色调）  │
│  ③ 景别切换必须流畅：                                  │
│     全景 → 中全景 → 中景 → 中近景 → 近景 → 特写      │
│     相邻格最多跨2级，不可从全景直接跳特写              │
│  ④ 角色朝向在所有格中保持一致（不翻转）               │
│  ⑤ 光影/色调在所有格中保持统一基调                    │
│  ⑥ 宫格比例：9:16竖屏内2-4格垂直排列                 │
│     → 2格：上下各占50%                                │
│     → 3格：上中下各占33%                              │
│     → 4格：2×2宫格排列                                │
│  ⑦ 每格之间用1px细白线分隔                            │
└──────────────────────────────────────────────────────┘
```

---

## SEG-01 · 妖星坠落·山门震动（3s · 2格）

```
宫格结构：上下2格（9:16竖屏·上下各50%）
格1 = T+0s 天空裂缝+妖星坠出（大全景仰视）
格2 = T+2.5s 地面碎裂+妖气上涌（中景俯视地面）
景别切换：大全景仰视 → 中景俯视地面（视角反转·强调从天到地的冲击传递）
```

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━
【操作指引】
  垫图上传：@图片9 大禹门山门·夜景妖劫版
  垫图权重：0.30-0.40（场景氛围参考·不限制构图）
  工具模式：图生图 / Flux img2img / MJ --sref
  备注：本段无角色出现·仅需场景参考图
━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**Nano Banana 提示词：**

```
prompt:
Game CG quality Chinese fantasy 3D animation storyboard,
9:16 vertical aspect ratio, two-panel vertical storyboard layout
separated by thin 1px white line at center,
consistent dark indigo #2C3E50 night atmosphere across both panels,
cinematic lighting, highly detailed:

TOP PANEL (upper 50%):
extreme low angle looking up 75 degrees at night sky,
indigo dark sky #2C3E50 torn open with violent crimson crack
#C0392B glowing with molten edges extending diagonally,
a blazing meteor with orange-red #E67E22 fire trail falling
through the crack, ancient mountain gate temple silhouette
visible in mid-ground backlit by crimson light,
volumetric crimson light pressing down from fracture,
cloud sea churning in background,
composition: sky crack occupying upper 60%, temple silhouette 25%,
stone stair edge at very bottom 15%

BOTTOM PANEL (lower 50%):
medium shot looking down at ancient grey-white stone staircase,
radial cracks spreading outward from center impact point,
dark green miasma #27AE60 seeping upward from crack fissures,
stone debris floating upward 0.3m from seismic tremor,
same crimson light from above illuminating the cracked surface,
dragon-wave carved patterns on stair edges visible under red light,
composition: cracked stone surface with green miasma rising occupying
full frame of this panel

both panels share: dark indigo base tone, crimson crack light as
primary illumination, same moment of catastrophe from two angles,
professional animation storyboard reference sheet style,
clean sharp rendering, no text no labels

negative prompt:
cartoon, anime, bright daylight, cheerful, blurry, low quality,
text, labels, arrows, speech bubbles, sketch style, pencil drawing,
horizontal layout, single panel only
```

---

## SEG-02 · 剑仙拔剑出鞘（5s · 3格）

```
宫格结构：上中下3格（9:16竖屏·各占33%）
格1 = T+0s 剑仙侧身静立石阶·握剑未出（中全景）
格2 = T+2s 拔剑瞬间·蓝色剑气爆闪（中景·动作核心）
格3 = T+4s 飞剑阵列成形·风压扩散（中全景后拉）
景别切换：中全景 → 中景（放大动作）→ 中全景（后拉展示结果）
```

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━
【操作指引】
  垫图上传：@图片1 剑仙三视图正面 + @图片9 大禹门夜景
  垫图权重：0.40-0.50（角色需高度还原·权重偏高）
  工具模式：图生图 / Flux img2img / MJ --cref [剑仙图] --cw 80
  备注：三格中角色必须保持同一朝向同一服装
       如MJ支持多图参考则同时传入角色+场景
━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**Nano Banana 提示词：**

```
prompt:
Game CG quality Chinese fantasy 3D animation storyboard,
9:16 vertical aspect ratio, three-panel vertical storyboard layout
separated by thin 1px white lines dividing into equal thirds,
consistent night scene with crimson-cracked sky above and cracked
stone staircase below, cinematic lighting, highly detailed:

TOP PANEL (upper 33%):
medium-full shot, low angle 35 degrees looking up,
white-haired male sword immortal in silver-white robes with blue trim
standing in calm side stance on cracked ancient stone steps,
right hand gripping sword handle with blade pointing down emitting
faint blue glow #4A90D9, weight shifted forward ready posture,
calm half-closed eyes with slight frown, individual white hair strands
visible, fabric texture detailed, crimson sky crack light from above
creating rim light on silver robes, dark green miasma faintly rising
from ground cracks behind him,
left-right body position clearly defined for consistency

MIDDLE PANEL (middle 33%):
medium shot, same low angle, SAME CHARACTER same position same direction,
the exact moment of sword draw - blade halfway out of sheath,
bright blue energy burst #4A90D9 exploding outward 1.5m from blade,
ring-shaped blue energy wave expanding, silver-white robes swept
dramatically backward from energy release at maximum billow,
white hair blown back with blue luminescent染色,
facial expression shifting to eyes widening slightly with blue glow
in pupils, sword tassel at peak swing,
blue energy illuminating the scene replacing crimson as primary light

BOTTOM PANEL (lower 33%):
medium-full shot pulled back slightly wider than top panel,
same character now with sword drawn and held to the side,
30+ luminous blue flying swords materialized in fan array formation
behind his upper body area, each with individual blue energy trail,
circular wind pressure ripple expanding at feet on stone surface
pushing small debris outward, robes settling back down from billow,
hair beginning to fall back into place with residual blue glow,
expression: controlled confidence with blue-lit pupils,
blue sword array dominant in upper portion of this panel

all three panels share: same character facing same direction throughout,
same stone staircase location, same night atmosphere, progressive
action sequence from still→action→result, consistent silver-white
and blue #4A90D9 color palette with crimson #C0392B sky accent,
professional animation storyboard, clean sharp CG render

negative prompt:
different characters, direction change, mirroring, flip,
cartoon, anime, sketch, bright daylight, blurry, low quality,
text, labels, horizontal layout, single panel, inconsistent lighting
```

---

## SEG-03 · 相柳九首显现·妖潮涌出（5s · 3格）

```
宫格结构：上中下3格（9:16竖屏·各占33%）
格1 = T+0s 黑绿云层翻涌·第一颗蛇首探出（大全景仰拍）
格2 = T+3s 九首全部显现·九对猩红眼排列（大全景仰拍·更多蛇首）
格3 = T+4.5s 地面妖潮涌出（中景俯视地面裂缝）
景别切换：大全景仰拍 → 同角度（内容增加）→ 中景俯视（从天到地）
```

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━
【操作指引】
  垫图上传：@图片7 相柳·九首从云层压下 + @图片10 妖潮群体涌出
  垫图权重：0.35-0.45（BOSS形态需还原·但构图由提示词主导）
  工具模式：图生图 / Flux img2img / MJ --cref [相柳图] --cw 70
  备注：格1&格2用相柳参考图主导
       格3用妖潮参考图主导
       如工具不支持分格不同参考·则优先用相柳图（占2格）
━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**Nano Banana 提示词：**

```
prompt:
Game CG quality Chinese fantasy 3D animation storyboard,
9:16 vertical aspect ratio, three-panel vertical storyboard layout
separated by thin 1px white lines dividing into equal thirds,
consistent extremely dark oppressive atmosphere, minimal lighting
only from crimson eyes and toxic green glow, highly detailed:

TOP PANEL (upper 33%):
extreme low angle 80 degrees looking straight up at pitch-black sky,
churning black-green storm clouds filling the frame,
ONE massive serpent head emerging from cloud base,
head impossibly large (10x human scale implied),
one pair of crimson glowing eyes #C0392B opening like blood-red lanterns
piercing through darkness, dark green-black scales with wet toxic sheen,
toxic green miasma #27AE60 beginning to cascade downward from cloud base,
composition: 65% dark cloud mass, serpent head emerging from center-right

MIDDLE PANEL (middle 33%):
same extreme low angle same perspective,
NOW nine massive serpent heads ALL visible arranged in dome/canopy
formation filling the entire sky, nine pairs of crimson eyes #C0392B
all blazing simultaneously creating a pattern of red point-lights
in the darkness, dark green toxic miasma pouring down like waterfall
curtain from between the heads, each head with detailed dark scales
#27AE60 low-saturation wet gleam, fangs visible dripping toxic liquid,
overwhelming oppressive scale - the creature blocks ALL sky,
composition: nine heads filling 100% of this panel's frame

BOTTOM PANEL (lower 33%):
medium shot looking down at ground level,
ancient stone staircase surface with widening cracks,
dark shadowy creature mass surging UPWARD from the fissures,
semi-solid shadow forms with green-yellow glowing eyes densely packed,
hundreds of dark creatures climbing out like a flood/tide,
dark mist trailing each creature form,
faint blue glow (sword immortal's residual energy) visible at frame edge
for spatial continuity with previous SEG,
composition: ground cracks with creature mass filling 80% of panel

all three panels share: pitch-black #1A1A1A base tone with only
crimson #C0392B eye-glow and toxic green #27AE60 as light sources,
extreme darkness and oppression atmosphere, no sunlight no warmth,
professional animation storyboard, CG render quality

negative prompt:
bright colors, daylight, blue sky, friendly creatures, small scale,
cartoon, anime, sketch, text, labels, single head only in middle panel,
horizontal layout, warm tones
```

---

## SEG-04 · 朱雀觉醒（7s · 4格·2×2宫格）

```
宫格结构：2×2宫格排列（9:16竖屏·4格）
格1(左上) = T+0s 剑仙腰间玉佩发光（中近景·道具特写）
格2(右上) = T+2s 小朱雀跌撞飞出·初生形态（中景）
格3(左下) = T+4.5s 朱雀身体开始变身·羽毛变色（中景）
格4(右下) = T+6.5s 觉醒完成·火翼全展（中全景后拉）
景别切换：中近景特写 → 中景 → 中景 → 中全景（从近到远逐步展开）
```

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━
【操作指引】
  垫图上传：@图片1 剑仙正面（格1用）
           + @图片5 小朱雀·初生灵雀形态（格2-3用）
           + @图片6 小朱雀·觉醒火翼形态（格4用）
  垫图权重：0.35-0.45
  工具模式：
    方案A（推荐）：分两次生成后拼接
      第一次：上传剑仙+初生朱雀图·生成格1+格2
      第二次：上传初生朱雀+觉醒朱雀图·生成格3+格4
      最后用拼图工具合成2×2宫格
    方案B：一次生成整张
      同时上传3张参考图·MJ --cref [初生朱雀] --cw 60
      （优先保证朱雀形态连贯·剑仙仅出现在格1边缘）
  备注：本段核心是朱雀变身过程·格2-4的朱雀形态渐变是重点
       格1剑仙只需腰部局部·不需要全身高精度还原
━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**Nano Banana 提示词：**

```
prompt:
Game CG quality Chinese fantasy 3D animation storyboard,
9:16 vertical aspect ratio, four-panel 2x2 grid storyboard layout
separated by thin 1px white lines (2 columns x 2 rows),
reading order: top-left → top-right → bottom-left → bottom-right,
consistent dark night mountain staircase setting with progressive
warm-color transformation across panels, highly detailed:

TOP-LEFT PANEL:
medium close-up shot of male sword immortal's waist area,
jade pendant at waist belt blazing with golden-orange fire #E67E22,
cracks of golden light forming on jade surface erupting outward,
surrounding silver-white robe fabric illuminated by warm gold light,
hand reaching toward the glowing pendant,
dark night background with faint green miasma atmosphere,
composition: jade pendant as focal point center-frame glowing intensely

TOP-RIGHT PANEL:
medium shot, a small baby phoenix bird (30cm size) tumbling out
of golden light particles in mid-air, tiny wings flapping unsteadily,
soft dawn-orange downy feathers with subtle glow,
large round amber eyes wide with panic and surprise,
behind it: dark creature shapes approaching from background,
the small bird looking back over its shoulder at approaching threat,
cute but nervous expression, feathers slightly puffed,
composition: small phoenix center-frame surrounded by dark atmosphere

BOTTOM-LEFT PANEL:
medium shot, same small phoenix but body TREMBLING and GLOWING,
feathers visibly transitioning from soft orange to blazing golden fire,
body beginning to expand in size, energy cracks forming on surface,
golden-orange #E67E22 light intensifying dramatically,
surrounding air distorting from heat emanation,
expression shifting from panic to fierce determination,
composition: transforming phoenix center-frame with expanding glow

BOTTOM-RIGHT PANEL:
medium-full shot pulled back to show full wingspan,
transformation COMPLETE: juvenile divine phoenix with enormous
golden fire wings spread wide (2m span), filling upper portion,
wings: solid golden feathers at base transitioning to pure flame
energy at tips, blazing gold-white coloring,
eyes burning pure amber-gold, ember particles ascending like fountain,
ground beneath scorched in circular pattern,
entire panel dominated by warm golden-white light,
composition: awakened phoenix center with wings spread to panel edges

all four panels share: same dark night mountain staircase setting,
progressive color temperature shift from cold-dark (panel 1) to
blazing warm-gold (panel 4), same left-right spatial orientation,
transformation sequence reading naturally across panels,
professional CG storyboard quality

negative prompt:
inconsistent character between panels, adult phoenix in early panels,
cartoon, anime, sketch, text, daylight, cool blue throughout,
single panel, horizontal layout, blurry
```

---

## SEG-05 · 灵狐撑伞落地·桃花法阵（7s · 3格）

```
宫格结构：上中下3格（9:16竖屏·各占33%）
格1 = T+0s 桃花瓣逆风飘入+灵狐从上方下降（大全景）
格2 = T+3s 灵狐着地·伞尖触地·法阵开始扩散（中景）
格3 = T+6s 法阵完全展开·妖物被冻结（中全景展示控场效果）
景别切换：大全景 → 中景（聚焦着地动作）→ 中全景（展示法阵全貌）
```

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━
【操作指引】
  垫图上传：@图片3 灵狐三视图正面 + @图片9 大禹门夜景
  垫图权重：0.40-0.50（角色需高度还原·权重偏高）
  工具模式：图生图 / Flux img2img / MJ --cref [灵狐图] --cw 80
  备注：三格中灵狐必须保持同一服装/狐耳/发型/朝向
       法阵为粉色#F8B4C8·如生成结果法阵颜色偏差
       可在提示词中加强 "pink #F8B4C8 magic circle" 权重
       格3需要同时出现灵狐+冻结妖物·构图较复杂
       如生成效果不佳可把格3单独生成后拼接
━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**Nano Banana 提示词：**

```
prompt:
Game CG quality Chinese fantasy 3D animation storyboard,
9:16 vertical aspect ratio, three-panel vertical storyboard layout
separated by thin 1px white lines dividing into equal thirds,
consistent night battle scene on ancient stone staircase,
pink cherry blossom and warm gold (from phoenix) as accent lights
against dark base, highly detailed:

TOP PANEL (upper 33%):
wide full shot of entire stone staircase battlefield at night,
cherry blossom petals #F8B4C8 blowing into frame from the right
against logical wind direction (supernatural),
a beautiful fox-eared female character descending gracefully from
upper-right area holding an ornate parasol with one hand,
parasol spinning slowly with petals drifting from its edges,
flowing pink and white robes with cherry blossom embroidery visible,
fox ears pointed upward, long black hair trailing in descent,
below her: dark creatures on the stairs with golden phoenix fire
visible in background providing warm back-light,
composition: character descending through upper-right quadrant,
petals filling the air, battlefield below

MIDDLE PANEL (middle 33%):
medium shot, fox-eared female character landing with elegant single-foot
touchdown on stone step surface, parasol tip making contact with ground,
at the exact contact point: pink circular magic formation #F8B4C8
beginning to expand outward, intricate cherry-blossom rune patterns
glowing within the circle, just reaching 2m radius in this frame,
character's face clearly visible: confident tilted head with knowing
half-smile, fox ears alert, outfit details and embroidery sharp,
composition: character center-frame at moment of landing, nascent
magic circle expanding beneath

BOTTOM PANEL (lower 33%):
medium-full shot pulled back to show the full 5m radius magic circle,
pink circular formation fully expanded with rotating rune patterns,
cherry blossom petals spiraling upward from circle edges in vortex,
dark creatures within the circle boundary FROZEN mid-motion,
visible pink binding energy threads around their frozen limbs,
fox character standing at circle center with translucent fox tail
shadow manifested behind her glowing purple-pink,
parasol resting on shoulder casually,
composition: full magic circle visible on ground with frozen creatures,
character at center commanding the field

all three panels share: same night staircase location, same character
facing same direction, progressive action (descend→land→control),
pink #F8B4C8 as primary accent color with dark #2C3E50 base,
consistent character design across all panels (outfit/hair/ears),
professional CG storyboard quality

negative prompt:
inconsistent character design, direction flip, no magic circle,
cartoon, anime, sketch, text, daylight, male character,
single panel, horizontal, blurry, low quality
```

---

## 使用说明

```
【宫格分镜图使用流程】
═══════════════════════════════════════════════════════

1. 用 Nano Banana 生成每个 SEG 的宫格分镜图

2. 检查生成结果：
   □ 角色朝向是否所有格一致？
   □ 光影色调是否所有格统一？
   □ 景别切换是否流畅（无跳跃）？
   □ 格与格之间叙事是否连贯？

3. 投喂 Seedance 时的上传方式：
   → style_reference 上传该SEG的宫格分镜图
   → 提示词输入框粘贴对应的时间轴连贯描述
   → Seedance 同时参考"长什么样"+"怎么动"

4. 如果某格生成不满意：
   → 单独重新生成该格
   → 或调整该格提示词后重跑整张宫格

═══════════════════════════════════════════════════════
```

---

## 后续 SEG 待补

| SEG | 宫格数 | 状态 |
|---|---|---|
| SEG-01 | 2格 | ✅ 已写 |
| SEG-02 | 3格 | ✅ 已写 |
| SEG-03 | 3格 | ✅ 已写 |
| SEG-04 | 4格(2×2) | ✅ 已写 |
| SEG-05 | 3格 | ✅ 已写 |
| SEG-06 | 4格(2×2) | 待补 |
| SEG-07 | 3格 | 待补 |
| SEG-08 | 3格 | 待补 |
| SEG-09 | 2格 | 待补 |

---

*先跑 SEG-01 到 SEG-05 看效果，确认格式满意后我补齐 SEG-06-09*
