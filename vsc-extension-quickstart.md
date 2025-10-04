# 🚀 Quantum Material Theme - Development Guide

Welcome to the Quantum Material Theme development environment! This guide will help you get started with developing, testing, and contributing to this beautiful VS Code theme.

## 📁 Project Structure

```
quantum-material-theme/
├── 📄 package.json                                    # Extension manifest
├── 📁 themes/
│   └── 📄 quantum-material-theme-ocean.json          # Theme definition
├── 📄 README.md                                       # Project documentation
├── 📄 CHANGELOG.md                                    # Version history
└── 📄 vsc-extension-quickstart.md                    # This guide
```

### Key Files Explained

| File | Description |
|------|-------------|
| `package.json` | Extension manifest with theme contribution point |
| `themes/quantum-material-theme-ocean.json` | Complete theme definition with all color mappings |
| `vsc-extension-quickstart.md` | This guide for getting started |

## 🛠️ Development Setup

### Prerequisites
- **VS Code** version 1.104.0 or higher
- **Node.js** (optional, for package management)
- **Git** for version control

### Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/michaelmendez/quantum-material-theme.git
   cd quantum-material-theme
   ```

2. **Open in VS Code**
   ```bash
   code .
   ```

3. **Launch Development Environment**
   - Press `F5` or `Ctrl+F5` to open Extension Development Host
   - A new VS Code window will open with your theme loaded

4. **Activate the Theme**
   - In the Extension Development Host window:
   - Open Command Palette (`Ctrl+Shift+P`)
   - Type `Preferences: Color Theme`
   - Select `Quantum Material Theme`

## 🎨 Theme Development

### Testing Your Changes

1. **Real-time Preview**
   - Changes to the theme file are automatically applied
   - No need to reload the Extension Development Host
   - Switch between themes to see differences

2. **Test with Different File Types**
   ```
   📁 test-files/
   ├── 📄 example.js        # JavaScript
   ├── 📄 example.py        # Python
   ├── 📄 example.html      # HTML
   ├── 📄 example.css       # CSS
   ├── 📄 example.json      # JSON
   └── 📄 example.md        # Markdown
   ```

3. **Inspect Token Scopes**
   - Place cursor on any code element
   - Open Command Palette (`Ctrl+Shift+P`)
   - Run `Developer: Inspect Editor Tokens and Scopes`
   - Use this to understand which scopes need styling

### Color Customization Workflow

1. **Identify the Element**
   - Use the token inspector to find the scope
   - Check existing color mappings in the theme file

2. **Update Theme File**
   ```json
   {
     "name": "Quantum Material Theme",
     "tokenColors": [
       {
         "name": "Comments",
         "scope": ["comment"],
         "settings": {
           "foreground": "#666666",
           "fontStyle": "italic"
         }
       }
     ]
   }
   ```

3. **Test Thoroughly**
   - Check multiple file types
   - Verify readability and contrast
   - Test in different lighting conditions

## 🧪 Testing Checklist

Before submitting changes, ensure:

- [ ] **Syntax Highlighting** works for major languages (JS, Python, HTML, CSS, JSON, Markdown)
- [ ] **UI Colors** are consistent across all VS Code panels
- [ ] **Contrast Ratios** meet accessibility standards
- [ ] **No Color Conflicts** between different code elements
- [ ] **Theme Works** in both light and dark system themes
- [ ] **Extensions Compatibility** (test with popular extensions)

## 📦 Installation Methods

### Method 1: Development Installation
```bash
# Copy to VS Code extensions folder
cp -r . ~/.vscode/extensions/quantum-material-theme-dev
```

### Method 2: Package as VSIX
```bash
# Install vsce (VS Code Extension manager)
npm install -g vsce

# Package the extension
vsce package

# Install locally
code --install-extension quantum-material-theme-*.vsix
```

## 🚀 Publishing Workflow

### Prerequisites for Publishing
1. **Microsoft Publisher Account** on [VS Code Marketplace](https://marketplace.visualstudio.com/)
2. **Personal Access Token** from Azure DevOps
3. **vsce CLI tool** installed globally

### Publishing Steps
```bash
# Login to publisher account
vsce login <publisher-name>

# Publish new version
vsce publish patch  # or minor/major
```

### Version Management
- **Patch** (0.0.1 → 0.0.2): Bug fixes, minor color adjustments
- **Minor** (0.0.1 → 0.1.0): New features, significant improvements
- **Major** (0.0.1 → 1.0.0): Breaking changes, complete redesigns

## 🐛 Debugging Tips

### Common Issues

1. **Theme Not Loading**
   - Check `package.json` syntax
   - Verify theme file path is correct
   - Restart Extension Development Host (`Ctrl+R`)

2. **Colors Not Applying**
   - Validate JSON syntax in theme file
   - Check scope names match VS Code's token system
   - Use token inspector to debug

3. **Performance Issues**
   - Minimize complex scope patterns
   - Remove unused color definitions
   - Test with large files

### Debug Commands
```bash
# Check extension logs
code --log-level=debug

# Validate package.json
npm run validate

# Format theme file
npm run format
```

## 📚 Resources

### Official Documentation
- [VS Code Theme Guide](https://code.visualstudio.com/api/extension-guides/color-theme)
- [Theme Color Reference](https://code.visualstudio.com/api/references/theme-color)
- [Publishing Extensions](https://code.visualstudio.com/api/working-with-extensions/publishing-extension)

### Tools & Utilities
- [Theme Studio](https://themes.vscode.one/) - Online theme editor
- [Color Picker](https://coolors.co/) - Color palette generator
- [Contrast Checker](https://webaim.org/resources/contrastchecker/) - Accessibility testing

### Community
- [VS Code Theme Development Discord](https://discord.gg/vscode)
- [GitHub Discussions](https://github.com/michaelmendez/quantum-material-theme/discussions)

## 🤝 Contributing

We welcome contributions! Please:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes and test thoroughly
4. Commit with descriptive messages (`git commit -m 'Add amazing feature'`)
5. Push to your branch (`git push origin feature/amazing-feature`)
6. Open a Pull Request

---

**Happy Theme Development!** 🎨✨

Need help? [Open an issue](https://github.com/michaelmendez/quantum-material-theme/issues) or start a [discussion](https://github.com/michaelmendez/quantum-material-theme/discussions).
