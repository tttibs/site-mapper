# 🗺️ Website Mapping Tool

An interactive, drag-and-drop visual sitemap designer inspired by Microsoft Power Automate. Create, organize, and visualize your website structure with an intuitive interface.

![Website Mapping Tool](https://img.shields.io/badge/version-1.0-blue) ![License](https://img.shields.io/badge/license-MIT-green)

## ✨ Features

### Core Functionality
- **🎨 Drag & Drop Interface** - Intuitive page creation and organization
- **🔗 Visual Connections** - Create relationships between pages with smart connectors
- **📐 Grid Snapping** - Automatic alignment for clean layouts
- **🔍 Zoom & Pan** - Navigate large sitemaps easily with zoom controls
- **💾 Auto-Save** - Your work is automatically saved to browser storage every 2 seconds
- **📤 Export/Import** - Save and load projects as JSON files

### Page Types
- 🏠 Home Page
- 🎯 Service Line Page
- 📊 Sub-Service Line Page
- 🏢 Property Listings
- 📄 Content Page

### Advanced Features
- **Smart Connections** - Automatically maintains horizontal/vertical connection logic
- **Auto Layout** - Intelligent reorganization of pages in hierarchical structure
- **Insert Between Pages** - Click "+" on connections to add pages mid-flow
- **Properties Panel** - Edit page details with URL path builder
- **Status Tracking** - Mark pages as "New" or "Existing"

## 🚀 Quick Start

### Option 1: Use Directly (No Installation)
1. Download `index.html`
2. Open in any modern web browser
3. Start creating your sitemap!

### Option 2: Host on GitHub Pages
1. Fork this repository
2. Go to Settings → Pages
3. Select "Deploy from main branch"
4. Access at `https://your-username.github.io/website-mapper/`

## 📖 How to Use

### Creating Pages
1. **Drag** a page type from the left sidebar onto the canvas
2. **Click** the page to open its properties
3. Edit the title, URL path, and description
4. Mark as "New" or "Existing" page

### Connecting Pages
1. **Click** a blue connection point (circle) on any page
2. **Drag** to another page's connection point
3. Release to create the connection

### Inserting Pages
1. **Click** the blue "+" button on any connection
2. **Select** a page type from the modal
3. The page is automatically inserted and layout reorganizes

### Managing Your Project

#### Auto-Save
- Your work saves automatically every 2 seconds
- Reopen the browser to continue where you left off
- Click "New Project" to start fresh

#### Export/Import
- **Download JSON**: Saves project file to your computer
- **Copy JSON**: Copies project data to clipboard (useful if downloads blocked)
- **Import JSON**: Load a previously saved project

### Keyboard & Controls
- **Click & Drag Background**: Pan the canvas
- **Zoom In/Out**: Use the +/- buttons
- **Reset View**: Return to default zoom and position
- **Auto Layout**: Reorganize all pages hierarchically

## 🎯 Use Cases

- **Website Planning** - Design site architecture before development
- **Client Presentations** - Visual sitemap for stakeholder review
- **Content Strategy** - Map content hierarchy and relationships
- **Information Architecture** - Plan navigation and user flows
- **Documentation** - Create visual documentation of existing sites

## 💻 Technical Details

### Built With
- Pure HTML5, CSS3, and Vanilla JavaScript
- No external dependencies or frameworks
- Single-file application (~1400 lines)
- Responsive design (optimized for desktop)

### Browser Support
- ✅ Chrome/Edge (Recommended)
- ✅ Firefox
- ✅ Safari
- ⚠️ Works best on desktop browsers

### Data Storage
- **LocalStorage**: Auto-save feature uses browser's localStorage
- **JSON Export**: Portable project files for sharing/backup
- **No Server Required**: Fully client-side application

## 📁 File Structure

```
website-mapper/
├── index.html          # Main application file
├── README.md           # This file
└── projects/           # (Optional) Store your saved JSON projects
    └── examples/
        └── sample-sitemap.json
```

## 🔧 Configuration

### Customize Page Types
Edit the `getNodeConfig()` function in the code:

```javascript
getNodeConfig(type) {
    const configs = {
        home: { title: 'Home', path: '', icon: '🏠', color: '#e3f2fd' },
        // Add your custom page types here
    };
}
```

### Adjust Layout Settings
Modify layout parameters in the `autoLayout()` function:

```javascript
const levelHeight = 200;      // Vertical spacing between levels
const horizontalSpacing = 250; // Horizontal spacing between nodes
```

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Feature Ideas
- [ ] Custom color themes
- [ ] Multi-level undo/redo
- [ ] Export to PNG/SVG image
- [ ] Collaborative editing
- [ ] Template library
- [ ] Custom page type creator

## 📝 JSON Format

Projects are saved in the following format:

```json
{
  "nodes": [
    {
      "id": 1,
      "type": "home",
      "x": 400,
      "y": 100,
      "title": "Home",
      "path": "",
      "icon": "🏠",
      "color": "#e3f2fd",
      "description": "",
      "status": "new"
    }
  ],
  "connections": [
    {
      "from": 1,
      "fromPoint": "bottom",
      "to": 2,
      "toPoint": "top"
    }
  ],
  "version": "1.0",
  "lastSaved": "2025-10-23T..."
}
```

## 🐛 Known Issues

- **Download Blocked**: Some browsers may block downloads. Use "Copy JSON" instead.
- **Large Sitemaps**: Performance may degrade with 100+ pages. Consider breaking into multiple projects.
- **Mobile Support**: Optimized for desktop; touch gestures limited on mobile.

## 📜 License

This project is licensed under the MIT License - see below:

```
MIT License

Copyright (c) 2025 Website Mapper

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 🙏 Acknowledgments

- Inspired by Microsoft Power Automate's flow design interface
- Built for efficient website architecture planning
- Created with ❤️ for web designers and developers

## 📞 Support

Having issues or questions?
- Check the [Known Issues](#-known-issues) section
- Open an issue on GitHub
- Review the [How to Use](#-how-to-use) guide

## 🔄 Changelog

### Version 1.0 (2025-10-23)
- Initial release
- Core drag-and-drop functionality
- Auto-save feature
- Export/Import JSON
- Auto-layout algorithm
- Insert pages between connections
- Properties panel with URL builder

---

**Made with ❤️ by [Your Name/Organization]**

⭐ Star this repo if you find it useful!
