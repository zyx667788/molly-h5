# 🎨 《云上创想·青春向新》H5 图像素材生成清单

> **更新时间：** 2026-05-05
> **生成工具：** 统一使用 `opencli chatgpt image`（gemini image 已不可用）
> **画幅比例：** 9:16 竖屏（1080×1920）
> **输出目录：** `~/tmp/molly-h5-images/`

---

## 一、封面页 P1 — 云海光束（纯视觉）

**用途：** 全屏背景，营造"穿越云层、创意启程"的仪式感
**文字密度：** 低（仅叠加主标题 + 按钮）

```
opencli chatgpt image "A vast luminous cloud sea viewed from above at golden hour, soft volumetric light beams piercing through translucent cloud layers in blue-purple gradients, a single glowing particle trail spiraling upward like a creative spark, minimalist futuristic aesthetic, no text, dreamy atmospheric depth, color palette: deep azure #4A90D9 to violet #7B68EE with warm gold #FFD700 accents, vertical composition 9:16 aspect ratio" --op ~/tmp/molly-h5-images/ --f yaml
```

**备选/简化版（如果上面太长）：**

```
opencli chatgpt image "Dreamy cloud sea panorama with light beams breaking through, blue-purple gradient sky, single golden spark trail rising upward, futuristic minimalist style, no text, vertical 9:16" --op ~/tmp/molly-h5-images/ --f yaml
```

---

## 二、命题说明页 P2 — 信息卡片背景

**用途：** 卡片式布局背景，不需要大面积图像，用 CSS 渐变即可
**文字密度：** 高（主题介绍文字）
**策略：** **不需要 AI 生图**，用 CSS 毛玻璃 + 渐变背景实现，成本更低效果更统一

> ✅ **跳过图像生成，由 @ui-specialist 用 CSS 实现**

---

## 三、场景痛点页 P3 — 校园创意场景插画

**用途：** 展示"大学生创作中遇到困难"的场景，需要亲和力
**文字密度：** 中（叠加选项卡文字）

```
opencli chatgpt image "Flat illustration of university students collaborating on creative projects in a modern campus studio, laptops and tablets scattered around, warm lighting, diverse group of young people brainstorming with sticky notes and screens, soft color palette with blue and purple tones, friendly optimistic mood, no text, vertical 9:16 composition, contemporary digital illustration style" --op ~/tmp/molly-h5-images/ --f yaml
```

**备选版：**

```
opencli chatgpt image "Young diverse students working together on digital creative projects, modern campus setting, warm studio lighting, laptops tablets sticky notes, blue-purple color accents, flat illustration style, no text, vertical 9:16" --op ~/tmp/molly-h5-images/ --f yaml
```

---

## 四、解决方案页 P4 — 云朵组件元素

**用途：** 三个可拖拽的"云朵卡片"图标（云算力/云协作/云智创）
**文字密度：** 低（图标+短标签）
**策略：** 用 SVG/CSS 绘制云朵形状更灵活，**但准备一张背景氛围图**

```
opencli chatgpt image "Three floating translucent cloud shapes in a row against a soft gradient background, each cloud has a subtle different glow - blue for computing, purple for collaboration, gold for AI creation, minimalist tech aesthetic, glassmorphism style, no text, clean modern design, vertical 9:16" --op ~/tmp/molly-h5-images/ --f yaml
```

**备选版：**

```
opencli chatgpt image "Three glowing cloud icons floating on gradient background, blue purple and gold colors, translucent glassmorphism effect, minimalist, no text, vertical 9:16" --op ~/tmp/molly-h5-images/ --f yaml
```

---

## 五、闯关测试页 P5 — 答题界面装饰

**用途：** 答题卡片区域的装饰元素/背景
**文字密度：** 高（题目+选项文字）
**策略：** **不需要 AI 生图**，答题界面用纯 CSS 实现更干净

> ✅ **跳过图像生成，由 @ui-specialist 用 CSS 实现**

---

## 六、成果海报页 P6 — 创意名片背景

**用途：** 用户答题后生成的"创意名片"底图，需要高颜值可分享
**文字密度：** 中（叠加结果文字）

```
opencli chatgpt image "Elegant gradient poster background transitioning from deep blue to purple with scattered golden light particles, abstract flowing energy ribbons, premium feel like a digital award certificate, no text, luminous and celebratory mood, vertical 9:16 composition" --op ~/tmp/molly-h5-images/ --f yaml
```

**备选版：**

```
opencli chatgpt image "Blue to purple gradient poster background with golden sparkles and flowing light ribbons, celebratory premium feel, digital award style, no text, vertical 9:16" --op ~/tmp/molly-h5-images/ --f yaml
```

---

## 七、收束页 P7 — 二维码区域背景

**用途：** 二维码/链接展示的背景，需要简洁不抢焦
**文字密度：** 中
**策略：** 复用 P1 封面图降低透明度即可，**不需要单独生成**

> ✅ **复用 P1 封面图 + CSS 降低 opacity**

---

## 八、封面标题装饰 — 光效叠加层

**用途：** 封面标题文字下方的光效装饰
**策略：** CSS radial-gradient + animation 实现，无需 AI 生图

> ✅ **CSS 实现**

---

## 📋 生成执行优先级

| 优先级 | 页面 | 内容 | 工具 | 预估时间 |
|--------|------|------|------|---------|
| 🔴 P0 | P1 封面 | 云海光束背景 | opencli chatgpt image | ~2min |
| 🔴 P0 | P6 海报 | 创意名片背景 | opencli chatgpt image | ~2min |
| 🟡 P1 | P3 场景 | 校园协作插画 | opencli chatgpt image | ~2min |
| 🟡 P1 | P4 方案 | 云朵组件背景 | opencli chatgpt image | ~2min |
| ⚪ 跳过 | P2 | CSS 毛玻璃 | — | — |
| ⚪ 跳过 | P5 | CSS 答题卡 | — | — |
| ⚪ 复用 | P7 | 复用 P1 降低透明度 | — | — |

**总计需生成：4 张图**（全部走 opencli chatgpt image）
**兜底方案：** 如果 chatgpt image 也不可用，回退到内联 SVG 插画

---

## ⚠️ 已知问题 & 注意事项

1. **opencli gemini image 已完全不可用**（2026-05 确认），不再尝试
2. **opencli chatgpt image** 偶尔也会不稳定，建议按优先级逐张生成
3. **Prompt 长度**：超过 200 词可能解析出错，上述 prompt 已控制在 80 词以内
4. **如果连续失败**：回退到 CSS 渐变 + SVG 插画方案，不卡流程
5. 生成后图片会自动下载到 `--op` 指定目录，用 `file` 命令验证是否为有效图片
