# PHIẾU KIỂM THỬ — EDUSAFE AI
(Phần "thí nghiệm" cho báo cáo — SỐ THẬT, KHÔNG BỊA!)

- **Ngày:** ......../11/2026 · **Người kiểm thử:** Minh PHú 
- **Chạy:** `run.bat` → `http://127.0.0.1:3000` **hoặc** `https://edusafe-ai.onrender.com`
- **Tài khoản:** dùng tài khoản MỚI (chưa có nhật ký cảm xúc)
  *(lý do: eff = max(điểm từ chữ, 100 - trung bình nhật ký); tài khoản mới thì "sàn" = 15)*

## CÁCH LÀM (mỗi mục 3 bước)
1. **ĐIỀN DỰ ĐOÁN TRƯỚC** — tính theo công thức `app.py` dòng 116–138
2. **Gõ / thao tác THẬT** trên app
3. **GHI KẾT QUẢ THẬT** → so → ✓ / ✗

> Trang CHAT sẽ hiện dòng `⚠️ [CẢNH BÁO] Mức độ nguy cơ: .... (X/100)` khi điểm ≥ 30.
> **KHÔNG có dòng ⚠️ = điểm eff < 30** (không hiện).

---

## PHẦN A — TRÒ CHUYỆN AI (13 câu)

| # | Câu gõ vào chat | Dự đoán (điểm · có ⚠️ không) | Thực tế | ✓/✗ |
|---|----------------|-------------------------------|---------|-----|
| 1 | Chào bạn, hôm nay mình vui lắm! | | | |
| 2 | Hôm nay áp lực thi quá, stress mệt mỏi | | | |
| 3 | Mình buồn lắm, khóc một mình cả ngày | | | |
| 4 | Bị bạn đánh ở trường | | | |
| 5 | Bị bạn đánh ở trường mà stress lắm | | | |
| 6 | Nó đe dọa giết mình, mang theo vũ khí | | | |
| 7 | Muốn tự tử quá, sống không nổi nữa | | | |
| 8 | Bị lột tiền ở cổng sau, sợ quá | | | |
| 9 | Hôm nay học bài xong, đi chơi với bạn vui | | | |
| 10 | Sợ đi học quá, bị các bạn tẩy chay | | | |
| 11 | Mình stress vì bài tập nhiều quá | | | |
| 12 | Hôm nay chơi game, muốn giết con boss đó cho đã | | | |
| 13 | Mình áp lực bài tập quá, lo lắng không ngủ được | | | |

*(#9 = bẫy "học bài" · #11–13 = bẫy CHỦ ĐỀ VÔ HẠI — app phải bình tĩnh!)*

---

## PHẦN B — NHẬT KÝ CẢM XÚC (6 mục)

| # | Thao tác | Dự đoán (điểm + nhãn) | Thực tế | ✓/�� |
|---|---------|------------------------|---------|-----|
| 1 | mood 😊 Vui + note "Hôm nay được 10 điểm toán" | | | |
| 2 | mood 😐 Bình thường + note "Hôm nay bình thường" | | | |
| 3 | mood 😢 Buồn + note "Bị các bạn chê xấu trước lớp" | | | |
| 4 | mood 😰 Lo âu + note "Ngày mai thi mà chưa học bài" | | | |
| 5 | mood 😡 Tức giận + note "Bị bạn giật sách" | | | |
| 6 | Lưu mood buổi "sáng" xong → lưu LẠI buổi "sáng" cùng ngày (dòng 529–530) | | | |

**+ Sau mục 3–5:** mở trang **teacher_alerts** → có cảnh báo nào không? ghi vào cột Thực tế.

---

## PHẦN C — LỖI TÀI KHOẢN / API (3 mục)

| # | Thao tác | Mã lỗi dự kiến | Thực tế | ✓/✗ |
|---|---------|----------------|---------|-----|
| 1 | Đăng ký thiếu email | 400 "Thiếu thông tin bắt buộc" | | |
| 2 | Đăng ký username đã có | 400 "Username đã tồn tại" | | |
| 3 | Đăng nhập sai mật khẩu | 401 "Sai tài khoản hoặc mật khẩu" | | |

---

## BẢNG TỔNG HỢP (điền sau khi làm xong)

- Phần A: **....../13** khớp · Phần B: **....../6** · Phần C: **....../3**
- **Tổng = ......./22 · Tỷ lệ chính xác = .......%** ← SỐ THẬT đưa thẳng vào báo cáo!
- **Phát hiện mới** (từ khóa nào app KHÔNG bắt được?):

........................................................................

---

# 🙈 ĐÁP ÁN DỰ ĐOÁN CỦA THẦY — ĐIỀN XONG MỚI ĐỌC!

.

.

.

**PHẦN A:**
1. **0 điểm** · không ⚠️
2. **15** (stress +15) · không ⚠️ (<30)
3. **12** (buồn +12) · không ⚠️
4. **30** (bị đánh = high) · ⚠️ "Trung bình - Cần chú ý (30/100)" · KHÔNG alert
5. **45** (30+15) · ⚠️ (45/100) · KHÔNG alert (<50)
6. **42** (30 + "giet" 12) · ⚠️ (42/100) · KHÔNG alert
7. **70** (tự tử 40 + 30) · ⚠️ "NGUY HIỂM - Cần hành động ngay! (70/100)" · **CÓ ALERT critical cho thầy!**
8. **0 điểm** · KHÔNG ⚠️ → **PHÁT HIỆN: app KHÔNG bắt "bị lột tiền" — từ khóa thiếu!**
9. **0 điểm** · không ⚠️ (bẫy — "học bài" KHÔNG phải bạo lực)
10. **10** (sợ đi học = low) · không ⚠️ (10 < 30)
11. **15** (stress +15) · không ⚠️ — từ "stress" có nhưng ĐIỂM THẤP
12. **12** ("giet" +12) · không ⚠️ — từ "giết" có nhưng ĐIỂM THẤP (ngữ cảnh game!)
13. **30** ("ap luc" 15 + "lo lang" 15) · ⚠️ (30/100) → **FALSE POSITIVE!**
    *(chủ đề học tập vô hại mà vẫn bị báo động → PHÁT HIỆN HẠN CHẾ: regex không hiểu ngữ cảnh!)*

**PHẦN B:** 1) ≥70 "An toàn" 2) ~70 3) <70 4) <70 5) <70 6) **BỊ CHẶN** (mỗi buổi chỉ 1 lần)

**PHẦN C:** đúng như cột "mã lỗi dự kiến" (nếu sai = BUG THẬT → ghi vào phát hiện mới!)

---
*Phiếu này = "Bước 5: Kiểm thử" của báo cáo. Số liệu GIỜ MỚI THẬT 100%!*
