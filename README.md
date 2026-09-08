<p>
    <strong>English</strong> | <a href="README.vi.md">Tiếng Việt</a>
  </p>
<div align="center">
  <h1>CodeGraph v2.0 (TokenVector Architecture)</h1>
  <p><em>The Ultimate Deterministic Architecture & Context Engine for AI Assistants (Cursor, Antigravity, Windsurf, Claude Desktop, VSCode)</em></p>
  
  [![Version](https://img.shields.io/badge/version-v2.0.0-blue.svg)](https://codegraph.lemonsqueezy.com/checkout/buy/701442e2-6153-408a-9d39-1eb1456538a3)
  [![Platform](https://img.shields.io/badge/platform-Windows-lightgrey.svg)]()
  [![Engine](https://img.shields.io/badge/engine-TokenVector-orange.svg)]()
  [![License](https://img.shields.io/badge/license-Commercial-success.svg)](https://codegraph.lemonsqueezy.com/checkout/buy/701442e2-6153-408a-9d39-1eb1456538a3)
</div>

---

## 🖼️ Preview: 3D Interactive Obsidian-Style Graph Visualizer

<img width="1311" height="673" alt="screenshot_graph" src="https://github.com/user-attachments/assets/2e441070-c61d-48f7-85c8-062962ba5857" />

---

## 🚀 Overview

**CodeGraph v2.0** is a next-generation static codebase architecture engine powered by the ultra-fast **TokenVector (.tkv)** runtime. CodeGraph transforms your entire repository into a deterministic Knowledge Graph and exposes it directly to AI Coding Assistants via the **Model Context Protocol (MCP)** standard.

By providing 100% deterministic structural links (function calls, class inheritance, module imports), CodeGraph completely eliminates AI hallucinations, enabling confident and precise codebase refactoring.

---

## ⚡ Real-World Benchmarks & Competitive Edge

### 📊 Benchmark Comparison

| Metric | CodeGraph v2.0 (TokenVector) | Vector Search / Legacy AST Tools | Key Advantage |
| :--- | :--- | :--- | :--- |
| **Scan Speed (800+ Files)** | **< 0.8 Seconds** | 12 - 45 Seconds | **15x - 50x Faster**. Zero parsing overhead. |
| **Link Accuracy** | **100% Deterministic** | Probabilistic | **0% Hallucination**. 2-level reverse dependency tracing. |
| **Memory Footprint (RAM)** | **~ 8 MB RAM** | 500 MB - 2 GB RAM | **Ultra-lightweight**. No embedded graph DB required (Neo4j, KùzuDB). |
| **Token Optimization** | **Saves 92% Tokens** | Full repo dumping | **Surgical context packaging (`get_optimal_context`)**. |
| **Security & Privacy** | **100% Local & Offline** | Uploads code to Cloud Vector DB | Source code never leaves your local machine. |

---

## 🌟 5 Core Competitive Advantages

1. 🎯 **Cascading Impact Analysis (`analyze_impact`):** Before an AI modifies a function or class, CodeGraph traverses 2 levels of reverse dependencies (Level 1 & Level 2) to warn: *"Modifying this function will break Class B in file X and Unit Test C in file Y"*.
2. 📦 **Optimal Context Packaging (`get_optimal_context`):** Automatically computes structural dependencies around target edits and packages them precisely within the AI's token limit, eliminating irrelevant noise.
3. 🕸️ **Interactive 3D Obsidian-Style Graph:** Automatically exports an interactive 3D graph visualizer built with D3.js, featuring community color clustering and node degree sizing.
4. 🔑 **Dual-Layer Licensing:** Combines seamless 24/7 activation via the Lemon Squeezy API with a fallback set of **100 permanent Offline Master Keys** (valid through `2099-12-31`) for enterprise and offline air-gapped environments.
5. 🎁 **Zero-Friction 30-Day Free Trial:** Instant 30-day trial automatically activated upon installation—no sign-up or credit card required.

---

## 📥 Licensing & Downloads
👉 **[Download Release](https://github.com/nguyenhungtran18/CodeGraph-Release/releases/download/v2.0.0/CodeGraph2.0_Release.zip)**

👉 **[Purchase Official License Key on Lemon Squeezy](https://codegraph.lemonsqueezy.com/checkout/buy/701442e2-6153-408a-9d39-1eb1456538a3)**

*(Each license key supports simultaneous activation on up to 2 devices).*

---

## 📖 Quick Start & Activation Guide

1. Extract the **`CodeGraph2.0_Release`** archive.
2. Double-click **`CodeGraph_v2_Launcher.bat`** to analyze the repository and generate the 3D graph view.
3. Register the MCP server in your AI Editor's `mcp_config.json`:
   ```json
   {
     "mcpServers": {
       "CodeGraph": {
         "command": "C:\\CodeGraph2.0_Release\\2.code\\tools\\pytok.exe",
         "args": ["C:\\CodeGraph2.0_Release\\2.code\\CodeGraph_MCP.exe"]
       }
     }
   }
For comprehensive usage instructions, refer to USER_GUIDE.md.

---

© 2026 CodeGraph. All rights reserved. TokenVector Engine Technology.
