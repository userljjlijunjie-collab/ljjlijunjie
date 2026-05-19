# 《**劫》宫格分镜图提示词（Nano Banana）

> ★ 本文档产出的宫格分镜图将作为 Seedance 2.0 的 style_reference 上传
> ★ 每张宫格图对应一个 SEG（4-15秒），由 2-4 格关键帧组成
> ★ 宫格图 + 时间轴提示词 = 双重约束投喂 Seedance
> ★ 工具：Nano Banana（Flux / MidJourney）
> ★ 景别切换原则：相邻格景别跨度≤2级（如全景→中景✓ 全景→特写✗）

---

## 参考图完整索引

```
@图片1 = 剑仙三视图正面
@图片2 = 剑仙三视图侧面
@图片3 = 剑仙·万剑归宗法（技能释放态）
@图片4 = 灵狐三视图正面
@图片5 = 灵狐三视图侧面
@图片6 = 灵狐·岚花飞琼（技能释放态·法阵展开）
@图片7 = 小朱雀·初生灵雀形态
@图片8 = 小朱雀·觉醒火翼形态
@图片9 = 相柳·九首从云层压下
@图片10 = 相柳·主首特写
@图片11 = 大禹门山门·夜景妖劫版
@图片12 = 妖潮·群体涌出全景
```

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
│  ⑥ 宫格比例：9:16竖屏内垂直排列                      │
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
景别切换：大全景仰视 → 中景俯视（从天到地）
```

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━
【操作指引】
  垫图上传：@图片11 大禹门山门·夜景妖劫版
  垫图权重：0.30-0.40（场景氛围参考·不限制构图）
  工具模式：图生图 / Flux img2img / MJ --sref
  备注：本段无角色出现·仅需场景参考图
━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**Nano Banana 提示词：**

```
prompt:
Game CG quality Chinese fantasy 3D animation storyboard,
9:16 vertical aspect ratio, two-panel vertical layout separated
by thin 1px white line at center, consistent dark indigo #2C3E50
night atmosphere across both panels, cinematic lighting, highly
detailed:

TOP PANEL (upper 50%):
extreme low angle looking up 75 degrees at night sky, indigo dark
sky #2C3E50 torn open with violent crimson crack #C0392B glowing
with molten edges extending diagonally, a blazing meteor with
orange-red #E67E22 fire trail falling through the crack, ancient
mountain gate temple silhouette visible in mid-ground backlit by
crimson light, volumetric crimson light pressing down from fracture,
cloud sea churning in background, composition: sky crack occupying
upper 60%, temple silhouette 25%, stone stair edge at bottom 15%

BOTTOM PANEL (lower 50%):
medium shot looking down at ancient grey-white stone staircase,
radial cracks spreading outward from center impact point, dark green
miasma #27AE60 seeping upward from crack fissures, stone debris
floating upward 0.3m from seismic tremor, same crimson light from
above illuminating the cracked surface, dragon-wave carved patterns
on stair edges visible under red light

both panels share: dark indigo base tone, crimson crack light as
primary illumination, professional CG storyboard, no text no labels

negative prompt:
cartoon, anime, bright daylight, blurry, low quality, text, labels,
sketch style, horizontal layout, single panel only
```

---


## SEG-02 · 剑仙拔剑出鞘（5s · 3格）

```
宫格结构：上中下3格（9:16竖屏·各占33%）
格1 = T+0s 剑仙侧身静立（中全景）
格2 = T+2s 拔剑蓝色剑气爆闪（中景）
格3 = T+4s 飞剑阵列成形（中全景后拉）
景别切换：中全景 → 中景 → 中全景
```

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━
【操作指引】
  垫图上传：@图片1 剑仙正面 + @图片3 万剑归宗技能态 + @图片11 山门夜景
  垫图权重：0.40-0.50（角色+技能特效需高度还原）
  工具模式：MJ --cref [@图片1] --cw 80 --sref [@图片11]
           或 Flux img2img 上传@图片1为主图·@图片3为辅助参考
  备注：三格角色同一朝向同一服装
       格2-3的蓝色剑气参考@图片3万剑归宗技能态的特效形态
━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**Nano Banana 提示词：**

```
prompt:
Game CG quality Chinese fantasy 3D animation storyboard,
9:16 vertical, three-panel vertical layout separated by 1px white
lines into equal thirds, consistent night scene crimson-cracked sky
and cracked stone staircase, cinematic lighting, highly detailed:

TOP PANEL (upper 33%):
medium-full shot low angle 35 degrees, white-haired male sword
immortal silver-white robes blue trim standing calm side stance on
cracked stone steps, right hand gripping sword handle blade pointing
down faint blue glow #4A90D9, weight forward ready posture, calm
half-closed eyes slight frown, individual white hair strands visible,
fabric texture detailed, crimson sky crack rim light on robes

MIDDLE PANEL (middle 33%):
medium shot same angle SAME CHARACTER same direction, exact moment
of sword draw blade halfway out, bright blue energy burst #4A90D9
exploding outward 1.5m from blade, ring-shaped blue energy wave,
robes swept dramatically backward maximum billow, white hair blown
back blue luminescence, eyes widening blue glow in pupils, sword
tassel peak swing

BOTTOM PANEL (lower 33%):
medium-full shot pulled back wider, same character sword drawn held
to side, 30+ luminous blue flying swords fan array formation behind
upper body each with blue energy trail, circular wind pressure ripple
at feet expanding 1.5m pushing debris, robes settling, hair falling
back with residual blue glow, controlled confidence expression

all panels: same character same direction throughout, same location,
progressive still→action→result, blue #4A90D9 + silver-white +
crimson #C0392B accent, professional CG storyboard

negative prompt:
direction change, mirroring, different characters, cartoon, anime,
sketch, daylight, blurry, text, horizontal, single panel
```

---

## SEG-03 · 相柳九首显现·妖潮涌出（5s · 3格）

```
宫格结构：上中下3格（9:16竖屏·各占33%）
格1 = T+0s 第一颗蛇首探出（大全景仰拍）
格2 = T+3s 九首全部显现（大全景仰拍）
格3 = T+4.5s 地面妖潮涌出（中景俯视）
景别切换：大全景仰拍 → 同角度内容增加 → 中景俯视
```

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━
【操作指引】
  垫图上传：@图片9 相柳九首压下 + @图片10 相柳主首特写 + @图片12 妖潮
  垫图权重：0.35-0.45（BOSS形态还原·构图由提示词主导）
  工具模式：MJ --cref [@图片9] --cw 70
           或 Flux img2img 上传@图片9为主图
  备注：格1-2用相柳参考图·格3用妖潮参考图
       优先保证相柳九首的猩红眼+深绿鳞形态还原
━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**Nano Banana 提示词：**

```
prompt:
Game CG quality Chinese fantasy 3D animation storyboard,
9:16 vertical, three-panel vertical layout 1px white line separators,
extremely dark oppressive atmosphere only crimson eyes and toxic green
glow as light, highly detailed:

TOP PANEL (upper 33%):
extreme low angle 80 degrees straight up at pitch-black sky, churning
black-green storm clouds, ONE massive serpent head emerging from cloud
base 10x human scale, one pair crimson glowing eyes #C0392B opening
like blood lanterns, dark green-black scales wet toxic sheen, toxic
green miasma #27AE60 cascading downward from cloud base

MIDDLE PANEL (middle 33%):
same extreme low angle, NOW nine massive serpent heads ALL visible
dome/canopy formation filling entire sky, nine pairs crimson eyes
#C0392B blazing simultaneously pattern of red point-lights in darkness,
dark green toxic miasma waterfall between heads, each head detailed
dark scales #27AE60 wet gleam fangs dripping toxic liquid, overwhelming
oppressive scale blocking ALL sky

BOTTOM PANEL (lower 33%):
medium shot looking down ground level, stone staircase widening cracks,
dark shadowy creature mass surging UPWARD from fissures, semi-solid
shadow forms green-yellow glowing eyes densely packed, hundreds
climbing out like flood, dark mist trailing each form, faint blue
glow at frame edge for spatial continuity

all panels: pitch-black #1A1A1A base, only crimson #C0392B and toxic
green #27AE60 as light, extreme darkness, CG storyboard quality

negative prompt:
bright colors, daylight, blue sky, friendly, small scale, cartoon,
anime, sketch, text, single head in middle panel, horizontal
```

---


## SEG-04 · 朱雀觉醒（7s · 4格·2×2）

```
宫格结构：2×2宫格排列（9:16竖屏）
格1(左上) = T+0s 玉佩发光（中近景）
格2(右上) = T+2s 小朱雀跌出（中景）
格3(左下) = T+4.5s 变身中·羽毛变色（中景）
格4(右下) = T+6.5s 火翼全展（中全景）
景别切换：中近景 → 中景 → 中景 → 中全景
```

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━
【操作指引】
  垫图上传：@图片1 剑仙正面（格1用）
           + @图片7 小朱雀初生形态（格2-3用）
           + @图片8 小朱雀觉醒火翼形态（格4用）
  垫图权重：0.35-0.45
  工具模式：
    推荐分两次生成后拼接：
      第一次：上传@图片1+@图片7·生成格1+格2
      第二次：上传@图片7+@图片8·生成格3+格4
      拼图合成2×2
    或一次生成：MJ --cref [@图片7] --cw 60（优先朱雀连贯）
  备注：核心是朱雀变身渐变过程·色温从冷暗逐格变暖金
━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**Nano Banana 提示词：**

```
prompt:
Game CG quality Chinese fantasy 3D animation storyboard,
9:16 vertical, four-panel 2x2 grid layout 1px white lines,
reading order top-left→top-right→bottom-left→bottom-right,
dark night staircase setting progressive warm-color transformation,
highly detailed:

TOP-LEFT: medium close-up male sword immortal waist area, jade
pendant blazing golden-orange fire #E67E22 cracking from within,
golden light erupting through surface fractures, silver-white robe
illuminated warm gold, dark night background green miasma atmosphere

TOP-RIGHT: medium shot small baby phoenix 30cm tumbling out of golden
light particles mid-air, tiny wings flapping unsteadily, soft dawn-
orange downy feathers subtle glow, large round amber eyes panic,
dark creature shapes approaching background, cute nervous feathers
puffed

BOTTOM-LEFT: medium shot same small phoenix body TREMBLING GLOWING,
feathers transitioning soft orange to blazing golden fire, body
expanding, energy cracks on surface, golden-orange #E67E22 intensifying,
air distorting from heat, expression shifting panic to determination

BOTTOM-RIGHT: medium-full shot pulled back full wingspan, transformation
COMPLETE juvenile divine phoenix enormous golden fire wings 2m spread,
solid feathers base transitioning pure flame energy at tips gold-white,
eyes burning pure amber-gold, ember particles ascending fountain,
ground scorched circular pattern, dominated warm golden-white light

all panels: same staircase setting, progressive cold-dark to warm-gold,
same spatial orientation, smooth transformation sequence, CG quality

negative prompt:
adult phoenix early panels, inconsistent, cartoon, anime, sketch,
text, daylight, cool throughout, single panel, horizontal
```

---

## SEG-05 · 灵狐撑伞落地·桃花法阵（7s · 3格）

```
宫格结构：上中下3格（9:16竖屏·各占33%）
格1 = T+0s 桃花飘入+灵狐下降（大全景）
格2 = T+3s 着地·伞触地·法阵扩散（中景）
格3 = T+6s 法阵全开·妖物冻结（中全景）
景别切换：大全景 → 中景 → 中全景
```

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━
【操作指引】
  垫图上传：@图片4 灵狐正面 + @图片6 岚花飞琼技能态 + @图片11 山门夜景
  垫图权重：0.40-0.50（角色+法阵特效需高度还原）
  工具模式：MJ --cref [@图片4] --cw 80 --sref [@图片11]
           或 Flux img2img 上传@图片4主图·@图片6辅助
  备注：三格灵狐同一朝向/服装/狐耳
       法阵粉色#F8B4C8参考@图片6技能态的圆形法阵形态
       格3需同时出现灵狐+冻结妖物·构图复杂可单独生成拼接
━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**Nano Banana 提示词：**

```
prompt:
Game CG quality Chinese fantasy 3D animation storyboard,
9:16 vertical, three-panel vertical layout 1px white lines equal
thirds, night battle scene stone staircase, pink cherry blossom and
warm gold accent against dark base, highly detailed:

TOP PANEL (upper 33%):
wide full shot entire staircase battlefield night, cherry blossom
petals #F8B4C8 blowing in from right supernatural wind, fox-eared
female character descending gracefully from upper-right holding ornate
parasol one hand, parasol spinning petals drifting from edges, flowing
pink white robes cherry blossom embroidery, fox ears pointed black hair
trailing, dark creatures on stairs golden phoenix fire background,
composition: character descending upper-right, petals filling air

MIDDLE PANEL (middle 33%):
medium shot fox-eared female landing elegant single-foot touchdown,
parasol tip contacting ground, at contact point pink circular magic
formation #F8B4C8 expanding outward reaching 2m radius, cherry-blossom
rune patterns rotating glowing within circle, face clearly visible
confident tilted head knowing half-smile, fox ears alert outfit sharp,
composition: character center-frame moment of landing magic circle beneath

BOTTOM PANEL (lower 33%):
medium-full shot pulled back full 5m radius magic circle visible, pink
formation fully expanded rotating rune patterns, petals spiraling
upward from edges vortex, dark creatures FROZEN mid-motion pink binding
threads around limbs, fox character center translucent fox tail shadow
purple-pink glow, parasol on shoulder casually, composition: full
circle frozen creatures character commanding center

all panels: same character same direction throughout, progressive
descend→land→control, pink #F8B4C8 primary accent dark #2C3E50 base,
consistent design across panels, CG storyboard

negative prompt:
direction flip, inconsistent design, no magic circle, cartoon, anime,
sketch, text, daylight, male character, horizontal, blurry
```

---


## SEG-06 · 三方合击（8s · 4格·2×2）

```
宫格结构：2×2宫格排列（9:16竖屏）
格1(左上) = T+0s 三人站位蓄力（中全景）
格2(右上) = T+3s 三方能量同时射出（中景）
格3(左下) = T+5s 三色命中爆裂（中景特效核心）
格4(右下) = T+7s 冲击波清场·妖物消散（中全景）
景别切换：中全景 → 中景 → 中景 → 中全景
```

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━
【操作指引】
  垫图上传：@图片1 剑仙正面 + @图片3 万剑归宗技能态
           + @图片4 灵狐正面 + @图片6 岚花飞琼技能态
           + @图片8 朱雀觉醒火翼
  垫图权重：0.35-0.40（多角色场景·权重适中避免某角色主导）
  工具模式：
    推荐：分两次生成
      第一次：@图片1+@图片4+@图片8 → 生成格1（三人站位）
      第二次：@图片3+@图片6+@图片8 → 生成格2-4（技能释放）
      拼图合成
    或一次：MJ --cref [@图片3] --sref [@图片6] --cw 50
  备注：本段是全片视觉高点·三色并存
       蓝#4A90D9+金#E67E22+粉#F8B4C8三色各占相近比例
       命中点白芯为最亮点
━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**Nano Banana 提示词：**

```
prompt:
Game CG quality Chinese fantasy 3D animation storyboard,
9:16 vertical, four-panel 2x2 grid 1px white lines, reading order
top-left→top-right→bottom-left→bottom-right, night staircase
battle scene three-color attack sequence, highly detailed:

TOP-LEFT: medium-full shot three heroes formation on stone stairs
night, white-haired sword immortal center silver-white robes right
hand pointing forward blue swords behind, fox-eared female left pink
parasol forward pink energy, golden phoenix above wings spread fire
building in chest, dark creatures frozen ahead, three different energy
colors beginning to surge forward simultaneously

TOP-RIGHT: medium shot three attacks launching simultaneously, blue
sword cone #4A90D9 50+ swords tight cone pattern individual trails,
golden fire stream #E67E22 pouring from above wide beam, pink petal
tidal surge #F8B4C8 rushing forward ground level flower tsunami, all
three converging on same target area

BOTTOM-LEFT: medium shot impact point, triple-color prismatic explosion
blue+gold+pink collision brilliant white-core burst expanding 3m, dark
creatures disintegrating on contact dissolving dark particles, maximum
brightness at convergence center overexposed bloom, sharp explosion edges

BOTTOM-RIGHT: medium-full shot pulled back wider aftermath, shockwave
expanding outward clearing all creatures, three heroes hair/robes/wings
blown backward from energy output, scorched ground between heroes and
impact, ground cleared of all dark creatures, residual three-color
energy particles dissipating

all panels: same staircase location same night, progressive
charge→launch→impact→aftermath, three colors balanced
blue+gold+pink, professional CG storyboard

negative prompt:
single color only, calm scene, cartoon, anime, sketch, text,
daylight, horizontal, inconsistent characters
```

---

## SEG-07 · 相柳真身压下·毒雨倾泻（8s · 3格）

```
宫格结构：上中下3格（9:16竖屏·各占33%）
格1 = T+0.5s 九首真身突然压出（大全景仰拍）
格2 = T+4s 毒雨从九口倾泻（中全景·毒雨覆盖）
格3 = T+7s 三人防御崩坏艰难抵抗（中景）
景别切换：大全景仰拍 → 中全景 → 中景
```

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━
【操作指引】
  垫图上传：@图片9 相柳九首压下 + @图片10 相柳主首特写
  垫图权重：0.40-0.50（BOSS真身形态高度还原·这是标志镜头）
  工具模式：MJ --cref [@图片9] --cw 80
           或 Flux img2img @图片9为主图
  备注：标志镜头#4·相柳形态还原度最重要
       格1-2优先保证九首+猩红眼+湿润深绿鳞的细节
       格3需要三人渺小身影作为体量对比参考
       三人在格3仅占画面下15%·不需要高精度面部
━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**Nano Banana 提示词：**

```
prompt:
Game CG quality Chinese fantasy 3D animation storyboard,
9:16 vertical, three-panel vertical layout 1px white lines equal
thirds, pitch-black oppressive atmosphere BOSS pressure scene,
highly detailed:

TOP PANEL (upper 33%):
extreme low angle 85 degrees almost ground level looking straight up,
nine REAL colossal serpent heads NOT shadows solid massive bodies
simultaneously thrusting down from pitch-black clouds, each head 10x
human scale, dark green-black scales #27AE60 low-saturation wet sheen
each scale visible, crimson glowing eyes #C0392B all nine pairs blazing,
main head lowest center others arranged dome canopy formation blocking
entire sky, fangs elongated toxic liquid dripping, extreme oppressive
vertical composition maximum size dominance

MIDDLE PANEL (middle 33%):
medium-full shot all nine mouths OPEN simultaneously releasing
torrential dark green toxic rain #27AE60 pouring downward like nine
poisonous waterfalls covering entire scene, toxic liquid cascading
with acidic corrosion visual on everything below, the rain forms a
dense curtain between upper serpent heads and lower ground, darkest
green-black atmosphere

BOTTOM PANEL (lower 33%):
medium shot three tiny heroes at bottom struggling against toxic
downpour, pink magic circle on ground cracking turning black under
acid, golden phoenix flames flickering suppressed smaller, blue sword
shield edges dissolving eaten away, three figures only 15% of frame
impossibly small against the overwhelming force above, all three
defense systems visibly failing simultaneously, extreme desperation

all panels: pitch-black #1A1A1A dominant, toxic green #27AE60 +
crimson #C0392B only lights, maximum oppressive scale difference,
BOSS overwhelms everything, professional CG storyboard

negative prompt:
bright colors, small creature, friendly, daylight, cartoon, anime,
balanced power, heroes winning, text, horizontal, sketch
```

---

## SEG-08 · 三人并肩·决意爆发（6s · 3格）

```
宫格结构：上中下3格（9:16竖屏·各占33%）
格1 = T+0s 毒雨中三人不倒·能量开始重燃（中景）
格2 = T+3s 三方能量增强·虚影显现（中景）
格3 = T+5s 保护罩成形·推退毒雨（中全景）
景别切换：中景 → 中景（内容变化）→ 中全景（后拉展示气场）
```

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━
【操作指引】
  垫图上传：@图片1 剑仙正面 + @图片3 万剑归宗技能态
           + @图片4 灵狐正面 + @图片8 朱雀觉醒火翼
  垫图权重：0.35-0.45（多角色情绪场景·面部需清晰）
  工具模式：MJ --cref [@图片1] --cw 60（剑仙居中主导）
           辅助 --sref [@图片3]（剑气参考）
  备注：本段是情绪转折点·表情是重点
       剑仙面部牙关紧咬+双目直视需清晰
       三色能量从微弱→重燃→形成保护罩的渐变过程
       格3朱雀身后巨大凤凰虚影参考@图片8形态放大
━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**Nano Banana 提示词：**

```
prompt:
Game CG quality Chinese fantasy 3D animation storyboard,
9:16 vertical, three-panel vertical layout 1px white lines equal
thirds, toxic rain atmosphere three heroes refusing to fall energy
rebuilding, highly detailed:

TOP PANEL (upper 33%):
medium shot three heroes standing firm in toxic green rain, sword
immortal center gripping sword both hands blade blue glow #4A90D9
beginning to intensify from dim, jaw clenched eyes staring upward
defiant, fox character left side reforming stance fox tail growing,
phoenix above wings spread fire rebuilding, all three refusing to
fall despite overwhelming pressure, dark toxic atmosphere around them,
faces showing absolute determination not fear

MIDDLE PANEL (middle 33%):
medium shot same three heroes energy INTENSIFYING, sword blade now
blazing bright blue energy spreading to hands as veins, fox tail
splitting into nine-tail phantom formation purple-pink #F8B4C8
intensifying, enormous translucent golden-white phoenix phantom
emerging behind small phoenix 3m+ wingspan, all three energy colors
growing stronger than before, toxic mist beginning to be pushed back
in their immediate vicinity

BOTTOM PANEL (lower 33%):
medium-full shot pulled back, three heroes combined three-color aura
forming visible protective dome 3m radius, dome surface visible where
toxic rain impacts and deflects outward, inside dome clear and bright
outside dome dark toxic, three heroes united within dome faces forward,
sword immortal center speaking mouth open determined expression,
composition showing the dome of resistance against overwhelming dark

all panels: same three heroes same positions progressive energy buildup,
three colors #4A90D9+#E67E22+#F8B4C8 reclaiming dominance from toxic
green, emotional turning point, CG storyboard quality

negative prompt:
heroes falling, defeated posture, single character, calm scene,
cartoon, anime, sketch, text, daylight, horizontal
```

---

## SEG-09 · 对撞定格·片名转化（4s · 2格）

```
宫格结构：上下2格（9:16竖屏·上60%下40%）
格1(上60%) = T+2s 三色能量上冲vs毒流下压即将碰撞（全景·主画面）
格2(下40%) = T+3.5s 定格瞬间+片名字幕空间（干净暗底）
景别切换：全景动态 → 定格静画+字幕区
```

```
━━━━━━━━━━━━━━━━━━━━━━━━━━━
【操作指引】
  垫图上传：@图片3 万剑归宗技能态 + @图片8 朱雀觉醒
           + @图片9 相柳九首压下
  垫图权重：0.30-0.35（定格构图由提示词主导·参考图仅供形态参考）
  工具模式：Flux img2img 或 MJ --sref [@图片9] --cw 40
  备注：这是最终定格画面·要求所有能量轨迹"悬停"不运动
       下方40%需要保持相对干净暗色用于后期叠加字幕
       整体构图为上下对称：暖色上冲vs冷毒下压·中心碰撞白芯
━━━━━━━━━━━━━━━━━━━━━━━━━━━
```

**Nano Banana 提示词：**

```
prompt:
Game CG quality Chinese fantasy 3D animation storyboard,
9:16 vertical, two-panel vertical layout upper panel 60% lower panel
40% separated by 1px white line, FROZEN MOMENT maximum tension
composition, highly detailed:

UPPER PANEL (upper 60%):
epic full shot THE FRAME IS FROZEN all motion suspended in time,
three-color heroic energy rising UPWARD: blue sword trails #4A90D9
ascending frozen mid-flight, pink petal wave #F8B4C8 rising frozen
mid-surge, golden fire stream #E67E22 ascending frozen, versus from
above: nine serpent heads dark green toxic breath #27AE60 pouring
DOWNWARD frozen, all particles suspended motionless in air, convergence
point at center where three-color rising meets toxic descending is
brightest white-hot overexposed, absolute stillness maximum visual
tension 0.1 second before ultimate collision, sword immortal visible
small below with hundred swords launched, fox character nine-tail
phantom visible, phoenix phantom wings spread

LOWER PANEL (lower 40%):
clean dark space mostly #1A1A1A to #2C3E50 gradient, minimal content
only faint residual energy glow at top edge transitioning from upper
panel, this space reserved for title text overlay, kept deliberately
clean and simple dark tone for maximum text readability, subtle
ground-level energy reflections only

both panels: frozen moment still image quality, upper panel maximum
visual density and tension, lower panel clean for text, professional
CG storyboard final frame composition

negative prompt:
motion blur, movement, animated feel, bright lower panel, busy lower
panel, text already present, cartoon, anime, sketch, horizontal,
single panel, calm scene
```

---

## 交付总览

| SEG | 宫格数 | 垫图 | 核心重点 |
|---|---|---|---|
| 01 | 2格 | @图片11 | 纯场景·天空→地面 |
| 02 | 3格 | @图片1+3+11 | 剑仙+万剑归宗技能态 |
| 03 | 3格 | @图片9+10+12 | 相柳九首+妖潮 |
| 04 | 4格 | @图片1+7+8 | 朱雀变身渐变过程 |
| 05 | 3格 | @图片4+6+11 | 灵狐+桃花法阵技能态 |
| 06 | 4格 | @图片1+3+4+6+8 | 三方合击·三色并存 |
| 07 | 3格 | @图片9+10 | 相柳真身标志镜头 |
| 08 | 3格 | @图片1+3+4+8 | 情绪转折·能量重燃 |
| 09 | 2格 | @图片3+8+9 | 终极定格·字幕空间 |

---

## 使用流程

```
【完整执行流程】
═══════════════════════════════════════════════════════
① 按操作指引上传对应垫图 + 粘贴提示词 → 生成宫格分镜图
② 检查：朝向一致？色调统一？景别流畅？格间连贯？
③ 满意后将宫格图作为 style_reference 上传 Seedance
④ 配合 STEP5 时间轴连贯描述粘贴提示词框
⑤ Seedance 出片（宫格图锁视觉+文字锁动态=双重约束）
═══════════════════════════════════════════════════════
```

---

*全9条宫格分镜图提示词交付完毕*
