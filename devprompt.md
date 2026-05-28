#@@@
Mục tiêu: LẬP KẾ HOẠCH Sử dụng theme DefaultTheme ở shopify store jugjjq-1m.myshopify.com , thay thế nội dung cho sản phâm mới Utrasonic Oral Appliance Cleaner, brand: Orivati . 
Các hạng mục cần mapping thay thế:
- Trang Product
- 2 Trang Advertorial
- Trang HomePage
Tiêu chí, yêu cầu thay thế:
- GIữ vững layout, cấu trúc sourcecode chính
- Thay thế tiêu đề, tên, nội dung text, url hình ảnh, video, media minh họa phù hợp với sản phẩm và thương hiệu đích
- Thay thế UI elements: trust badges, icon brand related, Social Proof,... phù hợp với sản phẩm và thương hiệu đích
- URL path, slug SEO friendly
Tài liệu tham khảo:
- DefaultTheme : nơi chứa source code theme shopify DefaultTheme
- hientrangDefaultTheme : screenshot các trang hiện tại ở shopify store jugjjq-1m.myshopify.com
- page-product : GraphQL file template quá trình tạo trước đó
- ultrasonic-oral-appliance-cleaner-with-uv-c : thư mục chứa các nội dung sản phẩm đích Utrasonic Oral Appliance Cleaner của brand Orivati
    - Thông tin sản phẩm: ultrasonic-oral-appliance-cleaner-with-uv-c\2026-05-15__main\00_inputs\product-intake.md
    - Ad brief : ultrasonic-oral-appliance-cleaner-with-uv-c\2026-05-15__main\03_OL3_ad_briefs\OL3-ad-brief-angles.md
    - Nội dung của Page advertorial 1: ultrasonic-oral-appliance-cleaner-with-uv-c\2026-05-15__main\05_OL5_advertorials\AV01__authority-reveals-advertorial.md (Chưa bao gồm Hình ảnh, video minh họa. Chưa bao gồm đúng cấu trúc layout hoàn thiện của trang advertorial)
    - Nội dung của Page advertorial 2: ultrasonic-oral-appliance-cleaner-with-uv-c\2026-05-15__main\05_OL5_advertorials\AV03__caregiver-relief-advertorial.md (Chưa bao gồm Hình ảnh, video minh họa. Chưa bao gồm đúng cấu trúc layout hoàn thiện của trang advertorial)
- final-media : hình ảnh sản phẩm, thương hiệu final
    - final-media\customer-review : hình ảnh, video của khách hàng (customer's review media)
- scrapewaggier : các file gốc HTML, screenshot của trang waggier dùng để tham chiếu cấu trúc sourcecode gốc
    - scrapewaggier\waggier-advertorial-page.html
    - scrapewaggier\waggier-homepage.html
    - scrapewaggier\waggier-pacebowl-2-product.html
- index-map-default-theme.md : tài liệu index map của sourcecode DefaultTheme phân tích trước đó
- migrate-plan-actual.md : tài liệu kế hoạch migrate trước đó từ Waggier -> DefaultTheme hiện tại
- prompt1.md : tài liệu phân tích cấu trúc sourcecode DefaultTheme shopify trước đó

Kế hoạch thực hiện gợi ý:
- Thực hiện từng phase page by page lần lượt: từ Homepage -> product page -> advertorial page
- Thực hiện vòng lặp ở mỗi phase:
    - Trích xuất ở tham chiếu
    - Hiểu cấu trúc tương ứng ở theme shopify đích
    Lưu ý: đảm bảo căn cứ theo tham chiếu để mapping thay thế lần lượt 1:1 toàn diện:
        - Design tokens
        - Sections -> components -> elements
        - Text content (title, heading, tagline, body content,...)
        - Media URLs/assets (images, videos, badges, icons, logos...)
        - Layout
        - Functionality
    - Lập Index mapping , checklist
    - Sửa trực tiếp ở theme shopify đích
    - Shopify theme dev
    - Shopify theme push -> báo link preview
    - Đối với product, page -> shopify auth để xin cấp quyền cần thiết (dev hỗ trợ auth thủ công, nếu đã cấp quyền đủ 1 lượt trong 1 lần đầu, thì cứ thế mà thực hiện) -> dùng shopify cli push deploy (lưu ý: tạo dùng file graphql để push qua cli để tránh lỗi cú pháp)
    - Thực hiện sửa lỗi, fix bug trong từng bước nếu gặp phải
- Hoàn tất các vòng lặp đủ các phase
    - thực hiện việc kiểm tra, đánh giá
    - thực hiện việc tinh chỉnh, điều chỉnh
    - hoàn tất, báo cáo tổng kết
- Tactic: đối với media (ảnh, video, icon, logos,...) sẽ dùng URL của file tham chiếu gốc (sau này sẽ dùng hosting media riêng); không sử dụng upload file lên Shopify Files (Tức là:  thay shopify://shop_images/... → URL media assets trực tiếp) (⚠️ Lưu ý về media assets: Shopify's url type field trong block settings thường chỉ nhận /relative hoặc shopify:// paths. Nếu media vẫn không hiện, có thể dùng custom-liquid section để inject HTML trực tiếp)
