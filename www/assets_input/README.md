# 图片输入文件夹

## 📂 使用流程

1. **将生成的 512×512 图片放入对应文件夹**
2. **运行压缩脚本**: `python3 resize_images.py`
3. **自动输出到游戏 assets 文件夹**

## 📁 文件夹结构

```
assets_input/                    ← 你放 512x512 图片的地方
├── characters_player/          ← 主角行走动画 (32张)
│   ├── 01.png                  ← 朝下第1帧
│   ├── 02.png                  ← 朝下第2帧
│   └── ... (按顺序放)
├── characters_npc/             ← NPC角色
│   ├── merchant.png
│   └── guard.png
└── buildings/                  ← 建筑
    ├── house.png
    └── shop.png

assets/                         ← 脚本自动输出到这里
├── characters/
│   ├── player/walk/           ← 64x64 压缩后的主角
│   └── npc/                   ← 64x64 压缩后的NPC
└── buildings/                 ← 128x160 压缩后的建筑
```

## 🎯 图片规格对照表

| 类型 | 输入尺寸 | 输出尺寸 | 存放位置 |
|-----|---------|---------|---------|
| 主角行走帧 | 512×512 | 64×64 | `assets/characters/player/walk/` |
| NPC | 512×512 | 64×64 | `assets/characters/npc/` |
| 建筑 | 512×512 | 128×160 | `assets/buildings/` |

## 🚀 快速使用

```bash
# 1. 放入图片后运行
python3 /Users/genji/.openclaw/workspace/resize_images.py

# 2. 查看输出
ls -la /Users/genji/.openclaw/workspace/assets/
```
