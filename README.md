# 🎨 MCP Tailwind Gemini

Advanced Model Context Protocol (MCP) server for Tailwind CSS with Gemini AI integration and cross-platform support for intelligent design assistance.

[![GitHub](https://img.shields.io/badge/GitHub-Repository-blue?style=flat-square&logo=github)](https://github.com/Tai-DT/mcp-tailwind-gemini)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)](LICENSE)
[![Node.js](https://img.shields.io/badge/Node.js-18+-green?style=flat-square&logo=node.js)](https://nodejs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0+-blue?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-CSS-38B2AC?style=flat-square&logo=tailwind-css)](https://tailwindcss.com/)

## 🌟 Features

### 🤖 AI-Powered Design
- **Intelligent Component Generation**: Create sophisticated Tailwind components using Gemini AI
- **Smart Optimization**: AI-driven class optimization and conflict resolution
- **Design Analysis**: Comprehensive design quality assessment with improvement suggestions
- **Theme Creation**: Generate cohesive design systems with AI assistance

### 🎨 Tailwind CSS Tools
- **Component Generator**: Create buttons, cards, forms, navigation, modals, and custom components
- **Class Optimizer**: Clean up redundant classes and resolve conflicts
- **CSS Converter**: Transform existing CSS/SCSS to Tailwind classes
- **Layout Generator**: Build responsive layouts for dashboards, landing pages, blogs, and more
- **Theme Creator**: Generate custom color palettes, typography, and design tokens
- **Preview Generator**: Visual component previews with screenshot capability

### 🌐 Cross-Platform Integration
- **Multi-Framework Support**: React, Vue, Svelte, Angular with automatic component conversion
- **Build Tool Integration**: Vite, Webpack, Next.js, Nuxt, SvelteKit project generation
- **IDE Extensions**: VS Code, WebStorm plugins with live assistance
- **Design Tool Sync**: Figma plugin for design-to-code conversion
- **Universal Deployment**: CLI tools, browser extensions, and API integrations

## 📦 Installation

### Prerequisites
- Node.js 18 or higher
- npm or yarn package manager
- Gemini API key for AI features

### Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Tai-DT/mcp-tailwind-gemini.git
   cd mcp-tailwind-gemini
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Build the project:**
   ```bash
   npm run build
   ```

4. **Set up Gemini AI (optional):**
   ```bash
   export GEMINI_API_KEY="your-api-key-here"
   ```

## 🔧 MCP Configuration

### For Cursor IDE

Add to your `~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "mcp-tailwind-gemini": {
      "command": "node",
      "args": ["/path/to/mcp-tailwind-gemini/dist/index.js"],
      "env": {
        "GEMINI_API_KEY": "your_gemini_api_key_here"
      }
    }
  }
}
```

### For Claude Desktop

Add to your `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "mcp-tailwind-gemini": {
      "command": "node",
      "args": ["/path/to/mcp-tailwind-gemini/dist/index.js"],
      "env": {
        "GEMINI_API_KEY": "your_gemini_api_key_here"
      }
    }
  }
}
```

**Config File Locations:**
- **macOS**: `~/Library/Application Support/Claude/claude_desktop_config.json`
- **Windows**: `%APPDATA%\\Claude\\claude_desktop_config.json`
- **Linux**: `~/.config/Claude/claude_desktop_config.json`

### Alternative Configuration (using npm)

```json
{
  "mcpServers": {
    "mcp-tailwind-gemini": {
      "command": "npm",
      "args": ["run", "start"],
      "cwd": "/path/to/mcp-tailwind-gemini",
      "env": {
        "GEMINI_API_KEY": "your_gemini_api_key_here"
      }
    }
  }
}
```

## 🛠️ Available Tools

### Component Generation
```javascript
{
  "tool": "generate_component",
  "description": "Create a responsive button component",
  "type": "button",
  "variant": "primary",
  "size": "lg",
  "framework": "react",
  "responsive": true,
  "accessibility": true
}
```

### Class Optimization
```javascript
{
  "tool": "optimize_classes", 
  "html": "<div class=\"p-4 px-4 py-4 text-blue-500 text-blue-600\">Content</div>",
  "removeRedundant": true,
  "mergeConflicts": true
}
```

### Theme Creation
```javascript
{
  "tool": "create_theme",
  "brandColor": "#3B82F6",
  "style": "modern",
  "colorCount": 9,
  "includeConfig": true
}
```

### Design Analysis
```javascript
{
  "tool": "analyze_design",
  "html": "<div>...</div>",
  "checkAccessibility": true,
  "checkResponsive": true,
  "checkPerformance": true
}
```

### Preview Generation
```javascript
{
  "tool": "generate_preview",
  "html": "<button class=\"bg-blue-500 text-white px-4 py-2 rounded\">Button</button>",
  "width": 800,
  "height": 600
}
```

### CSS Conversion
```javascript
{
  "tool": "convert_to_tailwind",
  "code": ".button { padding: 1rem; background: #3B82F6; }",
  "format": "css",
  "optimize": true
}
```

### AI Suggestions
```javascript
{
  "tool": "suggest_improvements",
  "html": "<div>...</div>",
  "context": "E-commerce product card",
  "focusAreas": ["accessibility", "performance", "ux"]
}
```

### Layout Generation
```javascript
{
  "tool": "create_layout",
  "type": "dashboard",
  "sections": ["header", "sidebar", "main", "footer"],
  "complexity": "medium",
  "framework": "react"
}
```

### Shadcn/ui Components
```javascript
{
  "tool": "get_shadcn_component",
  "componentName": "button",
  "includeDemo": true,
  "framework": "react"
}
```

### Project Generation
```javascript
{
  "tool": "create_project",
  "projectName": "My App",
  "framework": "react",
  "typescript": true,
  "components": ["button", "card", "form"],
  "template": "dashboard"
}
```

## 🎯 Use Cases

### Creating Components
Generate production-ready components with AI assistance:
- Modern button variants with accessibility features
- Responsive card layouts with proper spacing
- Form components with validation styling
- Navigation menus with mobile-first design

### Design Optimization
Improve existing designs with intelligent analysis:
- Remove redundant Tailwind classes
- Resolve conflicting utility classes
- Optimize for performance and maintainability
- Enhance accessibility compliance

### Theme Development
Build comprehensive design systems:
- Generate cohesive color palettes
- Create typography scales
- Design spacing systems
- Export Tailwind configuration files

## 🌐 Cross-Platform Usage

### Multi-Framework Development
```javascript
// Convert HTML component to any framework
{
  "tool": "generate_component",
  "description": "Modern button component",
  "framework": "react", // or "vue", "svelte", "angular"
  "typescript": true,
  "features": ["loading-state", "variant-support"]
}
```

### Universal Project Generation  
```javascript
// Create full-stack project with any tech stack
{
  "tool": "create_project",
  "name": "My App",
  "framework": "react",
  "buildTool": "vite", // or "webpack", "nextjs", "nuxt"
  "features": ["typescript", "tailwind", "testing", "deployment"]
}
```

## 🔧 Development

### Running Locally
```bash
# Development mode with hot reload
npm run dev

# Build for production
npm run build

# Start production server
npm start
```

### Testing MCP Server

1. **Test with echo command:**
```bash
echo '{"jsonrpc": "2.0", "id": 1, "method": "tools/list"}' | node dist/index.js
```

2. **Test with a simple tool call:**
```bash
echo '{"jsonrpc": "2.0", "id": 1, "method": "tools/call", "params": {"name": "generate_component", "arguments": {"description": "A simple button", "type": "button"}}}' | node dist/index.js
```

3. **Test with environment variable:**
```bash
GEMINI_API_KEY="your_key" node dist/index.js
```

### Environment Variables
- `GEMINI_API_KEY`: Your Google Gemini API key (optional)
- `NODE_ENV`: Environment mode (development/production)

### Project Structure
```
src/
├── index.ts              # Main MCP server
├── tools/                # MCP tool implementations
│   ├── component-generator.ts
│   ├── class-optimizer.ts
│   ├── theme-creator.ts
│   ├── design-analyzer.ts
│   ├── preview-generator.ts
│   ├── css-converter.ts
│   ├── ai-suggestions.ts
│   └── layout-generator.ts
└── utils/
    └── gemini.ts          # Gemini AI integration
```

## 🔧 Troubleshooting

### Common Issues

1. **MCP Server not starting:**
   - Ensure you've run `npm run build` first
   - Check that `dist/index.js` exists
   - Verify Node.js version is 18+

2. **Gemini API errors:**
   - Set your `GEMINI_API_KEY` environment variable
   - Verify the API key is valid and has proper permissions
   - Check your internet connection

3. **Claude Desktop not connecting:**
   - Restart Claude Desktop after updating config
   - Check the config file path is correct
   - Verify JSON syntax is valid

4. **Build errors:**
   ```bash
   # Clean and rebuild
   rm -rf dist/ node_modules/
   npm install
   npm run build
   ```

### Debug Mode
```bash
# Run with debug logging
DEBUG=mcp:* node dist/index.js
```

## 🤝 Contributing

We welcome contributions! Please see our contributing guidelines for details.

### Development Setup
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

MIT License - see LICENSE file for details.

## 🙋‍♂️ Support

- **Issues**: [GitHub Issues](https://github.com/Tai-DT/mcp-tailwind-gemini/issues)
- **Documentation**: Check the examples in this README
- **Discussions**: [GitHub Discussions](https://github.com/Tai-DT/mcp-tailwind-gemini/discussions)

---

Built with ❤️ for the Tailwind CSS and AI community 