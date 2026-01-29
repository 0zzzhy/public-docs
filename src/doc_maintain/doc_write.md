# 文档的编写

## 目录结构示例

```plaintext
src/
├── index.md                # 文档首页
├── SUMMARY.md              # 目录配置文件
├── products/               # 产品类
│   ├── index.md
│   ├── videoextensometer/  # 视频引伸计类
│   │   ├── index.md
│   │   └── ...
│   └── visualstraingauge/  # DIC 系统类
│       ├── index.md
│       └── DIC_Tracker_ONS-B-10/
│           ├── v0.5.1/     # 产品
│           │   ├── index.md
│           │   └── ...
│           └── v0.5.0/
│               ├── index.md
│               └── ...
├── ...
└── doc_maintain/           # 文档维护（当前目录）
    ├── index.md            # 文档维护首页（章节描述）
    ├── env_init.md
    ├── doc_write.md        # 文档的编写（当前页面）
    └── doc_format.md
```

## 须知

- `src/SUMMARY.md` 文件为目录结构，请勿删除。
- 所有的文档名称和层级关系必须在 `src/SUMMARY.md` 文件中定义，否则无法在在线文档中显示。
- 为防止自动化脚本解析出错，所有目录（文件夹）名称仅能由英文字母、下划线、减号、点和数字组成，且不能以下划线、减号、点或数字开头。
