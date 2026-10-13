# Sunset Valley · 江南春色

An interactive Song-dynasty Jiangnan river valley built with Three.js — a single HTML file, no external assets.
Drift down a winding river in a wooden boat past stone arch bridges, weeping willows, flowering cherry/peach trees,
reeds, lotus leaves, white-walled houses and a seven-story Song pagoda, wrapped in ink-wash morning mist.

一个用 Three.js 写成的宋代江南山水互动场景：单个 HTML 文件，不依赖任何外部素材。
乘一叶木舟顺河而下，经过石拱桥、垂柳、樱花与桃花、芦苇、荷叶、粉墙黛瓦的民居和七层宋塔，晨雾如水墨。

## Run / 运行

Open `index.html` in a modern browser (Chrome, Edge, Safari). Three.js loads from a CDN, so an internet connection is needed the first time.

用浏览器直接打开 `index.html` 即可（首次需要联网加载 Three.js）。

- Drag to look around · 拖拽鼠标环顾四周
- Space to pause the boat · 空格键暂停/继续行船
- `?u=0.5` start at a point along the river (0–0.97) · 从河道中某处出发
- `?low` lighter mode for weaker GPUs (smaller near-detail radius, no shadows) · 低配模式

## Highlights / 技术要点

- Custom GLSL water: planar reflection, animated ripple distortion, shoreline foam, view-dependent sun glitter
- Procedural trees: real branching structure; near trees get individual 3D blossoms and folded willow leaves, distant trees use painted cards (per-tree LOD)
- All textures (blossoms, willow leaves, roof tiles, plaster, wood, stone) painted on canvases at start-up
- PBR materials with a procedural sky environment map, soft sun shadows
- Post-processing: bloom, depth of field, distance + height fog, ink-wash colour grading
