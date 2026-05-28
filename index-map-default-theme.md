# Index Map – `Default Theme`

Tài liệu này map giữa **source code file**, **chức năng (function/role)** và **cấu hình liên quan** trong theme `Default Theme`, viết theo kiểu dễ hiểu cho dev entry-level.

> Phạm vi kiểm tra chính: `templates/page.json`, `templates/product.json`, `sections/main-page.liquid`, `sections/main-product.liquid`.

---

## 1) Tổng quan nhanh

### Có cấu hình cho Page không?
**Có.**
- `templates/page.json` dùng section `main-page`
- `sections/main-page.liquid` render:
  - tiêu đề page (`page.title`)
  - nội dung page (`page.content`)
  - padding trên/dưới từ settings

### Có cấu hình cho Product không?
**Có, và khá nhiều.**
- `templates/product.json` dùng section `main-product`
- `sections/main-product.liquid` là file điều khiển toàn bộ product page:
  - media gallery
  - title / price / inventory / description
  - variant picker
  - buy buttons
  - reviews / testimonials / FAQ / related products
  - nhiều custom blocks khác

---

## 2) Index map theo file

## A. `templates/page.json`

| File | Function / vai trò | Cấu hình liên quan | Ý nghĩa dễ hiểu |
|---|---|---|---|
| `templates/page.json` | Khai báo template cho trang page | `sections.main.type = "main-page"` | Đây là file nối page template với section hiển thị nội dung page |
| `templates/page.json` | Chọn section chính | `settings.padding_top`, `settings.padding_bottom` ở section `main-page` | Chỉ truyền cấu hình layout cơ bản, không có block phức tạp |

### Nội dung thực tế
```json
{"sections":{"main":{"type":"main-page","settings":{"padding_top":36,"padding_bottom":36}}},"order":["main"]}
```

### Kết luận
- Page template **có cấu hình**
- Nhưng là cấu hình **tối giản**
- Không thấy block/page builder phức tạp trong template này

---

## B. `sections/main-page.liquid`

| File | Function / vai trò | Cấu hình liên quan | Ý nghĩa dễ hiểu |
|---|---|---|---|
| `sections/main-page.liquid` | Render nội dung page | `page.title`, `page.content` | Hiển thị tiêu đề và nội dung của page trong admin Shopify |
| `sections/main-page.liquid` | Điều chỉnh khoảng cách layout | `padding_top`, `padding_bottom` | Cho phép chỉnh độ thoáng trên/dưới của section |
| `sections/main-page.liquid` | Tạo style theo section | `.section-{{ section.id }}-padding` | Mỗi section có padding riêng theo ID |

### Flow hoạt động
1. Theme load section `main-page`
2. CSS nội bộ set padding theo settings
3. Hiển thị `<h1>` bằng `page.title`
4. Hiển thị nội dung bằng `page.content`

### Cái có
- Title page
- Content page
- Padding trên/dưới

### Cái chưa có
- Không có image banner
- Không có sidebar
- Không có block editor
- Không có FAQ riêng cho page
- Không có custom metafield render trực tiếp trong file này

---

## C. `templates/product.json`

| File | Function / vai trò | Cấu hình liên quan | Ý nghĩa dễ hiểu |
|---|---|---|---|
| `templates/product.json` | Khai báo template cho product page | `sections.main.type = "main-product"` | Đây là nơi product page được ghép từ section chính và nhiều block |
| `templates/product.json` | Chứa dữ liệu block cụ thể | `blocks`, `block_order`, `settings` | Toàn bộ cấu hình hiển thị của product page nằm ở đây |
| `templates/product.json` | Gắn section chính cho product | `settings` của `main-product` | Điều khiển layout, gallery, spacing, thumbnails, mobile behavior |

### Điểm đáng chú ý
File này **rất dày cấu hình**, gồm:
- block nội dung product
- block custom html/liquid
- block reviews / testimonials
- block collapsible tabs
- block comparison / results / custom columns
- block related products
- custom CSS

### Kết luận
- Product template **có cấu hình rất nhiều**
- Đây không phải product page mặc định tối giản
- Có nhiều custom section/blocks phục vụ marketing/sales

---

## D. `sections/main-product.liquid`

| File | Function / vai trò | Cấu hình liên quan | Ý nghĩa dễ hiểu |
|---|---|---|---|
| `sections/main-product.liquid` | Render toàn bộ product page | `section.blocks`, `section.settings`, `product.*` | File trung tâm điều khiển hiển thị product |
| `sections/main-product.liquid` | Render media gallery | `product.media`, `variant_images`, `gallery_layout`, `media_position` | Quản lý ảnh/video/3D model của sản phẩm |
| `sections/main-product.liquid` | Render title | block type `title` | In tiêu đề sản phẩm |
| `sections/main-product.liquid` | Render rating stars | block type `rating_stars` | Hiển thị đánh giá sao |
| `sections/main-product.liquid` | Render price | block type `price` | Hiển thị giá, sale badge, installment |
| `sections/main-product.liquid` | Render inventory | block type `inventory` | Hiển thị tồn kho / trạng thái stock |
| `sections/main-product.liquid` | Render description | block type `description` | Hiển thị mô tả sản phẩm |
| `sections/main-product.liquid` | Render variant picker | block type `variant_picker` | Chọn variant / quantity breaks |
| `sections/main-product.liquid` | Render buy buttons | block type `buy_buttons` | Nút Add to cart / Buy it now |
| `sections/main-product.liquid` | Render custom content blocks | `custom_liquid`, `text`, `icon_with_text`, `collapsible_tab`, ... | Tạo nội dung marketing/benefit/FAQ |

### Luồng xử lý chính
1. Check cấu hình padding / layout
2. Load model viewer nếu product có 3D model
3. Xác định variant images và trạng thái hide variants
4. Render gallery bên trái
5. Render toàn bộ block bên phải theo `section.blocks`
6. Áp settings như sticky info, thumbnails, mobile layout

### Cái có trong file này
- Product title
- Product gallery
- Price & sale badge
- Inventory status
- Description
- Variant picker
- Buy buttons
- Reviews / testimonials
- Collapsible tabs / FAQ
- Related products
- Custom sections cho marketing

### Cái chưa có / không thấy trực tiếp
- Không thấy metafield mapping đặc thù trong đoạn đã kiểm tra
- Không thấy cấu hình schema cho custom product data riêng (ví dụ namespace/keys metafield)
- Không thấy logic checkout riêng trong file này
- Không thấy server-side product transform

---

## 3) Map chi tiết giữa block type và ý nghĩa

### Block types phổ biến trong `main-product`

| Block type | Vai trò | Dễ hiểu như |
|---|---|---|
| `title` | Hiển thị tên sản phẩm | Header của trang product |
| `price` | Hiển thị giá | Khu giá tiền + sale |
| `inventory` | Hiển thị tồn kho | Trạng thái còn hàng/hết hàng |
| `description` | Hiển thị mô tả | Nội dung giới thiệu sản phẩm |
| `variant_picker` | Chọn biến thể | Màu / size / bundle |
| `buy_buttons` | Nút mua hàng | Add to cart / Buy now |
| `rating_stars` | Sao đánh giá | Rating summary |
| `custom_liquid` | Chèn HTML/Liquid custom | Dùng để gắn badge/CTA riêng |
| `text` | Text + icon | Bullet list / highlight |
| `icon_with_text` | Icon + text box | Benefit cards |
| `collapsible_tab` | Tab gập/mở | Shipping, FAQ, guarantee |
| `reviews` | Review slider | Customer testimonials |
| `comparison-table` | Bảng so sánh | Compare với đối thủ |
| `related-products` | Sản phẩm liên quan | Cross-sell |

---

## 4) Map cấu hình theo nhóm

## A. Layout / spacing
- `padding_top`, `padding_bottom` ở page
- `mobile_padding_top`, `mobile_padding_bottom`, `desktop_padding_top`, `desktop_padding_bottom` ở product
- Mục đích: chỉnh khoảng trắng cho section

## B. Gallery / media
- `media_size`
- `media_position`
- `gallery_layout`
- `desktop_thumbnails_count`
- `mobile_thumbnails`
- `image_zoom`
- `enable_video_looping`
- `autoplay_videos_pause_btn`

## C. Product info
- `enable_sticky_info`
- `hide_variants`
- `variant_image_filtering`
- `display_id`

## D. Conversion / sales blocks
- `buy_buttons`
- `variant_picker`
- `price`
- `inventory`
- `rating_stars`
- `sticky_atc` (disabled trong JSON hiện tại)

## E. Marketing content
- `emoji_benefits`
- `reviews`
- `testimonials`
- `results`
- `comparison-table`
- `collapsible-content`
- `image-slider`
- `image-with-text`
- `custom-columns`

---

## 5) Những gì theme này đang có vs chưa có

### Đang có
- Page template cơ bản
- Product template rất nhiều custom blocks
- Layout settings đầy đủ cho product page
- Nhiều section marketing/testimonials/FAQ
- Custom CSS trong template product

### Chưa thấy rõ
- Metafield/Metaobject mapping cụ thể trong file đã xem
- Logic page builder cho page template
- Schema dữ liệu riêng cho content model của page
- Xử lý app block theo kiểu chuẩn hoá nhiều hơn (có thể có, nhưng chưa thấy trong phần kiểm tra)
- Tài liệu cấu trúc block map chính thức cho team dev

---

## 6) Kết luận ngắn gọn

- **Page**: có cấu hình, nhưng đơn giản.
- **Product**: có cấu hình rất nhiều, gần như là một product page custom theo hướng marketing.
- Nếu mục tiêu là hiểu “file nào chịu trách nhiệm gì”, thì:
  - `templates/*.json` = khai báo layout + block configuration
  - `sections/*.liquid` = code render UI thật
  - `config/settings_data.json` = cấu hình theme ở cấp toàn site

---

## 7) Cây luồng render: `templates -> sections -> snippets -> assets`

### 7.1 Luồng tổng quát
```text
templates/*.json
  -> chọn section chính / block order / settings
sections/*.liquid
  -> render HTML + logic + gọi snippets
snippets/*.liquid
  -> tái sử dụng UI/logic nhỏ
assets/*
  -> CSS/JS hỗ trợ tương tác và style
```

### 7.2 Ví dụ luồng Page
- `templates/page.json`
  - trỏ tới `main-page`
- `sections/main-page.liquid`
  - render `page.title`, `page.content`
  - tự tạo padding CSS
- `snippets/*`
  - **không thấy được dùng trực tiếp** trong `main-page.liquid`
- `assets/*`
  - **không cần JS riêng** cho page cơ bản này

### 7.3 Ví dụ luồng Product
- `templates/product.json`
  - trỏ tới `main-product`
  - chứa block config rất nhiều
- `sections/main-product.liquid`
  - render gallery, title, price, inventory, tabs, reviews...
  - gọi nhiều snippet như:
    - `product-media-gallery`
    - `text-with-icon-block`
    - `rating-stars-block`
    - `trustpilot-stars-block`
    - `price`
    - `material-icon`
    - `product-variant-picker` / `buy-buttons` (tùy phần tiếp theo của file)
- `snippets/*.liquid`
  - tách logic thành module nhỏ để dễ bảo trì
- `assets/*.js` / `assets/*.css`
  - hỗ trợ zoom, gallery, search, quick add, sticky, slider, review UI

---

## 8) Map riêng cho `templates/product.json` theo từng block

> Ghi chú: `product.json` là file cấu hình, nên “function” ở đây hiểu là **vai trò render** của block đó trong `sections/main-product.liquid`.

| Block type / block key | Vai trò | File render chính | Dễ hiểu |
|---|---|---|---|
| `rating_stars` | Hiện rating sao trên đầu product | `sections/main-product.liquid` | Cho khách thấy review score |
| `custom_liquid` | Chèn HTML/Liquid custom | `sections/main-product.liquid` | Badge/CTA tự thiết kế |
| `title` | Hiện tên sản phẩm | `sections/main-product.liquid` | Product name |
| `text` | Dòng text ngắn + icon | `sections/main-product.liquid` + snippet `text-with-icon-block` | Bullet highlight |
| `price` | Hiện giá / sale / installment | `sections/main-product.liquid` + snippet `price` | Khu giá bán |
| `inventory` | Hiện stock | `sections/main-product.liquid` | Còn hàng / ít hàng |
| `emoji_benefits` | Danh sách benefit có emoji | `sections/main-product.liquid` hoặc custom block renderer | Điểm mạnh sản phẩm |
| `variant_picker` | Chọn biến thể / bundle | `sections/main-product.liquid` | Màu, size, combo |
| `buy_buttons` | Nút mua | `sections/main-product.liquid` | Add to cart / Buy now |
| `icon_with_text` | Icon + heading + text | `sections/main-product.liquid` | USP cards |
| `reviews` | Review slider | `sections/main-product.liquid` | Testimonial carousel |
| `collapsible_tab` | Tab mở/đóng | `sections/main-product.liquid` | Shipping / FAQ / guarantee |
| `horizontal-ticker` | Dòng ticker chạy ngang | section/snippet tùy block | Banner chạy |
| `section-divider` | Dải ngăn section | section/snippet tùy block | Chia khối nội dung |
| `image-with-text` | Khối ảnh + text | section/snippet tùy block | Benefit section |
| `results` | Kết quả survey / social proof | section/snippet tùy block | Số liệu thuyết phục |
| `custom-columns` | Bố cục cột tùy biến | section/snippet tùy block | Layout dạng grid |
| `testimonials` | Khối testimonial | section/snippet tùy block | Review người dùng |
| `comparison-table` | Bảng so sánh | section/snippet tùy block | So sánh với đối thủ |
| `collapsible-content` | FAQ dạng accordion | section/snippet tùy block | Câu hỏi thường gặp |
| `image-slider` | Slider ảnh/video | section/snippet tùy block | Gallery marketing |
| `related-products` | Sản phẩm liên quan | `sections/main-product.liquid` | Cross-sell |

### Nhận xét nhanh
- `product.json` không chỉ chứa “product info” mà còn chứa **marketing blocks**.
- Nhiều block là **custom**, không phải block mặc định thuần Shopify.
- Đây là dấu hiệu theme đã được tailor cho landing/product page conversion.

---

## 9) Metafield / Metaobject đang dùng thật sự trong theme

### 9.1 Kết quả scan toàn theme
Mình scan toàn bộ `Default Theme` và tìm thấy các pattern metafield/metaobject sau:

| File | Dòng dùng | Key / path | Mục đích |
|---|---|---|---|
| `sections/main-product.liquid` | `product.metafields.reviews.rating.value` | `reviews.rating` | Lấy rating value để render sao và số review |
| `sections/main-product.liquid` | `product.metafields.reviews.rating_count` | `reviews.rating_count` | Lấy số lượt review |
| `snippets/card-product.liquid` | `card_product.metafields.reviews.rating.value` | `reviews.rating` | Hiển thị rating ở card sản phẩm |
| `snippets/card-product.liquid` | `card_product.metafields.reviews.rating_count` | `reviews.rating_count` | Hiển thị count ở card sản phẩm |
| `snippets/cjpod.liquid` | `product.metafields.productMetaField.sourceURL` | `productMetaField.sourceURL` | Gán source URL cho script CJPod |
| `snippets/gp-head.liquid` | `shop.metafields.GEMPAGES` | `GEMPAGES.*` | Lấy CSS / font / asset version của GemPages |
| nhiều `gp-section-*.liquid` | `shop.metafields.GEMPAGES.ASSETS_VERSION` | `GEMPAGES.ASSETS_VERSION` | Version hoá JS/CSS từ GemPages |

### 9.2 Metaobject
- Trong scan hiện tại, **chưa thấy metaobject reference rõ ràng** kiểu `metaobject`, `shop.metaobjects`, `product.metafields.namespace.value.reference`, hoặc `metaobject_reference`.
- Nói ngắn gọn: **theme đang dùng metafield là chính**, metaobject chưa thấy lộ diện trong phần scan này.

### 9.3 Kết luận về metafield/metaobject
**Có dùng thật.** Không phải chỉ là theme “thuần static”.

#### Dùng nhiều nhất:
1. `product.metafields.reviews.*`
2. `shop.metafields.GEMPAGES.*`
3. `product.metafields.productMetaField.sourceURL`

#### Chưa thấy:
- Metaobject mapping rõ ràng
- Schema định nghĩa metafield trong repo theme
- Cấu trúc namespace/key được document hoá sẵn cho team dev

---

## 10) Kết luận cập nhật

- **Chuỗi render** của theme là: `templates -> sections -> snippets -> assets`.
- **Product template** là khu vực custom mạnh nhất, có nhiều block marketing/conversion.
- **Metafield thật sự đang được dùng**, chủ yếu cho reviews, GemPages, và một custom source URL.
- **Metaobject chưa thấy** trong scan hiện tại.

---

## 11) Gợi ý bước tiếp theo

Nếu bạn muốn, mình có thể làm tiếp 1 file md nữa theo kiểu:
1. **Bản đồ metafield/metaobject chi tiết theo từng file và từng key**
2. **Cây phụ thuộc file-level đầy đủ cho toàn theme**
3. **Checklist kỹ thuật cho dev mới: file nào sửa khi cần đổi header, product, page, CTA, reviews**
