# 🚀 Quick Start Guide

## Prerequisites
- Node.js 18+
- npm or yarn
- Gemini API key (optional, for AI features)

## 1. Install Dependencies
```bash
npm install
```

## 2. Build the Project
```bash
npm run build
```

## 3. Test MCP Server
```bash
# Test if server responds
echo '{"jsonrpc": "2.0", "id": 1, "method": "tools/list"}' | node dist/index.js
```

## 4. Configure MCP Client

### For Cursor IDE
Add to your `~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "mcp-tailwind-gemini": {
      "command": "node",
      "args": ["/path/to/mcp-tailwind-gemini-clean/dist/index.js"],
      "env": {
        "GEMINI_API_KEY": "your_gemini_api_key_here"
      }
    }
  }
}
```

### For Claude Desktop
Create or edit `~/Library/Application Support/Claude/claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "mcp-tailwind-gemini": {
      "command": "node",
      "args": ["/path/to/mcp-tailwind-gemini-clean/dist/index.js"],
      "env": {
        "GEMINI_API_KEY": "your_gemini_api_key_here"
      }
    }
  }
}
```

## 5. Restart Your MCP Client

After updating the config, restart your MCP client (Claude Desktop or Cursor) to load the MCP server.

## 6. Test in Your AI Assistant

Ask your AI assistant to:
- "Generate a button component with Tailwind CSS"
- "Create a responsive card layout"
- "Optimize these Tailwind classes: p-4 px-4 py-4"

## Troubleshooting

### Server not starting?
```bash
# Check if build was successful
ls -la dist/

# Rebuild if needed
npm run build
```

### Client not connecting?
- Restart your MCP client
- Check config file syntax
- Verify the path to dist/index.js is correct

### API errors?
- Set your GEMINI_API_KEY
- Check internet connection
- Verify API key permissions

## Available Tools

- `generate_component` - Create Tailwind components
- `optimize_classes` - Clean up Tailwind classes
- `create_theme` - Generate color themes
- `analyze_design` - Get design feedback
- `generate_preview` - Create visual previews
- `convert_to_tailwind` - Convert CSS to Tailwind
- `suggest_improvements` - Get AI suggestions
- `create_layout` - Generate responsive layouts
- `get_shadcn_component` - Get shadcn/ui components
- `create_project` - Generate complete projects

## Example Usage

### Generate a Button Component
```javascript
{
  "tool": "generate_component",
  "description": "A modern primary button with hover effects",
  "type": "button",
  "variant": "primary",
  "size": "lg",
  "framework": "react",
  "responsive": true,
  "accessibility": true
}
```

### Optimize Tailwind Classes
```javascript
{
  "tool": "optimize_classes",
  "html": "<div class=\"p-4 px-4 py-4 text-blue-500 text-blue-600 bg-white bg-gray-100\">Content</div>",
  "removeRedundant": true,
  "mergeConflicts": true
}
```

### Create a Theme
```javascript
{
  "tool": "create_theme",
  "brandColor": "#3B82F6",
  "style": "modern",
  "colorCount": 9,
  "includeConfig": true
}
```

## Next Steps

1. **Explore the tools** - Try different component types and frameworks
2. **Create projects** - Generate complete project setups
3. **Optimize existing code** - Use the optimization tools on your current projects
4. **Build themes** - Create custom design systems
5. **Generate layouts** - Build responsive page layouts

---

**Happy coding with MCP Tailwind Gemini! 🎨✨** 