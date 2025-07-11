<h1 align="center"> OpenSpeedy </h1>


<p align="center">
  <img style="margin:0 auto" width=100 height=100 src="https://github.com/user-attachments/assets/bdbe4a60-7692-4e9c-9df4-ad1711337c57">
  </img>  
</p>

<p align="center">
  OpenSpeedy 是一款开源免费的游戏变速工具，让你的游戏突破帧率限制，提供更流畅丝滑的游戏加速体验。
</p>

<p align="center">
  <img src="https://api.visitorbadge.io/api/visitors?path=game1024.openspeedy&countColor=%234ecdc4">
  <br/>
  
  <a href="https://github.com/game1024/OpenSpeedy/issues">
    <img src="https://img.shields.io/github/issues-raw/game1024/OpenSpeedy?style=for-the-badge&label=Issues&color=orange" alt="Github Issues">
  </a>
  
  <a href="https://github.com/game1024/OpenSpeedy/stargazers">
    <img src="https://img.shields.io/github/stars/game1024/OpenSpeedy?style=for-the-badge&color=yellow" alt="GitHub Stars">
  </a>

  <img src="https://img.shields.io/github/forks/game1024/OpenSpeedy?style=for-the-badge&color=8a2be2" alt="GitHub Forks">
  <br/>  
  
  <a href="https://github.com/game1024/OpenSpeedy/releases">
    <img src="https://img.shields.io/github/downloads/game1024/OpenSpeedy/total?style=for-the-badge" alt="Downloads">
  </a>
  <a href="https://github.com/game1024/OpenSpeedy/releases">
    <img src="https://img.shields.io/github/v/release/game1024/OpenSpeedy?style=for-the-badge&color=brightgreen" alt="Version">
  </a>
  <a href="https://github.com/game1024/OpenSpeedy">
    <img src="https://img.shields.io/badge/Platform-Windows-lightblue?style=for-the-badge" alt="Platform">
  </a>
  <br/>
  
  <a href="https://github.com/game1024/OpenSpeedy/commits">
    <img src="https://img.shields.io/github/commit-activity/m/game1024/OpenSpeedy?style=for-the-badge" alt="提交活跃度">
  </a>
  <img src="https://img.shields.io/badge/language-C/C++-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/License-GPLv3-green.svg?style=for-the-badge">
  <br/>
</p>

<p align="center">
  <a href="https://github.com/game1024/OpenSpeedy">
    简体中文
  </a>
  ·
  <a href="https://github.com/game1024/OpenSpeedy/blob/master/docs/README_ja.md">
    日本語
  </a>
  ·
  <a href="https://github.com/game1024/OpenSpeedy/blob/master/docs/README_en.md">
    English
  </a>
</p>


# 🚀 特性
- 完全免费且开源
- 简单易用的界面
- 可自定义变速倍率
- 对多种游戏引擎兼容性良好
- 低系统资源占用
- 同时可以加速x86和x64平台进程
- 无内核侵入性，Ring3层Hook，不破坏系统内核

# 📥安装
1. 访问[安装页面](https://github.com/game1024/OpenSpeedy/releases) 下载最新版本
2. 解压缩下载的文件包到任意位置
3. 无需安装，直接运行 OpenSpeedy.exe 即可使用

# 💻 操作系统要求
- OS: Windows10 以上
- 平台：x86（32位） 和 x64 （64位）


# 📝 使用说明
1. 启动 OpenSpeedy
2. 运行需要变速的目标游戏
<img src="https://github.com/user-attachments/assets/648e721d-9c3a-4d82-954c-19b16355d084" width="50%">

3. 勾选游戏进程，在 OpenSpeedy 界面中调整速度倍率
<img src="https://github.com/user-attachments/assets/9469aae9-8be0-4e40-884d-1fbea3206e73" width="50%">

4. 即刻生效，对比效果如下

<video src="https://github.com/user-attachments/assets/74471b1f-7f95-4de8-b5aa-7edc85c9d5f0" width="70%"></video>

# 🔧 技术原理
OpenSpeedy 通过 Hook 以下 Windows 系统时间函数来实现游戏速度调整：

|函数名	| 所属库 |	功能 |
|--------|----------|------------------|
|Sleep|user32.dll|线程休眠|
|SetTimer|user32.dll|创建基于消息的计时器|
|timeGetTime | winmm.dll	| 获取系统启动后经过的毫秒数 |
|GetTickCount | kernel32.dll	| 获取系统启动后经过的毫秒数 |
|GetTickCount64	| kernel32.dll	| 获取系统启动后经过的毫秒数(64位) |
|QueryPerformanceCounter |	kernel32.dll	| 高精度性能计数器 |
|GetSystemTimeAsFileTime |	kernel32.dll	| 获取系统时间 |
|GetSystemTimePreciseAsFileTime |	kernel32.dll	| 获取高精度系统时间 |

# ⚠️ 注意事项
- 本工具仅供学习和研究使用
- 部分在线游戏可能有反作弊系统，使用本工具可能导致账号被封禁
- 过度加速可能导致游戏物理引擎异常或崩溃
- 不建议在竞技类在线游戏中使用
- 开源产品不带数字签名，可能被杀毒软件误报

# 🔄 反馈
如果在使用过程中遇到任何问题，欢迎通过以下方式反馈：
- [GitHub Issues](https://github.com/game1024/OpenSpeedy/issues) - 提交问题报告


# 📜 开源协议
OpenSpeedy 遵循 GNU v3 许可证。

# 🙏 鸣谢
OpenSpeedy使用到以下项目的源码，感谢开源社区的力量，如果OpenSpeedy对你有帮助，欢迎Star!
- [minhook](https://github.com/TsudaKageyu/minhook): 用于API Hook
- [Qt](https://www.qt.io/): GUI

免责声明: OpenSpeedy 仅用于教育和研究目的。用户应自行承担使用本软件的所有风险和责任。作者不对因使用本软件导致的任何损失或法律责任负责。

<p align="center">
  <img src="https://api.star-history.com/svg?repos=game1024/openspeedy&type=Date" Alt="Star History Chart">
</p>
