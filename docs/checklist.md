# Checklist tự kiểm tra – Giai đoạn 1

## HTML
- [x] Chỉ có một thẻ `h1`, các heading theo đúng thứ tự `h1 → h2 → h3`
- [x] Dùng thẻ ngữ nghĩa thay cho `div` khi có thể (`header`, `nav`, `main`, `section`, `article`, `footer`, `address`, `figure`)
- [x] Khai báo `lang="vi"`, `meta viewport`, `meta description`, `title`
- [x] Ảnh nội dung có `alt` mô tả, ảnh trang trí có `alt=""`
- [x] Ảnh có `width`/`height` để tránh layout shift
- [x] Mỗi input có `label` tương ứng, có `autocomplete`

## CSS
- [x] `box-sizing: border-box` cho mọi phần tử
- [x] Không dùng giá trị "magic number": màu, khoảng cách, bo góc lấy từ biến CSS
- [x] Mobile-first, breakpoint dùng `min-width`
- [x] Flexbox cho bố cục một chiều, Grid cho bố cục hai chiều
- [x] Chỉ dùng `!important` trong khối `prefers-reduced-motion`

## Accessibility
- [x] Skip link hiện ra khi focus
- [x] `:focus-visible` rõ ràng trên mọi phần tử tương tác
- [x] Vùng chạm tối thiểu 44×44px trên mobile
- [x] Tôn trọng `prefers-reduced-motion`

## Kiểm thử
- [x] Không có thanh cuộn ngang ở 375px, 800px, 1280px
- [ ] Kiểm tra HTML bằng W3C Validator
- [ ] Chạy Lighthouse (Accessibility, Best Practices)
