# TechStart Internship – Responsive Landing Page

Mini project **Giai đoạn 1 – HTML & CSS Fundamentals** (Frontend Developer Roadmap 2026).

Landing page giới thiệu chương trình thực tập Frontend, dựng hoàn toàn bằng **HTML5 + CSS3 thuần** (không framework, không JavaScript), responsive từ 320px đến màn hình desktop lớn.

## Mục tiêu giai đoạn và cách áp dụng

| Nội dung kiến thức | Áp dụng trong dự án | File |
| --- | --- | --- |
| **Semantic HTML & Accessibility** | Dùng `header`, `nav`, `main`, `section`, `article`, `figure`, `address`, `footer`; mỗi section có `aria-labelledby`; skip link "Bỏ qua điều hướng"; `alt` cho ảnh nội dung, `alt=""` cho ảnh trang trí; `label` gắn `for` với từng input; `:focus-visible` rõ ràng; vùng chạm nút menu 44×44px; `prefers-reduced-motion`; FAQ dùng `details/summary` hỗ trợ bàn phím sẵn | `index.html`, `css/base.css` |
| **CSS Box Model, Selectors & Typography** | `box-sizing: border-box` toàn trang; design tokens bằng CSS custom properties (màu, khoảng cách, bo góc, đổ bóng); cỡ chữ co giãn bằng `clamp()`; selector `:not()`, `:checked ~`, `+`, `> * + *`, `::before/::after`, `[open]`, `:user-invalid`; đặt tên class theo BEM đơn giản | `css/base.css`, `css/components.css` |
| **Flexbox, CSS Grid & Responsive Design** | Flexbox cho header, nhóm nút, mentor list, timeline item; Grid cho hero 2 cột, feature grid `repeat(auto-fit, minmax(240px, 1fr))`, pricing 1→2→3 cột, form 2 cột, footer; mobile-first với 3 breakpoint `640px / 960px / 1200px`; menu hamburger thuần CSS (checkbox hack) | `css/layout.css`, `css/responsive.css` |
| **Mini project: Responsive Landing Page** | 7 khu vực: Hero, Lợi ích, Lộ trình, Mentor, Gói học, Hỏi đáp, Form đăng ký + Footer | toàn bộ repo |

## Cấu trúc thư mục

```
tts-gd1-responsive-landing-page/
├── index.html            # Toàn bộ nội dung trang (semantic HTML)
├── css/
│   ├── base.css          # Design tokens, reset, typography, tiện ích a11y
│   ├── layout.css        # Bố cục: container, header, hero, section, grid, footer
│   ├── components.css    # Button, card, tag, badge, timeline, FAQ, form, hamburger
│   └── responsive.css    # Media query mobile-first + style khi in
├── assets/images/        # Logo, hình minh họa, icon, avatar (SVG)
└── docs/checklist.md     # Checklist tự kiểm tra trước khi nộp
```

Thứ tự nạp CSS: `base → layout → components → responsive`, để media query luôn được áp dụng sau cùng.

## Hướng dẫn chạy

Không cần cài đặt gì. Chọn một trong các cách:

1. Mở trực tiếp file `index.html` bằng trình duyệt.
2. Dùng extension **Live Server** của VS Code → chuột phải `index.html` → *Open with Live Server*.
3. Dùng server tĩnh:

   ```bash
   # Python
   python -m http.server 5500
   # hoặc Node.js
   npx serve .
   ```

   Sau đó mở `http://localhost:5500`.

## Responsive

| Kích thước | Bố cục |
| --- | --- |
| < 640px (mobile) | 1 cột, menu hamburger, form 1 cột |
| 640px – 959px (tablet) | Gói học 2 cột, form 2 cột, timeline 2 cột, footer 3 cột |
| ≥ 960px (laptop) | Menu ngang, hero 2 cột, gói học 3 cột (gói nổi bật phóng to), timeline 4 cột có đường nối |
| ≥ 1200px | Tăng khoảng cách section |

Đã kiểm tra bằng chế độ thiết bị của Chrome DevTools ở 375px, 800px và 1280px — không có thanh cuộn ngang.

## Accessibility

- Toàn bộ trang dùng được bằng bàn phím (Tab / Shift+Tab / Enter / Space).
- Màu chữ chính `#1f2937` trên nền trắng và chữ trắng trên `#4f46e5` đều đạt tương phản WCAG AA.
- Form dùng validate HTML5: `required`, `type="email"`, `minlength/maxlength`, `pattern` cho số điện thoại, thông báo gợi ý gắn bằng `aria-describedby`.
- Có thể kiểm tra thêm bằng Lighthouse (Accessibility) hoặc extension axe DevTools.

## Tác giả

Thực tập sinh Frontend – TechStart Internship 2026.
