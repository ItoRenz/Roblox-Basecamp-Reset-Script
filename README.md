# 🏠 Basecamp Reset System

A comprehensive checkpoint reset system for Roblox with modern GUI and cross-platform support.

**Author:** ItoRenz00

---

## 📋 Features

### Core Functionality
- ✅ One-click reset to basecamp/spawn location
- ✅ Automatic checkpoint reset to 0
- ✅ Summit progress preservation
- ✅ Physics reset (velocity & rotation)
- ✅ Health restoration on teleport
- ✅ Server-side checkpoint validation

### User Interface
- 🎨 Modern, animated reset button
- 🖱️ Smooth hover effects and tooltips
- 📱 Full mobile touch support
- 🎯 Responsive design (PC & Mobile)
- ⚡ Pulse animations on click

### Compatibility
- 🔗 Works with StatsCore Sequential CP System
- 🏷️ Supports multiple basecamp naming conventions
- 📊 Compatible with various checkpoint stat names
- 🔄 Fallback spawn location if basecamp not found

---

## 🚀 Installation

### Requirements
- Roblox Studio
- Basic understanding of Roblox Studio hierarchy

### Setup Steps

1. **Client Script (LocalScript)**
   - Location: `StarterGui > LocalScript`
   - Copy the content from `BasecampResetClient.lua`
   - Paste into a new LocalScript in StarterGui

2. **Server Script**
   - Location: `ServerScriptService > Script`
   - Copy the content from `BasecampResetServer.lua`
   - Paste into a new Script in ServerScriptService

3. **Test the System**
   - Press Play in Roblox Studio
   - Look for the reset button (⌂) in the top-right corner
   - Click to reset to basecamp

---

## 🎮 Usage

### For Players
1. **Desktop:** Click the home icon (⌂) button in the top-right corner
2. **Mobile:** Tap the home icon (⌂) button in the top-right corner
3. **Effect:** You'll be teleported to basecamp with checkpoint reset to 0

### Button Location
- Desktop: Top-right corner (below typical UI elements)
- Mobile: Optimized position for thumb reach

---

## ⚙️ Configuration

### Basecamp Names (Auto-detected)
The system automatically searches for these names in workspace:
- `Basecamp`
- `SpawnLocation`
- `Base`
- `Spawn`

### Checkpoint Stat Names (Auto-detected)
The system recognizes these leaderstats names:
- `Checkpoint`
- `CheckPoint`
- `checkpoint`
- `CHECKPOINT`

### Summit Stat Names (Preserved)
Summit progress is never reset:
- `Summit`
- `summit`
- `SUMMIT`

### Default Spawn
If no basecamp is found, players spawn at: `Vector3.new(0, 50, 0)`

---

## 🛠️ Customization

### Button Colors
Edit `Config.Button.Colors` in the client script:
```lua
Colors = {
    Normal = Color3.fromRGB(255, 107, 107),
    Hover = Color3.fromRGB(255, 85, 85),
    Stroke = Color3.fromRGB(255, 200, 200),
    StrokeHover = Color3.fromRGB(255, 150, 150)
}
```

### Button Position
Edit `Config.Button.Position` in the client script:
```lua
Position = UDim2.new(1, -40, 0, -45)
```

### Button Size
Edit `Config.Button.Size` in the client script:
```lua
Size = isMobile and 32 or 36
```

---

## 🔧 Technical Details

### Architecture
- **Client-Server Model:** Uses RemoteEvents for secure communication
- **Client Script:** Handles UI, animations, and player teleportation
- **Server Script:** Manages checkpoint stats and validation

### Security
- ✅ Server-side checkpoint validation
- ✅ No client-side stat manipulation
- ✅ Protected against exploits

### Performance
- ⚡ Optimized TweenService animations
- 📉 Minimal performance impact
- 🔄 Efficient event handling

---

## 📊 Compatibility Matrix

| System | Compatible | Notes |
|--------|-----------|-------|
| StatsCore Sequential CP | ✅ Yes | Fully integrated |
| Custom Checkpoint Systems | ✅ Yes | Auto-detects stat names |
| Mobile Devices | ✅ Yes | Touch support included |
| PC/Desktop | ✅ Yes | Mouse support included |
| VR | ⚠️ Untested | Should work (uses standard UI) |

---

## 🐛 Troubleshooting

### Button Not Showing
- Ensure LocalScript is in `StarterGui`
- Check if `StarterGui.ResetOnSpawn` is false for persistence

### Checkpoint Not Resetting
- Verify Server Script is in `ServerScriptService`
- Check Output for error messages
- Ensure leaderstats exist with correct names

### Teleport to Wrong Location
- Add/rename basecamp part in workspace
- Check if basecamp is a BasePart or Model
- Verify basecamp position is accessible

### Player Falling Through Ground
- Increase Y offset in spawn position: `Vector3.new(0, 5, 0)` → `Vector3.new(0, 10, 0)`
- Ensure basecamp has collision enabled

---

## 📝 Changelog

### Version 1.0.0 (Initial Release)
- ✨ Modern GUI with animations
- 🔄 Checkpoint reset functionality
- 📱 Mobile support
- 🎨 Hover tooltips
- ⚡ Pulse click effects
- 🔒 Server-side validation

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

### Development Guidelines
1. Maintain code style consistency
2. Add comments for complex logic
3. Test on both PC and mobile
4. Update README for new features

---

## 📄 License

This project is open source and available for use in any Roblox game.

**Author:** ItoRenz00

---

## 💬 Support

For issues, questions, or suggestions:
- Open an issue on GitHub
- Contact the author: ItoRenz00

---

## 🌟 Credits

**Created by:** ItoRenz00

**Special Thanks:**
- Roblox Developer Community
- StatsCore System Users

---

## 📸 Screenshots

*(Add screenshots of your GUI in action here)*

---

**Made with ❤️ for the Roblox Community**
