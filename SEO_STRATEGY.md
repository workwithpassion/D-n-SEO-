# SEO Strategy & Deployment Checklist

## 1. Keyword Strategy & Research Summary
- **Niche:** Excel Troubleshooting cho dân văn phòng (nhỏ, dễ tiếp cận, độ khó cạnh tranh thấp).
- **Pillar Keyword (Trang chủ):** Các lỗi thường gặp trong Excel và cách khắc phục (Search volume ổn định, giải quyết vấn đề tổng quan).
- **Long-tail Keywords (Articles):**
  1. *cách sửa lỗi value trong excel* (loi-value-trong-excel.html)
  2. *cách khắc phục lỗi ref trong excel* (loi-ref-trong-excel.html)
  3. *lỗi name trong excel là gì* (loi-name-trong-excel.html)
  4. *sửa lỗi div/0 trong excel* (loi-div-0-trong-excel.html)
  5. *file excel bị nặng xử lý chậm* (file-excel-bi-cham.html)

Tất cả các bài viết đều nhắm mục tiêu vào Search Intent rõ ràng: Khắc phục sự cố (Troubleshooting & How-to).

## 2. Full Folder Structure
Mã nguồn đã được tạo đáp ứng chuẩn cấu trúc:
```text
/
├── index.html                  # Pillar Page (Homepage)
├── sitemap.xml                 # SEO Sitemap
├── robots.txt                  # Crawl Rules
├── style.css                   # Global Styles (Pure CSS, mobile-friendly)
├── SEO_STRATEGY.md             # Tài liệu chiến lược
└── articles/                   # Content Cluster
    ├── loi-value-trong-excel.html
    ├── loi-ref-trong-excel.html
    ├── loi-name-trong-excel.html
    ├── loi-div-0-trong-excel.html
    └── file-excel-bi-cham.html
```
(Các file thư viện React mặc định đã được dọn dẹp để đảm bảo 100% No-JS/Pure HTML).

## 3. SEO Audit Checklist (Implementation Verified)
- [x] **Meta Tags:** Tiêu đề (<= 60 chars), Meta Description (<= 160 chars) chứa keyword.
- [x] **Canonical Tags:** Tránh duplicate content, trỏ đúng URL.
- [x] **Open Graph:** Đã tích hợp cho chia sẻ MXH.
- [x] **Semantic HTML:** Cấu trúc `<header>`, `<main>`, `<article>`, `<footer>` đầy đủ.
- [x] **Heading Structure:** Mỗi trang CHỈ có một `<h1>` làm Exact search query, theo sau là `<h2>` và `<h3>` logic.
- [x] **Schema Markup (JSON-LD):** Được tích hợp (WebSite cho trang chủ, Article và HowTo/FAQ cho bài viết).
- [x] **Internal Linking:** Trang chủ link tới bài con, bài con có link điều hướng về Trang chủ và link chéo tới bài liên quan.
- [x] **Core Web Vitals Optimized:** Không có library ngoài, CSS inline critical (cho phần LCP), CSS siêu gọn nhẹ, đảm bảo LCP < 2s.

## 4. Deployment Checklist (Vercel)
Website hiện là 100% tài nguyên tĩnh, sẵn sàng deploy ngay lập tức!
1. **Xuất mã nguồn:** Mở Menu tùy biến (Settings) ở góc trên, click "Export as ZIP", giải nén folder.
2. **Đẩy lên GitHub:**
   ```bash
   git init
   git add .
   git commit -m "SEO Foundation Setup"
   git push origin main
   ```
3. **Kết nối Vercel:**
   - Truy cập [Vercel](https://vercel.com/new).
   - Chọn Import project từ GitHub.
   - Build Command: Bỏ trống (Override về rỗng).
   - Output Directory: Bỏ trống (Mặc định).
   - Bấm **Deploy**.
4. **Kiểm tra Indexing Files:**
   - Truy cập `https://<ten-mien-vercel>/sitemap.xml`
   - Truy cập `https://<ten-mien-vercel>/robots.txt`

## 5. Post-Launch Action Plan (2-4 Weeks)
- **Tuần 1:**
  - Setup **Google Search Console** và **Google Analytics 4**.
  - Submit sitemap `sitemap.xml` lên GSC để ép Google quét hệ thống.
  - Mang bài viết Share lên mạng xã hội (Facebook, LinkedIn cá nhân).
- **Tuần 2:**
  - Tạo tài khoản và trả lời thắc mắc trên các cộng đồng (Ví dụ: Group Tự Học Excel, Reddit r/excel) -> chèn tự nhiên URL của bài viết vào bình luận để tạo traffic thật.
- **Tuần 3 & 4:**
  - Viết Email hoặc liên hệ qua Fanpage các cộng đồng học Kế Toán / Hành Chính xin Guest Post hoặc đặt link.
  - Mở GSC kiểm tra *Performance* -> Xem Queries nào đang có số lần hiển thị (Impressions) nhiều nhất để tiếp tục bổ sung nội dung cho từ khóa đó.
