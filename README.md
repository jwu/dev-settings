# 开发环境配置

## Windows 配置方案

### 自动配置 (推荐)

1. 打开终端。
2. 进入 `win` 目录：
   ```bash
   cd ~/bin/dev-settings/win
   ```
3. 运行开发环境配置脚本：
   ```bash
   ./setup_dev.bat

### 手动配置

1. 阅读 [MSVC](https://github.com/nvim-treesitter/nvim-treesitter/wiki/Windows-support#msvc) session
2. 安装 [Visual Studio Build Tools](https://visualstudio.microsoft.com/zh-hans/downloads/?q=build+tools+for+visual+studio)

## Mac 配置方案

MacOS 开发环境自动配置脚本，会安装以下开发工具和运行时。

### 自动配置 (推荐)

1. 打开终端。
2. 进入 `mac` 目录：
   ```bash
   cd ~/bin/dev-settings/mac
   ```
3. 运行开发环境配置脚本：
   ```bash
   ./setup_dev.sh
   ```

**安装的工具包括：**
- **Xcode Command Line Tools** - Apple 官方编译工具链
- **Git** - 版本控制工具
- **Rust (rustup)** - Rust 编程语言及工具链
- **uv** - Python 快速包管理器和安装器
- **Bun** - 快速的 JavaScript 运行时和包管理器
- **Zig** - Zig 编程语言
- **tree-sitter-cli** - 解析器生成工具
- **Node.js (LTS)** - JavaScript 运行时（通过 NVM）

### 手动配置

如果你更喜欢手动安装这些工具，请按照以下步骤操作：

1. 安装 Xcode Command Line Tools
  ```bash
  xcode-select --install
  ```
  等待安装对话框完成。

2. 安装 Git (如果尚未安装)
  ```bash
  brew install git
  ```

3. 安装 Rust
  ```bash
  curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y
  source "$HOME/.cargo/env"
  ```

4. 安装 Zig
  ```bash
  brew install zig
  ```

5. 安装 tree-sitter-cli
  ```bash
  cargo install tree-sitter-cli
  ```

6. 安装 uv (Python 工具)
  ```bash
  curl -LsSf https://astral.sh/uv/install.sh | sh
  ```

7. 安装 Bun
  ```bash
  curl -fsSL https://bun.sh/install | bash
  ```

8. 安装 Node.js (通过 NVM)
  ```bash
  export NVM_DIR="$HOME/.nvm"
  curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
  [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
  nvm install --lts
  nvm use --lts
  nvm alias default 'lts/*'
  ```

---

## Reference

- Language
  - [Rust](https://rust-lang.org/)
  - [Zig](https://ziglang.org/)
  - [Python](https://www.python.org/)
  - [TypeScript](https://www.typescriptlang.org/)
  - [Lua](https://www.lua.org/)
    - [Lua](https://luajit.org/)
- Package Management
  - [uv](https://github.com/astral-sh/uv)
  - [bun](https://github.com/oven-sh/bun)
  - [nvm](https://github.com/nvm-sh/nvm)
  - [mise](https://github.com/jdx/mise)
- Node.js
  - [deno](https://github.com/denoland/deno)
  - [tauri](https://github.com/tauri-apps/tauri)
- utils
  - [hexyl](https://github.com/sharkdp/hexyl)
  - [xh](https://github.com/ducaale/xh)
  - [yq](https://github.com/mikefarah/yq)
    - [jq](https://github.com/stedolan/jq)
  - [sttr](https://github.com/abhimanyu003/sttr)
  - [grex](https://github.com/pemistahl/grex)
  - [hyperfine](https://github.com/sharkdp/hyperfine)
- Version Control
  - [lazygit](https://github.com/jesseduffield/lazygit)
    - [gitui](https://github.com/gitui-org/gitui)
  - [gh](https://github.com/cli/cli)
  - [worktrunk](https://github.com/max-sixty/worktrunk)
- AI dev
  - [opencode](https://opencode.ai/)
  - [llmfit](https://github.com/AlexsJones/llmfit)
