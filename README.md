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

![CodeGraph 3D Interactive Architecture Graph](screenshot_graph.jpg)

---

## 🚀 Overview

**CodeGraph v2.0** là động cơ phân tích tĩnh kiến trúc mã nguồn thế hệ mới, được xây dựng trên nền tảng **TokenVector (.tkv)** siêu tốc. CodeGraph chuyển đổi toàn bộ mã nguồn dự án thành bản đồ đồ thị tri thức (Knowledge Graph) và bộc lộ trực tiếp tới các AI Coding Assistant thông qua chuẩn giao thức **Model Context Protocol (MCP)**.

Nhờ việc cung cấp bản đồ liên kết 100% chính xác (cuộc gọi hàm, kế thừa lớp, import module), CodeGraph triệt tiêu hoàn toàn hiện tượng AI ảo giác (Hallucination), giúp AI refactor code an toàn và chính xác tuyệt đối.

---

## ⚡ Benchmark Thực Tế & Lợi Thế Cạnh Tranh Vượt Trội

### 📊 Bảng So Sánh Benchmark Thực Tế

| Tiêu Chí Benchmark | CodeGraph v2.0 (TokenVector) | Công Cụ Vector Search / Legacy AST | Lợi Thế Vượt Trội |
| :--- | :--- | :--- | :--- |
| **Tốc độ Quét (800+ Files)** | **< 0.8 Giây** | 12 - 45 Giây | **Nhanh hơn 15x - 50x**. Không có độ trễ parsing. |
| **Độ Chính Xác Liên Kết** | **100% Deterministic** | Probabilistic (Dự đoán xác suất) | **0% Ảo giác (Zero Hallucination)**. Truy vết ngược 2 tầng. |
| **Tiêu Tốn Bộ Nhớ (RAM)** | **~ 8 MB RAM** | 500 MB - 2 GB RAM | **Siêu nhẹ**. Không cần Database ngầm (Neo4j, KuzuDB). |
| **Tối Ưu Ngân Sách Token** | **Tiết kiệm 92% Tokens** | Bơm tràn Full Repo | **Gói ngữ cảnh phẫu thuật (`get_optimal_context`)**. |
| **Bảo Mật & Offline** | **100% Local & Offline** | Đẩy code lên Cloud Vector DB | Mã nguồn không bao giờ rời khỏi máy tính cá nhân. |

---

## 🌟 5 Lợi Thế Cạnh Tranh Cốt Lõi (Core Competitive Advantages)

1. 🎯 **Đánh Giá Tác Động Dây Truyền (`analyze_impact`):** Trước khi AI sửa một hàm/lớp, CodeGraph tự động dò tìm liên kết ngược 2 tầng (Level 1 & Level 2) để cảnh báo: *"Nếu sửa hàm này, Class B ở file X và Unit Test C ở file Y sẽ bị hỏng"*.
2. 📦 **Đóng Gói Ngữ Cảnh Tối Ưu (`get_optimal_context`):** Tự động tính toán phụ thuộc xung quanh điểm chỉnh sửa và đóng gói vừa khít hạn mức Token của AI, triệt tiêu thông tin rác.
3. 🕸️ **Giao Diện HTML 3D Interactive Obsidian Graph:** Xuất tự động giao diện đồ thị 3D tương tác bằng D3.js, hiển thị cụm màu sắc cộng đồng và kích thước bậc liên kết (`degree`).
4. 🔑 **Kiến Trúc Bản Quyền Kép (Dual-Layer Licensing):** Kết hợp xác thực tự động 24/7 qua cổng Lemon Squeezy API và bộ **100 Offline Master Keys** vĩnh viễn (đến năm `2099-12-31`) cho môi trường Doanh nghiệp/Offline.
5. 🎁 **Dùng Thử 30 Ngày Tự Động (30-Day Free Trial):** Kích hoạt dùng thử 30 ngày ngay khi cài đặt mà không cần đăng ký rườm rà.

---

## 📥 Mua Bản Quyền & Tải Về

👉 **[Mua License Key Chính Thức trên Lemon Squeezy](https://codegraph.lemonsqueezy.com/checkout/buy/701442e2-6153-408a-9d39-1eb1456538a3)**

*(Mỗi License Key hỗ trợ kích hoạt đồng thời trên 2 thiết bị).*

---

## 📖 Hướng Dẫn Kích Hoạt & Sử Dụng Nhanh

1. Giải nén bộ cài **`CodeGraph2.0_Release`**.
2. Click đúp vào **`CodeGraph_v2_Launcher.bat`** để chạy quét dự án và sinh giao diện đồ thị 3D.
3. Thêm cấu hình MCP vào file `mcp_config.json` của AI Editor:
   ```json
   {
     "mcpServers": {
       "CodeGraph": {
         "command": "C:\\CodeGraph2.0_Release\\2.code\\tools\\pytok.exe",
         "args": ["C:\\CodeGraph2.0_Release\\2.code\\CodeGraph_MCP.exe"]
       }
     }
   }
   ```
4. Tham khảo tài liệu chi tiết tại **`USER_GUIDE.md`**.

---
*© 2026 CodeGraph. All rights reserved. TokenVector Engine Technology.*
