# 海塞姆科技文档仓库

深圳市海塞姆科技有限公司（Haytham AI）的公开文档仓库，使用 [mdBook](https://rust-lang.github.io/mdBook/) 构建并部署至 Cloudflare Pages。

## 技术栈

- **文档引擎**: [mdBook](https://rust-lang.github.io/mdBook/)（基于 Rust 的静态站点生成器）
- **持续集成和部署**: GitHub Actions
  - 自动检查：使用 [AutoCorrect](https://github.com/huacnlee/autocorrect) 进行中英文排版格式化
  - 自动构建：使用 `peaceiris/actions-mdbook` 安装 mdBook 并构建静态站点
  - 自动部署：推送到 `master` 分支后自动部署至 Cloudflare Pages
- **托管**: Cloudflare Pages
- **代码仓库**: GitHub ([haytham-ai/public-docs](https://github.com/haytham-ai/public-docs))
- **编辑体验**: 支持通过 GitHub 的“编辑此页”链接直接在线修改文档

## 本地开发

### 前提条件

1. 安装 mdBook：

   下载 [mdBook](https://github.com/rust-lang/mdBook/releases/latest) 可执行文件并放到环境变量包含的目录中。
   或使用包管理器（如 `pamac install mdbook`）。

2. 安装 AutoCorrect：

   下载 [AutoCorrect](https://github.com/huacnlee/autocorrect/releases/latest) 可执行文件并放到环境变量包含的目录中。
   或使用包管理器（如 `pamac install autocorrect-bin`）。

### 构建与预览

```bash
# 克隆仓库
git clone https://github.com/haytham-ai/public-docs.git
cd public-docs

# 本地构建（生成到 ./book 目录）
mdbook build

# 测试
mdbook test

# 本地预览（默认 http://localhost:3000）
mdbook serve
```

访问 http://localhost:3000 查看实时预览。

## 贡献指南

我们欢迎任何形式的贡献，包括但不限于：

- 修正错别字、语法错误
- 补充文档内容
- 改进文档结构
- 翻译或国际化

### 提交规范

本项目遵循 [PJ568 规范](https://github.com/PJ-568/git-commit-regulation)。

### 自动检查

每次合并请求都会触发以下检查：

- **多语言格式检查**：使用 AutoCorrect 自动修正混合文字排版
- **框架静态测试**：使用 mdBook 构建并测试文档完整性

请确保本地运行 `mdbook build` 和 `mdbook test` 通过后再提交。

## 提问与讨论

- **GitHub Issues**：[新建 Issue](https://github.com/haytham-ai/public-docs/issues) 用于报告问题、提出建议或发起讨论。
- **编辑页面**：每个文档页面的右上角都有“编辑此页”链接，可直接跳转到 GitHub 编辑界面。

## 许可证

本文档内容版权归深圳市海塞姆科技有限公司所有，仅供内部及合作伙伴参考使用。未经书面许可，不得转载或用于其他商业用途。

## 相关链接

- [GitHub 仓库](https://github.com/haytham-ai/public-docs)
- [mdBook 官方文档](https://rust-lang.github.io/mdBook/)
