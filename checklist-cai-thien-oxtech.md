# Checklist cải thiện landing page oxtech.vn

Đánh giá ngày 05/07/2026, cập nhật sau khi sửa trực tiếp trên code ngày hôm nay.

## Ưu tiên 1 — Lỗi cần sửa ngay

- [x] Sửa link `mailto:` ở footer: đổi từ `info@positivus.com` thành `bao.tnp@oxtech.vn`.
- [x] Sửa `og:url` (và URL trong JSON-LD, vike pageContext) từ placeholder `https://url/` thành `https://oxtech.vn/`.
- [x] Thêm nội dung cho `og:image` (dùng ảnh `apple-touch-icon`).
- [x] `<html lang="vi-VN">` — kiểm tra lại thì thực ra đã có sẵn, không cần sửa (lần đánh giá trước bị nhầm do lỗi đọc file).

## Ưu tiên 2 — Dọn tài nguyên rác

- [x] Đã kiểm tra lại: trang thực tế chỉ tải ~730KB (không nặng như đánh giá ban đầu — con số 8.6MB là tổng cả thư mục `assets/`, phần lớn không được trang gọi tới).
- [x] Xóa 8 file ảnh/SVG không được bất kỳ trang nào trong repo tham chiếu (4 PNG "positivus-cover...", 4 SVG "Picture..."), tổng ~7.8MB rác từ template gốc. `assets/` giảm từ 9MB còn 1.3MB.

## Ưu tiên 3 — SEO & đo lường

- [x] Viết lại meta description (và og:description) có từ khóa chuyển đổi số, phát triển phần mềm, tư vấn công nghệ.
- [ ] Gắn Google Analytics hoặc công cụ tương đương để đo traffic và tỷ lệ click "Liên hệ" — **chưa làm**, cần bạn cung cấp Measurement ID (GA4) nếu muốn triển khai.
- [ ] Gắn Meta Pixel nếu có kế hoạch chạy quảng cáo Facebook sau này — **chưa làm**, tùy nhu cầu.

## Ưu tiên 4 — UX liên hệ

- [x] Thêm form liên hệ trực tiếp (Họ tên, Email, SĐT, Nội dung) trong mục Liên hệ, gửi qua **Web3Forms**.
- [x] Đã gắn access key thật vào form (`7973e828-4803-4eeb-82df-cbe1f665e6f0`) — form đã sẵn sàng hoạt động.

## Lưu ý quan trọng

- File `index.html` có thuộc tính `data-ws-project` / `data-ws-last-published` — cho thấy trang được xuất bản (publish) từ một công cụ dựng web dạng kéo-thả (khả năng là Webstudio) dựa trên template Figma "Positivus". Nếu sau này bạn chỉnh sửa và publish lại từ công cụ đó, **các thay đổi tay ở trên (đặc biệt là form liên hệ) có thể bị ghi đè mất**. Nếu muốn giữ form, cân nhắc thêm nó qua tính năng "custom code/embed" ngay trong công cụ dựng web đó, thay vì chỉ sửa file tĩnh.
