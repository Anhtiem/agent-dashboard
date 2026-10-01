# 🤖 Dashboard Agent - Hướng Dẫn Sử Dụng

## ✨ Dashboard này dành cho bạn nếu:
- 🎯 Bạn muốn tổ chức công việc thành các bước
- 🤖 Mỗi bước được một Agent độc lập đảm nhận
- 👁️ Bạn muốn xem toàn bộ quy trình trên một trang
- 📱 Bạn không phải kỹ sư IT - giao diện dễ sử dụng
- 🚀 Sau này chạy trên Claude Pro để tự động hóa

---

## 🚀 Cách Sử Dụng

### 1️⃣ Mở Dashboard
```
Mở file index.html bằng trình duyệt web (Chrome, Firefox, Safari, Edge)
```

### 2️⃣ Thêm Agent Mới
```
Nhấn nút "+ Thêm Agent Mới" 
→ Một thẻ mới sẽ xuất hiện
```

### 3️⃣ Điền Thông Tin Agent
Mỗi Agent có 5 phần bạn cần điền:

| Phần | Ý Nghĩa | Ví Dụ |
|------|---------|-------|
| **📝 Tên Agent** | Tên công việc mà Agent đảm nhận | "Phân tích Yêu Cầu" |
| **📝 Mô Tả** | Giải thích Agent này làm cái gì | "Thu thập và phân tích yêu cầu chi tiết từ người dùng" |
| **📥 Đầu Vào (Input)** | Agent nhận cái gì | "Yêu cầu từ người dùng (text, file)" |
| **⚙️ Quy Trình (Process)** | Agent làm thế nào | "1. Đọc yêu cầu 2. Tìm tài liệu liên quan 3. Tạo báo cáo" |
| **📤 Đầu Ra (Output)** | Agent tạo ra cái gì | "Báo cáo phân tích chi tiết, danh sách tài liệu" |

### 4️⃣ Cập Nhật Trạng Thái
Mỗi Agent có 3 trạng thái:
- ⏳ **Chưa Làm** - Chưa bắt đầu
- ⏸️ **Đang Làm** - Đang xử lý
- ✅ **Hoàn Thành** - Đã xong

### 5️⃣ Xóa Agent
- Nhấn nút **🗑️ Xóa** nếu không cần Agent nào đó

---

## 📊 Những Gì Bạn Thấy Trên Dashboard

### Phần Tổng Quan (Summary)
```
📊 Tổng Quan
├─ Tổng Agent: Số lượng Agent trong quy trình
├─ Hoàn Thành: Số Agent đã xong
├─ Đang Làm: Số Agent đang xử lý
└─ Chưa Làm: Số Agent chưa bắt đầu
```

### Sơ Đồ Quy Trình (Workflow)
```
Agent 1 → Agent 2 → Agent 3 → Agent 4
```
- Mỗi hộp là một Agent
- Màu xanh = Hoàn thành
- Màu tím = Đang làm
- Màu trắng = Chưa làm

### Danh Sách Chi Tiết (Cards)
- Mỗi Agent là một thẻ với tất cả thông tin
- Bạn có thể sửa bất cứ lúc nào

---

## 💾 Dữ Liệu Được Lưu Ở Đâu?

**Dữ liệu của bạn được lưu trong trình duyệt** (Local Storage)
- ✅ Không cần internet
- ✅ Dữ liệu lưu lại khi tắt/mở lại
- ❌ Nếu xóa cache trình duyệt sẽ mất dữ liệu

### Sao Lưu Dữ Liệu
1. Mở Console (nhấn F12)
2. Gõ: `copy(JSON.stringify(JSON.parse(localStorage.getItem('agents')), null, 2))`
3. Paste vào file txt để lưu

---

## 🎯 Ví Dụ: Quy Trình Viết Blog

```
Agent 1: Thu thập ý tưởng
├─ Input: Chủ đề blog
├─ Process: Tìm kiếm, sưu tầm ý tưởng
└─ Output: Danh sách ý tưởng chi tiết

Agent 2: Lập kế hoạch
├─ Input: Danh sách ý tưởng
├─ Process: Sắp xếp, tạo outline
└─ Output: Cấu trúc bài viết

Agent 3: Viết nội dung
├─ Input: Cấu trúc bài viết
├─ Process: Viết từng phần, kiểm tra ngữ pháp
└─ Output: Bài viết hoàn chỉnh

Agent 4: Kiểm tra chất lượng
├─ Input: Bài viết
├─ Process: Kiểm tra nội dung, SEO, định dạng
└─ Output: Báo cáo chất lượng + Phê duyệt
```

---

## 🚀 Tiếp Theo: Chạy Trên Claude Pro

Khi bạn chạy trên Claude Pro, bạn có thể:

1. **Tải Dashboard này lên Claude**
2. **Mô tả quy trình của bạn**
3. **Claude sẽ tự động hóa** các Agent
4. **Chạy toàn bộ quy trình** tự động

Ví dụ:
```
"Viết một bài blog 2000 từ về Python"
↓
Claude chạy 4 Agent lần lượt:
- Agent 1: Thu thập ý tưởng
- Agent 2: Lập kế hoạch
- Agent 3: Viết nội dung  
- Agent 4: Kiểm tra
↓
Kết quả: Bài blog hoàn chỉnh
```

---

## ❓ Câu Hỏi Thường Gặp

**Q: Dữ liệu của tôi có được lưu trên server không?**
A: Không, tất cả dữ liệu chỉ lưu trên máy tính của bạn trong Local Storage.

**Q: Tôi có thể chia sẻ Dashboard với người khác không?**
A: Có! Bạn có thể:
- Chia sẻ link GitHub repository
- Export dữ liệu JSON (xem phần Sao Lưu)
- Người khác mở file index.html và import dữ liệu

**Q: Tôi có thể thêm bao nhiêu Agent?**
A: Không giới hạn! Thêm bao nhiêu cũng được.

**Q: Làm sao để reset toàn bộ dữ liệu?**
A: Mở Console (F12), gõ: `localStorage.clear()` rồi F5 tải lại.

---

## 📞 Hỗ Trợ

Nếu có vấn đề:
1. Mở Console (F12)
2. Kiểm tra có lỗi không (đoạn text đỏ)
3. Copy lỗi đó
4. Tạo Issue trên GitHub repository

---

**Chúc bạn sử dụng Dashboard Agent vui vẻ! 🎉**