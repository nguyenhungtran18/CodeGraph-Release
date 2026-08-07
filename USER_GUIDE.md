# CodeGraph User Guide

Welcome to CodeGraph! CodeGraph is a blazing-fast, C++ powered static analysis engine that maps out your entire codebase and feeds this architectural knowledge directly into your favorite AI Editors (Cursor, Claude, Windsurf, etc.) via the Model Context Protocol (MCP).

This guide will walk you through how to use CodeGraph to supercharge your AI coding assistant.

---

## 1. Initial Setup & Licensing

### Unzipping the Application
Extract the downloaded `CodeGraph_v1.0.0_Secure.zip` to a safe location on your computer (e.g., `C:\CodeGraph`). 

### Activating the License
Before scanning any projects, you need to activate your license or start your free 30-day trial.

1. Double-click the **`Codegraph.exe`** file.
2. A terminal window will open.
3. **If you have a License Key:** Paste your key when prompted and press Enter.
4. **To start the 30-day Free Trial:** Simply press **Enter** without typing anything to bypass the prompt and start your trial.

*(Note: Your license state is securely saved to your system's `%APPDATA%` folder. You will not need to enter it again).*

---

## 2. Scanning a Project (Generating the Graph)

Before your AI can understand your project, CodeGraph needs to scan it.

1. Double-click **`Codegraph.exe`** to launch the interactive prompt.
2. **Project Name:** Enter a unique name for your project (e.g., `MyApp`).
3. **Project Path:** Enter the absolute path to your project folder (e.g., `C:\Work\MyApp`).
4. CodeGraph's C++ engine will execute a 5-step pipeline:
   - Scanning Python files
   - Generating Import & Type inference graphs
   - Analyzing Node Metadata
   - Running the Architectural Reviewer
   - Creating a Version Fingerprint
5. Once complete, a `graph/` folder is generated inside your project, and a local HTML visualization map is created for you to view in your browser.

> [!TIP]
> **When to rescan?** You should re-run `Codegraph.exe` whenever you make massive structural changes to your project (like renaming core files, restructuring folders, or adding many new modules). For small daily coding edits, you do not need to rescan immediately.

---

## 3. Integrating with AI Editors (MCP Server)

To let your AI interact with the generated graph, you must configure your AI editor to run **`CodeGraph-MCP.exe`** as a background server.

> [!TIP]
> **Quick Auto-Config:** You can double-click **`CodeGraph-MCP.exe`** at any time. It will open a console displaying the exact copy-paste configuration paths tailored for your machine!

### For Cursor / Windsurf / Roo Code / Cline
1. Open your editor's **Settings**.
2. Navigate to **Features** > **MCP Servers** > Click **Add New**.
3. Fill in the fields:
   - **Name:** `CodeGraph`
   - **Type:** `command`
   - **Command:** `C:\Path\To\Your\CodeGraph-MCP.exe` *(Use the actual path on your PC)*
4. Click **Save**.

### For Claude Desktop
1. Open your configuration file at: `%APPDATA%\Claude\claude_desktop_config.json`
2. Add the following to the `mcpServers` block:
```json
"mcpServers": {
  "CodeGraph": {
    "command": "C:\\Path\\To\\Your\\CodeGraph-MCP.exe"
  }
}
```
3. Restart Claude Desktop.

---

## 4. How to Use CodeGraph with your AI

Once configured, your AI Editor will automatically detect CodeGraph's tools. You do not need to memorize commands—just talk to your AI naturally! 

Here are some examples of what you can ask your AI:

### View Available Projects
> *"What projects are currently registered in CodeGraph?"*
> 
> The AI will use the `list_projects` tool to check which projects have been scanned.

### Get Optimal Context (Avoiding Token Bloat)
> *"I want to refactor `auth_manager.py` in the `MyApp` project. Get the optimal context for this file."*
> 
> The AI will use the `get_optimal_context` tool. Instead of reading your entire repo, CodeGraph will inject a surgical payload of only the classes, functions, and imports that directly interact with `auth_manager.py`.

### Analyze Architectural Impact
> *"If I change the return type of `validate_token()` in `auth_manager.py`, what other files in the project will break?"*
>
> The AI will use the `analyze_impact` tool. CodeGraph will trace the call edges and import edges to provide a list of all upstream dependencies, ensuring the AI fixes all related files.

---

## 5. Troubleshooting

- **AI says "Graph is Stale":** This means your codebase has changed significantly since your last scan. Close your editor, double-click `Codegraph.exe`, and scan the project again.
- **AI says "License Expired":** Your 30-day trial has ended. The MCP server will automatically shut down to prevent hanging your AI. To fix this, buy a key at https://codegraph.lemonsqueezy.com, double-click `Codegraph.exe` (or `CodeGraph-MCP.exe`), and paste your key.
- **Cannot find ctxpack.exe / impact.exe:** Ensure you extracted the *entire* ZIP file, not just the `.exe` files. The `tools/` folder must remain in the same directory as the executables.

---
*CodeGraph - Empowering AI with Deterministic Architectural Context.*
