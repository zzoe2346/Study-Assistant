# Obsidian Study Assistant MCP Server
AI-powered MCP server for Obsidian that helps you manage, analyze, and optimize your study notes.

## Features
- 📖 Read and analyze vault contents
- 🏷️ Tag-based note filtering
- 📅 Date-based organization using frontmatter
- 📊 Automatic study summaries
- 🎯 Next study recommendations
- ✍️ Auto-generated review notes

## Built with
- Spring AI MCP
- Java 21+
- Claude Desktop

## Architecture
### Caching Strategy
This MCP server implements an intelligent caching system to ensure optimal performance when working with large Obsidian vaults.
#### Initial Loading
- On startup, the server performs a one-time scan of your entire vault
- All markdown files are parsed and indexed in memory
- Typical loading times:
  - Small vault (< 100 notes): ~1 second
  - Medium vault (100-1000 notes): 2-5 seconds
  - Large vault (1000+ notes): 5-15 seconds
