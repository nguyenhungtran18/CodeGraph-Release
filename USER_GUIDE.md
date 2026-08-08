# Hướng Dẫn Sử Dụng CodeGraph v2.0.0 (TokenVector Architecture)

Chào mừng bạn đến với **CodeGraph v2.0.0**! CodeGraph là động cơ phân tích tĩnh cấu trúc mã nguồn siêu tốc được xây dựng trên nền tảng **TokenVector (.tkv)**. Hệ thống quét toàn bộ kiến trúc dự án và cung cấp tri thức liên kết hàm/lớp thời gian thực cho các AI Editor (Cursor, Antigravity, Windsurf, Claude Desktop, VSCode) thông qua giao thức **Model Context Protocol (MCP)**.

---

## 1. Cấu Trúc Gói Đóng Gói Phát Hành (`CodeGraph2.0_Release`)

Bản phát hành v2.0.0 được đóng gói độc lập chuẩn hóa nhị phân (Binary-Only Release):

- 🚀 **`CodeGraph_v2_Launcher.bat`**: Tập lệnh 1-Click khởi chạy quét mã nguồn trên Windows.
- 📝 **`README.md` & `USER_GUIDE.md`**: Tài liệu hướng dẫn cài đặt và vận hành hệ thống.
- ⚙️ **`.env.example`**: File cấu hình biến môi trường mẫu.
- 🌐 **`1.UI/GraphView/`**:
  - `graph_visualization.html`: Giao diện trực quan hóa đồ thị 3D tương tác D3.js.
  - `codegraph_data.js`: Tập tin dữ liệu chứa toàn bộ các Nút (Nodes) và Cạnh (Edges) liên kết.
- 💻 **`2.code/`**:
  - `codegraph_v2.exe`: Động cơ điều phối quét đồ thị tĩnh chính (Orchestrator).
  - `CodeGraph_MCP.exe`: Server MCP kết nối thời gian thực với AI Editor.
  - `master_key_manager.exe`: Trình quản lý Master Keys offline.
  - `tools/`: Bộ 11 công cụ nhị phân phân tích tĩnh (`pytok.exe`, `impgraph.exe`, `typegraph.exe`, `layers.exe`, `nodemeta.exe`, `defmeta.exe`, `graphreview.exe`, `graphstale.exe`, `ctxpack.exe`, `impact.exe`, `visualize_graph.exe`).
  - `extensions/`: Bộ công cụ mở rộng nhị phân (`dynamic_call_scanner.exe`, `treesitter_parser.exe`, `test_read.exe`).

---

## 2. Bản Quyền & Chế Độ Dùng Thử 30 Ngày (30-Day Free Trial)

CodeGraph v2.0 hỗ trợ đầy đủ 3 chế độ bản quyền linh hoạt:

1. **Chế Độ Dùng Thử 30 Ngày Miễn Phí (30-Day Free Trial):**
   - Khi chạy ứng dụng lần đầu tiên mà chưa có License Key, hệ thống **tự động kích hoạt 30 ngày dùng thử miễn phí (`CG-FREE-TRIAL-30DAYS`)**.
   - Dữ liệu dùng thử được lưu bảo mật tại `%APPDATA%\CodeGraph\license_state.json`.
2. **Khóa Thương Mại Mua Trực Tuyến:** Tự động kích hoạt trực tuyến qua cổng Lemon Squeezy API khi mua hàng tại:
   👉 **https://codegraph.lemonsqueezy.com/checkout/buy/701442e2-6153-408a-9d39-1eb1456538a3**
3. **Kích Hoạt Offline Master Keys:**
   - Nếu có Marter Key hãy Nhập mã Master Key (Ví dụ: `CG-MASTER-KEY-001-***`).
   - Sử dụng công cụ `2.code/master_key_manager.exe`
   - Master Key cho phép sử dụng vĩnh viễn không phụ thuộc Internet (Hạn sử dụng: `2099-12-31`).

---

## 3. Quét Dự Án & Trực Quan Hóa Đồ Thị 3D

Để tạo hoặc cập nhật bản đồ đồ thị cho dự án:

1. Click đúp vào file **`CodeGraph_v2_Launcher.bat`**.
2. Hệ thống TokenVector Engine tự động thực thi quy trình 5 bước:
   - Quét danh mục tập tin mã nguồn.
   - Sinh đồ thị liên kết `import` và cuộc gọi hàm/lớp (`calls`).
   - Phân tích siêu dữ liệu (Metadata) & cấu trúc tầng kiến trúc.
   - Kiểm duyệt toàn vẹn đồ thị (Architectural Reviewer).
   - Đóng gói giao diện HTML 3D tại **`1.UI/GraphView/graph_visualization.html`**.
3. Mở file `1.UI/GraphView/graph_visualization.html` bằng trình duyệt web để xem trực tiếp sơ đồ vật lý tương tác 3D.

---

## 4. Tích Hợp MCP Server Vào AI Editor

Để AI Assistant (Cursor, Antigravity, Windsurf, Claude Desktop) đọc được dữ liệu đồ thị:

### Cấu hình `mcp_config.json` (Google Antigravity / VSCode / Cursor / Windsurf):
```json
{
  "mcpServers": {
    "CodeGraph": {
      "command": "C:\\CodeGraph2.0_Release\\2.code\\tools\\pytok.exe",
      "args": [
        "C:\\CodeGraph2.0_Release\\2.code\\CodeGraph_MCP.exe"
      ]
    }
  }
}
```

### Cấu hình Claude Desktop (`%APPDATA%\Claude\claude_desktop_config.json`):
```json
{
  "mcpServers": {
    "CodeGraph": {
      "command": "C:\\CodeGraph2.0_Release\\2.code\\tools\\pytok.exe",
      "args": [
        "C:\\CodeGraph2.0_Release\\2.code\\CodeGraph_MCP.exe"
      ]
    }
  }
}
```

---

## 5. Các Công Cụ MCP Phục Vụ Lập Trình Viên & AI

Sau khi cắm MCP Server, AI Editor sẽ tự động sử dụng các tool sau:

1. **`list_projects`**: Liệt kê danh sách các dự án đã được CodeGraph quét.
2. **`get_optimal_context`**: Trích xuất ngữ cảnh tối ưu theo hạn mức Token, giúp AI chỉ đọc đúng các hàm/lớp liên quan mà không lãng phí token.
3. **`analyze_impact`**: Phân tích rủi ro tác động ngược dây chuyền. Cảnh báo danh sách các file và unit test bị ảnh hưởng ở Level 1 & Level 2 trước khi sửa mã nguồn.

---
© 2026 CodeGraph Team. All Rights Reserved. TokenVector Engine Technology.
