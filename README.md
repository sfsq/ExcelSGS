# 素材更新工具

用于管理和更新游戏素材资源文件的工具。

## 快速开始

把 `MaterialUpdateTool.exe` 放到本目录（`essck`）下，双击运行即可。

```
essck/
├── MaterialUpdateTool.exe    ← 放这里
├── README.md                 ← 本文件
└── material/                 ← 自动扫描此目录
    ├── tianming/ExcelSGS/    ← 素材目录
    ├── guanfang/ExcelSGS/
    └── ...
```

## 操作说明

- **↑ ↓** 方向键选择素材
- **Enter** 确认执行更新
- **q** 退出程序
- 默认选中 **天命(默认)**

## 支持的素材

| 名称 | 文件夹 | 说明 |
|------|--------|------|
| 天命(默认) | `tianming` | 默认素材 |
| 扩展 | `kuozhan` | 扩展素材（目录结构不同） |
| 水墨 | `shuimo` | 水墨风格 |
| Q版粤语 | `qbanyueyu` | Q版粤语配音 |
| 官方 | `guanfang` | 官方素材 |
| 其他 | `xxx` | 未知素材自动识别 |

## 首次使用

如果没有素材目录，程序会询问是否创建目录结构：
- 选 **0** → 仅创建 天命(默认)
- 选 **1** → 创建全部 5 个素材

创建后把素材文件放入对应目录即可。

## 目录结构

### 标准素材（tianming, guanfang, shuimo, qbanyueyu）
```
material/xxx/ExcelSGS/
├── drawable/   ← 存放图片 (.png)
├── raw2/       ← 存放音频 (.ogg)
└── data/       ← 自动生成的索引文件
```

### 扩展素材（kuozhan）
```
material/kuozhan/ExcelSGS/
├── extension/  ← 存放脚本/配置 (.js, .txt, .json)
├── editor/     ← 存放编辑器文件
└── data/       ← 自动生成的索引文件
```

## 生成的文件

运行后会在 `data/` 目录生成以下文件：

| 文件 | 说明 |
|------|------|
| `data.json_sgs` | 所有素材文件清单 |
| `data_special.json_sgs` | 超过 1MB 被拆分的文件清单 |
