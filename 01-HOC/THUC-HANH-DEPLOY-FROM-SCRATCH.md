# THỰC HÀNH DEPLOY TỪ ĐẦU — GitHub + Render
Ngày: 23/11/2026 · Thời lượng: 45-60 phút · Người thực hiện: Minh

## ⚠️ QUY TẮC VÀNG (đọc TRƯỚC khi xóa gì)
- [ ] **File trong máy = KHÔNG BAO GIỜ XÓA** (máy là bản gốc + phao cứu sinh)
- [ ] **`.env` KHÔNG push** (gitignore giữ nó) → mở sẵn file `.env` để copy giá trị sang Render
- [ ] **Phao cứu sinh test trước:** chạy `run.bat` → app mở `127.0.0.1:3000` ✓ → mới được bắt đầu

## PHASE 0 — GHI LẠI THÔNG TIN (5 phút)
- [ ] Chạy `git remote -v` → chụp/chép URL lại
- [ ] Render → service `edusafe-ai` → tab **Environment** → chụp TOÀN BỘ biến (AI_MODE, GEMINI_API_KEY, JWT_SECRET, SECRET_KEY, OPENCODE_API_KEY...)
- [ ] GitHub repo: ghi tên `Ai-si-u-an-to-n-2-` + loại (Public/Private) — xem ở Settings trước khi xóa

## PHASE 1 — XÓA + TẠO LẠI GITHUB (15 phút)
- [ ] Kiểm tra chưa có gì bị bỏ sót: `git status` → nếu có → `git add .` + `git commit`
- [ ] GitHub → repo → **Settings → Danger Zone → Delete this repository**
- [ ] Tạo repo MỚI:
      - [ ] Tên **TRÙNG NGUYÊN**: `Ai-si-u-an-to-n-2-`
      - [ ] Visibility **giống cũ** (Public/Private)
      - [ ] **KHÔNG** tick README/.gitignore (tạo trống để không có commit lạ)
- [ ] Máy: `git push origin main` *(URL cũ vẫn đúng vì trùng user + tên repo)*
      - Lỗi quyền → `git remote set-url origin https://github.com/minhphudanghb2023-cloud/Ai-si-u-an-to-n-2-.git` rồi push lại
- [ ] **Kiểm tra trên GitHub:** thấy 6 file gốc + `templates/` + `run.bat` + `.gitignore`
- [ ] **KIỂM TRA QUAN TRỌNG:** KHÔNG thấy `.env` trong repo! ✅

## PHASE 2 — XÓA + TẠO LẠI RENDER (25 phút)
- [ ] Render → `edusafe-ai` → Settings (cuối trang) → **Delete Service**
- [ ] **New + → Web Service** → Connect GitHub repo vừa tạo (authorize nếu bắt)
- [ ] Cài đặt:
      - [ ] Name: **`edusafe-ai`** (TRÙNG TÊN = lấy lại URL cũ `edusafe-ai.onrender.com`)
      - [ ] Branch: **main** · Region: giống cũ
- [ ] Tab **Environment → Add** từng biến, copy giá trị từ file `.env` trong máy
- [ ] **Create Web Service** → chờ build 5-10 phút (xem Log nếu lỗi)
- [ ] Mở `https://edusafe-ai.onrender.com` → **đăng ký tài khoản test MỚI**

## PHASE 3 — KIỂM TRA HAI CHỖ (5 phút)
- [ ] Chat 1 câu → AI trả lời ✓
- [ ] Lưu 1 nhật ký → điểm hiện ✓
- [ ] Push thêm 1 commit nhỏ → Render: Manual Deploy → **Deploy latest commit** (tập flow thường ngày) ✓

## ❌ NẾU HỎNG — CÁCH XỬ LÝ
| Lỗi | Xử lý |
|---|---|
| Push lỗi quyền | `git remote -v` → kiểm tra đăng nhập GitHub (credential) |
| Render build lỗi | Đọc **Log** → thiếu file gì? (.env KHÔNG có trên repo là ĐÚNG!) |
| URL cũ không lấy lại được | Đặt lại tên `edusafe-ai` (tên còn trống = lấy lại được) |
| Lỡ tay xóa nhầm file máy | **BÁO THẦY NGAY** — đừng tự cố sửa |

## ⏰ THỜI ĐIỂM
- Làm: **TỐI 23/11** hoặc **SÁNG 24/11 TRƯỚC buổi test**
- **24-28/11: KHÔNG xóa / KHÔNG deploy** giữa chừng (đang có số liệu + tài khoản test)
- Xong tập → **QUIZ Khu 4-6** (vẫn nợ tối nay!)
