# 🐱 团团 — Codex 桌面宠物

**一只软萌、友好的橘白短毛小猫。**

由 [jbbom](https://github.com/jbbom) 在 Codex 中生成，托管于 [codex-pet-share](https://codex-pet-share.pages.dev)。

---

## 预览

团团是一只橘白相间的可爱小猫，会在你的 Codex 桌面陪伴你。

> `v001-original/spritesheet.webp` — 猫咪各个姿态的精灵图（包含 idle、walk、sleep 等动画帧）

---

## 安装

### 前提条件

- 已安装 [Codex](https://codex.ai)（OpenAI 的 AI 编程助手）
- Codex 版本支持 Pets 功能（`~/.codex/pets/` 目录）

### 安装步骤

```bash
# 1. 克隆仓库（或下载 ZIP）
git clone https://github.com/jbbom/tuantuan-codex-pet.git
cd tuantuan-codex-pet

# 2. 复制宠物到 Codex
cp -r v001-original ~/.codex/pets/tuantuan

# 3. 验证安装
ls ~/.codex/pets/tuantuan/
# 应该看到: pet.json  spritesheet.webp
```

安装后重启 Codex，团团就会出现在你的宠物列表中。

### 一键安装（快捷版）

```bash
git clone https://github.com/jbbom/tuantuan-codex-pet.git /tmp/tuantuan && cp -r /tmp/tuantuan/v001-original ~/.codex/pets/tuantuan && rm -rf /tmp/tuantuan
```

---

## 如何使用

在 Codex **设置 → Pets** 中：

1. 选择 **团团** 作为当前宠物
2. 它就会出现在桌面陪你啦 🎉

团团支持 idle 待机动画，当你 Coding 时它会安静地陪伴你。

---

## 卸载

```bash
rm -rf ~/.codex/pets/tuantuan
```

重启 Codex 即可。

---

## 宠物格式说明

```
~/.codex/pets/
  └── <pet-id>/
       ├── pet.json           ← 宠物元数据
       └── spritesheet.webp   ← 精灵图（1.7MB, WebP 格式）
```

`pet.json` 字段：

| 字段 | 说明 |
|------|------|
| `id` | 宠物唯一标识（文件夹名） |
| `displayName` | 显示名称 |
| `description` | 宠物描述 |
| `spritesheetPath` | 精灵图文件名 |
| `author` | 作者 GitHub ID |
| `tags` | 分类标签 |
| `source` | 来源标识 |
| `sourceUrl` | 来源链接 |

---

## 许可证

[MIT](LICENSE) © jbbom

---

*用 ❤️ 和 Codex 生成*
