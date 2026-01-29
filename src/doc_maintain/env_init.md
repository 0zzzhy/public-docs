# 软件环境初始化

可选在线维护和本地维护两种方式。

在线维护仅需网页环境即可修改维护，但对 Git 提交（Commit）的修改和文档的测试需依赖仓库持续集成。

本地维护需安装并配置多个软件并拉取仓库到本地，对 Git 提交（Commit）的修改和文档测试更友好。

## 在线维护

### 仓库配置

[**点击我以复刻（Fork）本仓库**](https://github.com/haytham-ai/public-docs/fork)，选择“Create fork”按钮。

您应看到在您的命名空间中的仓库如 `your-user-name/public-docs`，其中 `your-user-name` 为您的 GitHub 用户名。
地址似 `https://github.com/your-user-name/public-docs`。
下文称做“您的仓库”。

**启用持续集成自动测试工作流**：
在您的仓库的主页面（`Code` 页面）中，点击 `Settings`，然后点击 `Actions`，选择 `General`，
确保 `Actions permissions` 设置为 `Allow all actions and reusable workflows`；
确保 `Workflow permissions` 设置为 `Read and write permissions`。

### 启动在线编辑器

在您的仓库的主页面（`Code` 页面）中，按下键盘上的句号键 <kbd>.</kbd>，
或访问 `https://github.dev/your-user-name/public-docs` 启动网页编辑器进行编辑。

## 本地维护

### 软件安装

开始在本地维护前，请确保已安装以下软件：

- [Git](https://git-scm.com/)：

  确保运行 `git --version` 命令无报错。

- [mdBook](https://github.com/rust-lang/mdBook/releases)，选择版本：{{ mdbook-version }}：
  - 使用包管理器安装，如执行 `pamac install mdbook`。
  - 对应操作系统下载后解压出可执行文件并放到环境变量包含的目录中。

  确保运行 `mdbook --version` 命令无报错。

- [AutoCorrect](https://github.com/huacnlee/autocorrect/releases/latest)（可选）：
  - 使用包管理器安装，如执行 `pamac install autocorrect-bin`。
  - 对应操作系统下载后解压出可执行文件并放到环境变量包含的目录中。

  确保运行 `autocorrect --version` 命令无报错。

### 仓库配置

[**点击我以复刻（Fork）本仓库**](https://github.com/haytham-ai/public-docs/fork)，选择“Create fork”按钮。

您应看到在您的命名空间中的仓库如 `your-user-name/public-docs`，其中 `your-user-name` 为您的 GitHub 用户名。
地址似 `https://github.com/your-user-name/public-docs`。
下文称做“您的仓库”。

**启用持续集成自动测试工作流**：
在您的仓库的主页面（`Code` 页面）中，点击 `Settings`，然后点击 `Actions`，选择 `General`，
确保 `Actions permissions` 设置为 `Allow all actions and reusable workflows`；
确保 `Workflow permissions` 设置为 `Read and write permissions`。

### 拉取至本地

在终端模拟器或命令行执行：

```bash
git clone https://github.com/your-user-name/public-docs.git
```

即可拉取仓库到本地目录 `public-docs`。

在该目录下启动您喜好的编辑器，就可开始编写文档了。
