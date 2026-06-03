# 团团 Codex 桌面宠物

这个仓库现在保留两个宠物：

- **团团**：原来的橘白小猫，目录 `v001-original`
- **红泰狮金鱼**：新增的红色泰狮金鱼，目录 `v004-red-taishi-goldfish`

猫不会被金鱼覆盖。安装时它们应该放进两个不同的 Codex pets 目录：`tuantuan` 和 `red-taishi-goldfish`。

## English Intro

This repository keeps the original Tuantuan orange-and-white kitten and adds a separate red Thai lionhead goldfish pet. They use different pet IDs, so installing the goldfish will not replace the cat.

| Pet | Version | Install directory |
|---|---|---|
| 团团小猫 | `v001-original` | `~/.codex/pets/tuantuan` |
| 红泰狮金鱼 | `v004-red-taishi-goldfish` | `~/.codex/pets/red-taishi-goldfish` |

## 金鱼预览

![红泰狮金鱼挥鳍](assets/v004/preview/waving.gif)

| 待机 | 工作中 | 认真 review |
|---|---|---|
| ![idle](assets/v004/preview/idle.gif) | ![running](assets/v004/preview/running.gif) | ![review](assets/v004/preview/review.gif) |

| 向右游 | 向左游 | 跳起来 |
|---|---|---|
| ![running right](assets/v004/preview/running-right.gif) | ![running left](assets/v004/preview/running-left.gif) | ![jumping](assets/v004/preview/jumping.gif) |

| 等你一下 | 失败委屈 | 打招呼 |
|---|---|---|
| ![waiting](assets/v004/preview/waiting.gif) | ![failed](assets/v004/preview/failed.gif) | ![waving](assets/v004/preview/waving.gif) |

完整精灵图总览：

![红泰狮金鱼精灵图总览](assets/v004/contact-sheet.png)

## 安装

### 安装两个宠物

```bash
git clone https://github.com/JbBom/tuantuan-codex-pet.git
cd tuantuan-codex-pet

mkdir -p ~/.codex/pets
rm -rf ~/.codex/pets/tuantuan
rm -rf ~/.codex/pets/red-taishi-goldfish
cp -R v001-original ~/.codex/pets/tuantuan
cp -R v004-red-taishi-goldfish ~/.codex/pets/red-taishi-goldfish
```

安装后重启 Codex，在 **Settings -> Pets** 中可以分别选择 **团团** 或 **红泰狮金鱼**。

### 只安装原来的猫

```bash
mkdir -p ~/.codex/pets
rm -rf ~/.codex/pets/tuantuan
cp -R v001-original ~/.codex/pets/tuantuan
```

### 只安装金鱼

```bash
mkdir -p ~/.codex/pets
rm -rf ~/.codex/pets/red-taishi-goldfish
cp -R v004-red-taishi-goldfish ~/.codex/pets/red-taishi-goldfish
```

## 版本说明

| 版本 | 说明 |
|---|---|
| `v001-original` | 原始橘白小猫版本，保留为 `tuantuan` |
| `v003-red-taishi-goldfish` | 废弃实验版，错误地复用了 `tuantuan` id |
| `v004-red-taishi-goldfish` | 当前金鱼版本，独立 id：`red-taishi-goldfish` |

`v004-red-taishi-goldfish/spritesheet.webp` 已通过 Codex pet atlas 校验：`1536x1872`、RGBA WebP、`8x9` atlas、透明像素残留为 `0`，没有 errors 或 warnings。

## 宠物文件

```text
v001-original/
  pet.json
  spritesheet.webp

v004-red-taishi-goldfish/
  pet.json
  spritesheet.webp

assets/
  v004/contact-sheet.png
  v004/preview/*.gif
```

## 许可证

[MIT](LICENSE) © JbBom
