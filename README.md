![Windows/Ubuntu/MacOS](https://github.com/LeagueRaINi/Aida64-Keygen/workflows/Windows/Ubuntu/MacOS/badge.svg)

# **This is for educational purposes only!**
- this project contains methods for generating and verifying aida64 keys

**Thanks to:**
- approved for helping reverse some of this
- wildbook & veykril for helping me a lot converting this to rust
- moonshadow565 for explaining and simplifying some of the methods

  ---
https://www.extremexbb.com/aida64-keys/

  伸手党专用编译好下载链接
仅供学习交流，严禁用于商业用途，请于24小时内删除

使用的源代码版本位于 commit 671ebf719d9af74cdaace4f4122d1caeb8dbd393

我错了，才发现 115 网盘下载共享文件要登陆账号，迁移到百度网盘

Windows:

链接：https://pan.baidu.com/s/1y3pkvuzAnVBfufUXT_VDbA
提取码：B6YA

Linux:

链接：https://pan.baidu.com/s/1beoB2waKWWLRTip8f-8pUw
提取码：AG5Y

# 使用说明
以 Windows GUI 版本为例

1. 运行 aida64-keys-gui.exe
2. Generate 按钮旁边 切换版本，如 Extreme 或 Business 版
3.（可选）Purchase Date 选项设置为想要的购买日期
4.（可选）Expire Date 设置为想要的授权期限，或勾选旁边的 No Expiry 就是永不过期
5.（可选）Maintenance Expire Date 设置为想要的维护期限
6. 点击 Generate 按钮
7. 点击右边生成的序列号，自动复制到剪贴板
8. AIDA64 中粘贴序列号

# Build
我使用的环境是 Ubuntu 22.04，理应 Debian 11 也不会有什么问题

```
# 安装 Rust 编译环境
curl https://sh.rustup.rs -sSf | sh
# 安装其他依赖项
apt update
apt install pkg-config cmake build-essential libxcb-composite0-dev libfontconfig1-dev
# 克隆源码
git clone https://github.com/LeagueRaINi/Aida64-Keys.git
# 编译
cd ./Aida64-Keys
cargo build --verbose
```

# 如果想要 Windows 的文件，那就继续这么弄

```
# 安装 MinGW-w64 作为开发环境
apt install mingw-w64
# 添加 Windows GNU目标
rustup target add x86_64-pc-windows-gnu
# 编译
cargo build --target x86_64-pc-windows-gnu
```

# 编译成功的话，可执行文件会在这个目录里面
```
# Linux
./target/debug/
# Windows
./target/x86_64-pc-windows-gnu/debug/
```
