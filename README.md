# 网页小游戏合集

两个纯前端的单文件网页游戏，**双击就能玩，不需要联网、不需要安装、没有任何外部依赖**。

在线试玩：把本仓库开启 GitHub Pages 后，访问 `https://liuhuize0711git.github.io/html-games/`，
根目录的入口页会直接链接到这两个游戏。

---

## 游戏列表

| 游戏 | 目录 | 类型 | 说明 |
| --- | --- | --- | --- |
| 围棋 · Go | [`go-game/`](go-game/) | 棋类对弈 | 支持单人（对战电脑）与双人模式，鼠标点交叉点落子，手机上也能下 |
| 尖塔行者 · Spire Wanderer | [`spire-wanderer/`](spire-wanderer/) | 卡牌构筑 Roguelike | 网页版爬塔游戏，卡牌、敌人、遗物、商店、事件与 C 版保持一致 |

每个目录下都有一份更详细的说明（`README.md`）。

---

## 怎么运行

**方式一：本地直接打开**

双击对应目录里的 `index.html`，或者把文件拖进浏览器窗口即可。

**方式二：本地起一个静态服务**（部分浏览器对本地文件的权限限制较严时更稳）

```bash
cd html-games
python -m http.server 8000
# 然后浏览器打开 http://localhost:8000/
```

**方式三：在线玩**

仓库开启 GitHub Pages 后访问仓库的 Pages 地址即可，见下方「发布到线上」。

---

## 目录结构

```
html-games/
├── index.html             # 入口页，链接到下面两个游戏
├── README.md
├── go-game/
│   ├── index.html         # 围棋（单文件，约 95 KB）
│   └── README.md
└── spire-wanderer/
    ├── index.html         # 尖塔行者（单文件，约 342 KB）
    └── README.md
```

---

## 发布到线上（GitHub Pages）

1. 打开仓库页面 → **Settings** → 左侧 **Pages**
2. Source 选择 **Deploy from a branch**
3. Branch 选 **main**，目录选 **/ (root)**，点 **Save**
4. 等一两分钟，访问 `https://liuhuize0711git.github.io/html-games/`

---

## 技术说明

- 两个游戏都是**单文件 HTML**：结构、样式、脚本全部内联在一个文件里，方便分享和托管
- 渲染使用 Canvas / DOM，逻辑用原生 JavaScript 编写，没有引入任何框架或 CDN
- 无后端、无数据上报，所有状态保存在浏览器本地

