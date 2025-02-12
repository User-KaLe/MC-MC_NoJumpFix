
---

### **英文版 README.md**
```markdown
# MC NoJumpFix - Minecraft Hold-to-Jump Disabler  
![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11-blue)

A tool designed for Minecraft parkour maps, completely preventing accidental continuous jumps caused by holding the spacebar. One-click execution, zero dependencies!

---

## 🚀 Key Features
- **Precise Hold-to-Jump Interception**  
  ✅ Short press Space → Normal jump (1 time)  
  ✅ Long press Space → **Single jump only** (no continuous jumps)  
  ✅ Rapid clicks → Manual multi-jumps preserved  

- **Lightweight Operation**  
  🔋 Background memory usage < 1MB, no performance impact  

- **Smart Window Detection**  
  🎮 Only affects Minecraft, preserves normal spacebar functionality in other apps  

- **Flexible Control**  
  ⚙️ Right-click system tray icon (H icon) → Pause/exit anytime  

---

## 📥 Download & Usage
### Step 1: Download
Download the latest `NoHoldJumpFix.exe` from [Releases page](https://github.com/yourusername/NoHoldJumpFix/releases).

### Step 2: Run
- **Right-click file** → **Run as Administrator**  
  ![Admin Permission](https://i.imgur.com/5qL9Z8s.png)  
  *Administrator permission required for initial run.*

### Step 3: Verify
1. Launch Minecraft and enter a world.  
2. **Short press Space** → 1 jump.  
3. **Long press Space** → No continuous jumps.  
4. **Shift+Space sprint** → Works normally.  

---

## 🖥️ Compatibility
| Edition       | Process Name          | Status |
|---------------|-----------------------|--------|
| Java Edition  | `java.exe` / `javaw.exe` | ✅ Full |
| Bedrock Edition | `Minecraft.Windows.exe` | ✅ Full |

**System Requirements**: Windows 10/11 (Administrator rights required).

---

## ⚠️ Notes
- **Multiplayer Caution**: May trigger anti-cheat systems on some servers. Verify server rules before use.  
- **Process Name Check**: If the script fails, confirm the game process name is `java.exe` in Task Manager.  
- **Close Conflicting Apps**: Exit Logitech G HUB, Razer Synapse, etc.  

---

## ⚙️ Advanced Configuration
### Customize Press Duration
Edit the `Sleep` parameter in script (requires [AutoHotkey](https://www.autohotkey.com)):
```autohotkey
$Space::
    Send {Blind}{Space Down}
    Sleep 80  ; Adjust this value (ms)
    Send {Blind}{Space Up}
    KeyWait, Space
return
