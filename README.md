# MC NoJumpFix - 《我的世界》长按空格连跳禁用工具

![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11-blue)

专为《我的世界》跑酷地图设计的工具，彻底解决长按空格键导致的意外连跳问题。一键运行，零配置依赖！
A tool designed for Minecraft parkour maps, completely preventing accidental continuous jumps caused by holding the spacebar. One-click execution, zero dependencies!

## 🚀 功能亮点

- **精准拦截长按空格**  
  ✅ 短按空格 → 正常跳跃 1 次                          Short press Space → Normal jump (1 time)  
  ✅ 长按空格 → **仅触发单次跳跃**（按住不放不会连跳）   Long press Space → **Single jump only** (no continuous jumps)  
  ✅ 快速连点空格 → 保留手动多次跳跃的自由度            Rapid clicks → Manual multi-jumps preserved  

- **轻量无感运行**  
  🔋 后台内存占用 < 1MB，不影响游戏性能  

- **智能窗口识别**  
  🎮 仅针对《我的世界》生效，其他程序空格键功能完全保留  

- **自由开关控制**  
  ⚙️ 右键系统托盘图标（H 图标）→ 随时暂停或退出脚本  


## 📥 下载与使用

### 步骤 1：下载工具
前往 [Release 页面](https://github.com/yourusername/MC_NoJumpFix/releases) 下载最新版 `MC_NoJumpFix.exe`。

### 步骤 2：运行工具
- **右键文件** → **以管理员身份运行**  
  ![管理员权限提示](https://i.imgur.com/5qL9Z8s.png)  
  *（首次运行需允许权限，否则无法拦截游戏按键）*

### 步骤 3：验证效果
1. 启动《我的世界》并进入游戏。
2. **短按空格** → 应跳跃 1 次。
3. **长按空格不放** → 仅跳跃 1 次，无连跳。
4. **Shift+空格疾跑** → 功能正常保留。

## 🖥️ 兼容性

| 游戏版本       | 进程名                   | 支持状态 |
|----------------|--------------------------|----------|
| Java 版        | `java.exe` / `javaw.exe` | ✅ 全适配 |
| 基岩版 (Win10/11) | `Minecraft.Windows.exe` | ✅ 全适配 |

**系统要求**：Windows 10/11（需管理员权限）

## ⚠️ 注意事项
- 部分多人服务器可能检测为作弊工具，使用前请确认规则。  
- 若脚本未生效，请检查游戏进程名是否为 `java.exe`。  

## 🙌 贡献与反馈
欢迎提交 Issue 或 PR！遇到问题请提供：  
1. 游戏版本与启动器名称  
2. 任务管理器中的进程截图  

## ⚙️ 高级配置

### 自定义按下时长
编辑脚本中的 `Sleep` 参数（需安装 [AutoHotkey](https://www.autohotkey.com)）：
```autohotkey
$Space::
    Send {Blind}{Space Down}
    Sleep 80  ; 调整此值（单位：毫秒）
    Send {Blind}{Space Up}
    KeyWait, Space
return


