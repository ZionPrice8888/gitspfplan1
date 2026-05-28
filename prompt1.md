# SHOPIFY CUSTOM THEME - FULL PROJECT STRUCTURE

## Phân Tích Trước Khi Xây Dựng

Dựa trên phân tích 2 trang reference:
- **Product Sales Page (Calmbowl):** Hero video/image, trust badges, benefit blocks, before/after, testimonials, sticky ATC, quantity breaks, FAQ accordion, UGC gallery, comparison table
- **Advertorial Page:** Long-form editorial style, native ad feel, embedded product CTAs, story-driven layout, doctor/expert quotes, social proof blocks

---

## FULL FOLDER TREE

```
waggier-theme/
│
├── 📁 assets/
│   │
│   │── ── ── CSS FILES ── ── ──
│   │
│   ├── base.css
│   ├── reset.css
│   ├── typography.css
│   ├── variables.css
│   ├── utilities.css
│   ├── animations.css
│   │
│   ├── component-card.css
│   ├── component-badge.css
│   ├── component-button.css
│   ├── component-modal.css
│   ├── component-accordion.css
│   ├── component-slider.css
│   ├── component-drawer.css
│   ├── component-loading-overlay.css
│   ├── component-quantity-selector.css
│   ├── component-price.css
│   ├── component-rating-stars.css
│   ├── component-progress-bar.css
│   ├── component-countdown-timer.css
│   ├── component-sticky-bar.css
│   ├── component-announcement-bar.css
│   ├── component-tooltip.css
│   ├── component-video-player.css
│   │
│   ├── section-header.css
│   ├── section-footer.css
│   ├── section-hero-product.css
│   ├── section-product-info.css
│   ├── section-product-variant-picker.css
│   ├── section-quantity-breaks.css
│   ├── section-trust-badges.css
│   ├── section-benefit-blocks.css
│   ├── section-before-after.css
│   ├── section-comparison-table.css
│   ├── section-testimonials-carousel.css
│   ├── section-testimonials-grid.css
│   ├── section-ugc-gallery.css
│   ├── section-faq-accordion.css
│   ├── section-guarantee-banner.css
│   ├── section-sticky-add-to-cart.css
│   ├── section-social-proof-popup.css
│   ├── section-image-with-text.css
│   ├── section-rich-text.css
│   ├── section-featured-product.css
│   ├── section-video-hero.css
│   ├── section-ingredient-list.css
│   ├── section-how-it-works.css
│   ├── section-press-logos.css
│   ├── section-cart-drawer.css
│   ├── section-collection-list.css
│   │
│   ├── section-advertorial-hero.css
│   ├── section-advertorial-body.css
│   ├── section-advertorial-expert-quote.css
│   ├── section-advertorial-product-callout.css
│   ├── section-advertorial-inline-cta.css
│   ├── section-advertorial-social-proof.css
│   ├── section-advertorial-image-block.css
│   │
│   ├── template-product.css
│   ├── template-advertorial.css
│   ├── template-collection.css
│   ├── template-cart.css
│   ├── template-index.css
│   ├── template-page.css
│   ├── template-404.css
│   │
│   │── ── ── JAVASCRIPT FILES ── ── ──
│   │
│   ├── global.js
│   ├── pubsub.js
│   │
│   ├── product-form.js
│   ├── product-variant-picker.js
│   ├── product-image-gallery.js
│   ├── product-media.js
│   ├── quantity-selector.js
│   ├── quantity-breaks.js
│   ├── price-calculator.js
│   │
│   ├── sticky-add-to-cart.js
│   ├── cart-drawer.js
│   ├── cart-notification.js
│   ├── cart-items.js
│   │
│   ├── accordion.js
│   ├── slider-component.js
│   ├── testimonial-carousel.js
│   ├── modal-dialog.js
│   ├── drawer-component.js
│   ├── details-disclosure.js
│   ├── deferred-media.js
│   ├── video-player.js
│   ├── countdown-timer.js
│   ├── before-after-slider.js
│   ├── social-proof-popup.js
│   ├── announcement-bar.js
│   ├── smooth-scroll.js
│   ├── lazy-image.js
│   ├── intersection-observer.js
│   ├── scroll-animations.js
│   │
│   ├── advertorial-progress-bar.js
│   ├── advertorial-inline-cta.js
│   │
│   │── ── ── STATIC ASSETS ── ── ──
│   │
│   ├── favicon.ico
│   ├── logo.svg
│   ├── logo-white.svg
│   ├── placeholder-product.svg
│   ├── trust-badge-moneyback.svg
│   ├── trust-badge-shipping.svg
│   ├── trust-badge-secure.svg
│   ├── trust-badge-satisfaction.svg
│   ├── payment-icons-strip.svg
│   ├── star-filled.svg
│   ├── star-empty.svg
│   ├── icon-checkmark.svg
│   ├── icon-cross.svg
│   ├── icon-arrow-right.svg
│   ├── icon-arrow-left.svg
│   ├── icon-cart.svg
│   ├── icon-menu.svg
│   ├── icon-close.svg
│   ├── icon-play.svg
│   ├── icon-quote.svg
│   ├── icon-verified.svg
│   └── icon-spinner.svg
│
├── 📁 config/
│   ├── settings_schema.json
│   └── settings_data.json
│
├── 📁 layout/
│   ├── theme.liquid
│   ├── theme.advertorial.liquid
│   └── password.liquid
│
├── 📁 locales/
│   ├── en.default.json
│   └── en.default.schema.json
│
├── 📁 sections/
│   │
│   │── ── ── GLOBAL SECTIONS ── ── ──
│   │
│   ├── header.liquid
│   ├── header-minimal.liquid
│   ├── footer.liquid
│   ├── footer-minimal.liquid
│   ├── announcement-bar.liquid
│   ├── cart-drawer.liquid
│   ├── cart-notification.liquid
│   │
│   │── ── ── PRODUCT SALES PAGE SECTIONS ── ── ──
│   │
│   ├── main-product.liquid
│   ├── product-hero-media.liquid
│   ├── product-info-panel.liquid
│   ├── product-variant-picker.liquid
│   ├── product-quantity-breaks.liquid
│   ├── product-sticky-add-to-cart.liquid
│   ├── product-trust-badges.liquid
│   ├── product-benefit-icons.liquid
│   ├── product-benefit-blocks-detailed.liquid
│   ├── product-before-after.liquid
│   ├── product-comparison-table.liquid
│   ├── product-how-it-works.liquid
│   ├── product-ingredients.liquid
│   ├── product-testimonials-carousel.liquid
│   ├── product-testimonials-grid.liquid
│   ├── product-ugc-gallery.liquid
│   ├── product-faq-accordion.liquid
│   ├── product-guarantee-banner.liquid
│   ├── product-press-logos.liquid
│   ├── product-social-proof-popup.liquid
│   ├── product-video-testimonial.liquid
│   ├── product-vet-endorsed.liquid
│   │
│   │── ── ── ADVERTORIAL PAGE SECTIONS ── ── ──
│   │
│   ├── advertorial-hero.liquid
│   ├── advertorial-meta-bar.liquid
│   ├── advertorial-body-content.liquid
│   ├── advertorial-expert-quote.liquid
│   ├── advertorial-product-callout.liquid
│   ├── advertorial-inline-cta.liquid
│   ├── advertorial-image-block.liquid
│   ├── advertorial-social-proof-strip.liquid
│   ├── advertorial-before-after.liquid
│   ├── advertorial-related-articles.liquid
│   ├── advertorial-sticky-cta-bar.liquid
│   ├── advertorial-comment-section.liquid
│   │
│   │── ── ── SHARED / REUSABLE SECTIONS ── ── ──
│   │
│   ├── rich-text.liquid
│   ├── image-with-text.liquid
│   ├── video-section.liquid
│   ├── featured-product.liquid
│   ├── featured-collection.liquid
│   ├── collection-list.liquid
│   ├── multicolumn.liquid
│   ├── collapsible-content.liquid
│   ├── newsletter.liquid
│   ├── custom-liquid.liquid
│   ├── spacer.liquid
│   ├── divider.liquid
│   │
│   │── ── ── HOMEPAGE SECTIONS ── ── ──
│   │
│   ├── hero-banner.liquid
│   ├── collection-hero.liquid
│   │
│   │── ── ── OTHER PAGE SECTIONS ── ── ──
│   │
│   ├── main-collection.liquid
│   ├── main-cart.liquid
│   ├── main-page.liquid
│   ├── main-404.liquid
│   ├── main-blog.liquid
│   ├── main-article.liquid
│   ├── main-search.liquid
│   ├── main-list-collections.liquid
│   └── main-password-header.liquid
│
├── 📁 snippets/
│   │
│   │── ── ── CORE SNIPPETS ── ── ──
│   │
│   ├── head-meta-tags.liquid
│   ├── head-structured-data.liquid
│   ├── head-preload.liquid
│   ├── head-critical-css.liquid
│   ├── css-variables.liquid
│   ├── icons.liquid
│   ├── social-icons.liquid
│   │
│   │── ── ── PRODUCT SNIPPETS ── ── ──
│   │
│   ├── product-card.liquid
│   ├── product-media-image.liquid
│   ├── product-media-video.liquid
│   ├── product-media-gallery.liquid
│   ├── product-price.liquid
│   ├── product-compare-at-price.liquid
│   ├── product-badge-sale.liquid
│   ├── product-badge-bestseller.liquid
│   ├── product-variant-options.liquid
│   ├── product-buy-buttons.liquid
│   ├── product-quantity-input.liquid
│   ├── product-quantity-break-tier.liquid
│   ├── product-rating-stars.liquid
│   ├── product-review-count.liquid
│   ├── product-shipping-estimate.liquid
│   ├── product-stock-countdown.liquid
│   │
│   │── ── ── UI COMPONENT SNIPPETS ── ── ──
│   │
│   ├── button.liquid
│   ├── badge.liquid
│   ├── trust-badge-item.liquid
│   ├── testimonial-card.liquid
│   ├── testimonial-card-minimal.liquid
│   ├── benefit-icon-item.liquid
│   ├── before-after-item.liquid
│   ├── faq-item.liquid
│   ├── comparison-row.liquid
│   ├── ingredient-item.liquid
│   ├── step-item.liquid
│   ├── press-logo-item.liquid
│   ├── countdown-timer.liquid
│   ├── progress-bar.liquid
│   ├── loading-spinner.liquid
│   ├── image-lazy.liquid
│   ├── responsive-image.liquid
│   ├── video-embed.liquid
│   ├── modal-wrapper.liquid
│   │
│   │── ── ── ADVERTORIAL SNIPPETS ── ── ──
│   │
│   ├── advertorial-paragraph.liquid
│   ├── advertorial-pullquote.liquid
│   ├── advertorial-expert-card.liquid
│   ├── advertorial-cta-button.liquid
│   ├── advertorial-product-mini-card.liquid
│   ├── advertorial-fake-comment.liquid
│   ├── advertorial-source-citation.liquid
│   ├── advertorial-reading-progress.liquid
│   │
│   │── ── ── CART SNIPPETS ── ── ──
│   │
│   ├── cart-line-item.liquid
│   ├── cart-upsell-item.liquid
│   ├── cart-free-shipping-bar.liquid
│   ├── cart-discount-code.liquid
│   ├── cart-totals.liquid
│   │
│   │── ── ── UTILITY SNIPPETS ── ── ──
│   │
│   ├── json-ld-product.liquid
│   ├── json-ld-article.liquid
│   ├── json-ld-breadcrumb.liquid
│   ├── json-ld-organization.liquid
│   ├── pagination.liquid
│   ├── breadcrumbs.liquid
│   └── share-buttons.liquid
│
├── 📁 templates/
│   │
│   │── ── ── JSON TEMPLATES ── ── ──
│   │
│   ├── index.json
│   ├── product.json
│   ├── product.sales-page.json
│   ├── collection.json
│   ├── cart.json
│   ├── page.json
│   ├── page.advertorial.json
│   ├── page.contact.json
│   ├── page.about.json
│   ├── page.faq.json
│   ├── blog.json
│   ├── article.json
│   ├── search.json
│   ├── list-collections.json
│   ├── 404.json
│   ├── password.json
│   │
│   │── ── ── CUSTOMERS TEMPLATES ── ── ──
│   │
│   └── 📁 customers/
│       ├── account.json
│       ├── activate_account.json
│       ├── addresses.json
│       ├── login.json
│       ├── order.json
│       ├── register.json
│       └── reset_password.json
│
├── 📁 blocks/
│   │
│   │── ── ── PRODUCT BLOCKS (Theme Blocks) ── ── ──
│   │
│   ├── product-title.liquid
│   ├── product-price-block.liquid
│   ├── product-description.liquid
│   ├── product-variant-selector.liquid
│   ├── product-quantity-selector.liquid
│   ├── product-buy-button.liquid
│   ├── product-rating-block.liquid
│   ├── product-trust-strip.liquid
│   ├── product-shipping-info.liquid
│   ├── product-collapsible-tab.liquid
│   ├── product-custom-text.liquid
│   ├── product-icon-with-text.liquid
│   │
│   │── ── ── ADVERTORIAL BLOCKS ── ── ──
│   │
│   ├── advertorial-text-block.liquid
│   ├── advertorial-image-block.liquid
│   ├── advertorial-quote-block.liquid
│   ├── advertorial-cta-block.liquid
│   ├── advertorial-product-embed.liquid
│   ├── advertorial-divider-block.liquid
│   └── advertorial-highlight-box.liquid
│
└── 📁 dev-docs/
    ├── README.md
    ├── SECTIONS-MAP.md
    ├── STYLE-GUIDE.md
    └── DEPLOYMENT.md
```

---

## CHI TIẾT MÔ TẢ TỪNG FILE

---

### 📁 CONFIG/

#### `settings_schema.json`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Định nghĩa toàn bộ theme settings xuất hiện trong Theme Editor > Theme Settings |
| **Nội dung chính** | Các setting groups: Colors (primary, secondary, accent, sale, background), Typography (heading font, body font, sizes), Layout (container widths, spacing scale), Brand (logo, favicon), Social media links, Cart settings (drawer vs page, free shipping threshold), Trust badges global toggle, Announcement bar global settings, SEO defaults, Custom CSS injection field |
| **Liên kết** | Được đọc bởi `theme.liquid`, `css-variables.liquid`; values được lưu trong `settings_data.json` |

#### `settings_data.json`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Lưu trữ giá trị thực tế của tất cả theme settings và section configurations |
| **Nội dung chính** | Auto-generated bởi Theme Editor. Chứa current values cho mọi setting trong `settings_schema.json` và section arrangements cho từng template |
| **Liên kết** | Được generate từ `settings_schema.json`; source of truth cho toàn bộ theme customization |

---

### 📁 LAYOUT/

#### `theme.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Layout chính - wrapper cho TẤT CẢ pages (trừ advertorial). Chứa `<html>`, `<head>`, `<body>` tags |
| **Nội dung chính** | `<head>`: meta tags (snippet `head-meta-tags`), preload hints (snippet `head-preload`), critical CSS inline (snippet `head-critical-css`), CSS variables (snippet `css-variables`), base.css, global.js. `<body>`: render `header` section group, `{{ content_for_layout }}`, render `footer` section group, `cart-drawer` section, `social-proof-popup` section. Accessibility skip links, JSON-LD structured data snippets |
| **Liên kết** | Includes: `head-meta-tags.liquid`, `head-preload.liquid`, `head-critical-css.liquid`, `css-variables.liquid`, `json-ld-organization.liquid`. Renders sections: `header.liquid`, `footer.liquid`, `cart-drawer.liquid`, `announcement-bar.liquid` |

#### `theme.advertorial.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Layout riêng cho advertorial pages - minimal chrome, editorial feel, KHÔNG có navigation header chuẩn |
| **Nội dung chính** | `<head>`: same meta setup nhưng thêm advertorial-specific CSS. `<body>`: `header-minimal` (chỉ logo, không nav), `{{ content_for_layout }}`, `footer-minimal` (simplified), `advertorial-sticky-cta-bar`. Reading progress bar ở top. Không có cart drawer (CTA links trực tiếp đến product page hoặc checkout). Body class `template-advertorial` cho scoped styling |
| **Liên kết** | Includes: `head-meta-tags.liquid`, `css-variables.liquid`, `advertorial-reading-progress.liquid`. Renders: `header-minimal.liquid`, `footer-minimal.liquid`, `advertorial-sticky-cta-bar.liquid` |

#### `password.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Layout cho password-protected storefront (pre-launch) |
| **Nội dung chính** | Minimal layout với logo, password form, newsletter signup option |
| **Liên kết** | Renders: `main-password-header.liquid` |

---

### 📁 TEMPLATES/

#### `index.json`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Homepage template |
| **Sections mặc định** | `hero-banner`, `press-logos`, `featured-product` (Calmbowl), `product-benefit-blocks-detailed`, `product-testimonials-carousel`, `product-before-after`, `featured-collection`, `newsletter` |
| **Layout** | `theme.liquid` |

#### `product.json`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Template product mặc định - standard layout |
| **Sections mặc định** | `main-product` (chứa media gallery + product info blocks), `product-trust-badges`, `rich-text` (description expanded), `product-testimonials-grid`, `product-faq-accordion`, `featured-collection` |
| **Layout** | `theme.liquid` |

#### ⭐ `product.sales-page.json`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | **TEMPLATE CHÍNH** - Long-form product sales page giống Calmbowl. Template alternate cho product, được assign qua admin |
| **Sections theo thứ tự** | 1. `product-hero-media` (full-width hero image/video), 2. `product-info-panel` (title, rating, price, variant picker, quantity breaks, ATC), 3. `product-trust-badges`, 4. `product-benefit-icons` (icon row), 5. `product-benefit-blocks-detailed` (image + text alternating blocks), 6. `product-how-it-works` (numbered steps), 7. `product-before-after` (slider comparison), 8. `product-ingredients`, 9. `product-comparison-table` (us vs them), 10. `product-vet-endorsed`, 11. `product-testimonials-carousel`, 12. `product-ugc-gallery`, 13. `product-video-testimonial`, 14. `product-guarantee-banner`, 15. `product-faq-accordion`, 16. `product-press-logos`, 17. `featured-product` (final CTA block), 18. `product-sticky-add-to-cart`, 19. `product-social-proof-popup` |
| **Layout** | `theme.liquid` |

#### ⭐ `page.advertorial.json`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | **TEMPLATE ADVERTORIAL** - Long-form editorial/native ad page giống "Dog Owner Exposes Hidden Truth". Dùng alternate layout |
| **Layout** | `theme.advertorial.liquid` (NOT default theme.liquid) |
| **Sections theo thứ tự** | 1. `advertorial-hero` (editorial headline, featured image, author/date), 2. `advertorial-meta-bar` (publication name, reading time, share), 3. `advertorial-body-content` (main article body với nested blocks), 4. `advertorial-expert-quote` (doctor/vet quote callout), 5. `advertorial-image-block` (inline editorial images), 6. `advertorial-product-callout` (product feature box mid-article), 7. `advertorial-inline-cta` (CTA button trong article flow), 8. `advertorial-before-after`, 9. `advertorial-social-proof-strip` (mini testimonials), 10. `advertorial-product-callout` (repeat - bottom), 11. `advertorial-inline-cta` (repeat - final CTA), 12. `advertorial-comment-section` (social proof fake comments), 13. `advertorial-related-articles` |

#### `collection.json`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Collection page template |
| **Sections** | `collection-hero`, `main-collection` (product grid), `newsletter` |
| **Layout** | `theme.liquid` |

#### `cart.json`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Full cart page (fallback khi cart drawer disabled) |
| **Sections** | `main-cart` (line items, upsells, totals, checkout button, free shipping bar) |
| **Layout** | `theme.liquid` |

#### `page.json` / `page.contact.json` / `page.about.json` / `page.faq.json`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Standard page templates và alternates cho specific page types |
| **Layout** | `theme.liquid` |

#### `blog.json` / `article.json`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Blog listing và individual article pages |
| **Layout** | `theme.liquid` |

#### `search.json` / `list-collections.json` / `404.json` / `password.json`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Utility pages |
| **Layout** | `theme.liquid` (password uses `password.liquid`) |

---

### 📁 SECTIONS/ - CHI TIẾT

---

#### GLOBAL SECTIONS

##### `header.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Navigation header chính cho toàn site |
| **Thành phần** | Logo (linked to homepage), main navigation menu (configurable via schema), mobile hamburger menu trigger, cart icon với item count badge, optional promotional text, mobile slide-out drawer navigation |
| **Schema settings** | Logo image, logo width, menu handle, sticky header toggle, background color, text color, show announcement toggle |
| **CSS** | `section-header.css` |
| **JS** | Part of `global.js` for mobile menu, `drawer-component.js` |
| **Liên kết** | Snippets: `icons.liquid` (cart, menu, close icons) |

##### `header-minimal.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Stripped-down header cho advertorial layout - chỉ logo centered, không navigation |
| **Thành phần** | Centered logo only, optional "Back to site" text link, thin bottom border |
| **Schema settings** | Logo image, background color, show back link toggle |
| **CSS** | `section-header.css` (shared, scoped classes) |
| **Liên kết** | Used exclusively by `theme.advertorial.liquid` |

##### `footer.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Full site footer |
| **Thành phần** | Multi-column layout: menu links, about text, newsletter signup, social media icons, payment icons, copyright, legal links (privacy, terms, refund) |
| **Schema settings** | Column blocks (menu, text, newsletter), social links, payment icons toggle, background/text colors |
| **CSS** | `section-footer.css` |
| **Liên kết** | Snippets: `social-icons.liquid`, `newsletter` form logic |

##### `footer-minimal.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Minimal footer cho advertorial pages |
| **Thành phần** | Single line: copyright, privacy link, terms link. Nhỏ gọn, không distract |
| **Schema settings** | Text color, background color, legal page links |
| **CSS** | `section-footer.css` (shared, scoped) |
| **Liên kết** | Used by `theme.advertorial.liquid` |

##### `announcement-bar.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Top-of-page promotional banner |
| **Thành phần** | Scrolling or static text, optional countdown timer, dismissible (cookie-based), optional link |
| **Schema settings** | Text content, background color, text color, link URL, show countdown, countdown end date, auto-rotate multiple messages |
| **CSS** | `component-announcement-bar.css` |
| **JS** | `announcement-bar.js`, optionally `countdown-timer.js` |

##### `cart-drawer.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Slide-out cart drawer (AJAX cart) |
| **Thành phần** | Cart header with item count, line items list, free shipping progress bar, upsell product suggestions, discount code input, subtotal, checkout button, continue shopping link |
| **Schema settings** | Free shipping threshold, upsell collection handle, empty cart message |
| **CSS** | `section-cart-drawer.css`, `component-drawer.css` |
| **JS** | `cart-drawer.js`, `cart-items.js` |
| **Liên kết** | Snippets: `cart-line-item.liquid`, `cart-upsell-item.liquid`, `cart-free-shipping-bar.liquid`, `cart-totals.liquid` |

##### `cart-notification.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Toast/popup notification khi item added to cart |
| **Thành phần** | Product thumbnail, product title, "Added to cart" message, view cart button, continue shopping button |
| **JS** | `cart-notification.js` |

---

#### PRODUCT SALES PAGE SECTIONS

##### `main-product.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Standard product section (for `product.json` default template) - 2-column layout |
| **Thành phần** | Left: product media gallery. Right: product info (rendered via blocks). Sử dụng theme blocks architecture cho flexible ordering |
| **Schema blocks** | `product-title`, `product-price-block`, `product-rating-block`, `product-variant-selector`, `product-quantity-selector`, `product-buy-button`, `product-description`, `product-trust-strip`, `product-collapsible-tab`, `product-shipping-info`, `product-icon-with-text`, `product-custom-text` |
| **Schema settings** | Media gallery position (left/right), enable zoom, enable video autoplay, container width |
| **CSS** | `section-product-info.css`, `template-product.css` |
| **JS** | `product-form.js`, `product-variant-picker.js`, `product-image-gallery.js` |
| **Liên kết** | Snippets: `product-media-gallery.liquid`, `product-price.liquid`, `product-buy-buttons.liquid`, `product-variant-options.liquid`, `product-rating-stars.liquid`. Blocks from `blocks/` folder |

##### ⭐ `product-hero-media.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Full-width hero section ở top của sales page - first impression |
| **Thành phần** | Full-width product image hoặc autoplay video, optional overlay text (headline + subheadline), optional CTA button scroll-to-buy, mobile-optimized aspect ratio |
| **Schema settings** | Desktop image, mobile image, video URL (YouTube/Vimeo/hosted), overlay text, overlay position, overlay color, CTA text, CTA target section ID, aspect ratio (desktop/mobile), enable parallax |
| **CSS** | `section-hero-product.css` |
| **JS** | `deferred-media.js`, `video-player.js` |
| **Liên kết** | Snippets: `responsive-image.liquid`, `video-embed.liquid` |

##### ⭐ `product-info-panel.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Main product info + purchase section trên sales page (tương tự phần buy box của Calmbowl) |
| **Thành phần** | Product title (H1), star rating + review count, price display (compare-at + sale price), savings badge ("Save 40%"), variant picker (if applicable), quantity break tiers (integrated hoặc link to separate section), Add to Cart button (large, prominent), trust badges strip dưới ATC, payment icons, shipping estimate text, stock countdown ("Only X left!") |
| **Schema settings** | Show rating, show compare price, show savings badge, show stock countdown, stock countdown threshold, show payment icons, ATC button text, ATC button color, enable quantity breaks (inline vs separate section) |
| **CSS** | `section-product-info.css`, `component-price.css`, `component-button.css`, `component-quantity-selector.css` |
| **JS** | `product-form.js`, `product-variant-picker.js`, `quantity-breaks.js`, `price-calculator.js` |
| **Liên kết** | Snippets: `product-price.liquid`, `product-compare-at-price.liquid`, `product-rating-stars.liquid`, `product-review-count.liquid`, `product-buy-buttons.liquid`, `product-quantity-input.liquid`, `product-quantity-break-tier.liquid`, `product-badge-sale.liquid`, `product-stock-countdown.liquid`, `product-shipping-estimate.liquid`, `trust-badge-item.liquid` |

##### ⭐ `product-quantity-breaks.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Standalone quantity break / bundle pricing section (1x, 2x, 3x options as cards) |
| **Thành phần** | Heading ("Choose Your Bundle"), tier cards (each showing: quantity, per-unit price, total price, savings amount, savings percentage, optional "Most Popular" badge), visual selection state, auto-update cart quantity on selection |
| **Schema settings** | Heading text, tier blocks (each: quantity, label, badge text, highlight toggle), background color, card style |
| **CSS** | `section-quantity-breaks.css` |
| **JS** | `quantity-breaks.js`, `price-calculator.js` |
| **Liên kết** | Snippets: `product-quantity-break-tier.liquid` |

##### `product-sticky-add-to-cart.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Fixed bottom bar hiện khi main ATC button scrolls out of view |
| **Thành phần** | Product thumbnail (small), product title (truncated), price, ATC button, variant selector (simplified dropdown if multiple variants). Slides in/out with animation |
| **Schema settings** | Show on mobile, show on desktop, background color, button color |
| **CSS** | `section-sticky-add-to-cart.css`, `component-sticky-bar.css` |
| **JS** | `sticky-add-to-cart.js` (intersection observer on main ATC button) |
| **Liên kết** | Snippets: `product-price.liquid` |

##### `product-trust-badges.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Horizontal strip of trust/guarantee badges |
| **Thành phần** | Icon + label pairs: "30-Day Money Back", "Free Shipping", "Vet Approved", "Made in USA", etc. Responsive: wraps to 2x2 grid on mobile |
| **Schema settings** | Badge blocks (each: icon image/SVG, title text, subtitle text), columns per row, alignment, background color |
| **CSS** | `section-trust-badges.css`, `component-badge.css` |
| **Liên kết** | Snippets: `trust-badge-item.liquid` |

##### `product-benefit-icons.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Compact row of benefit icons với short labels (quick scan section) |
| **Thành phần** | 4-6 icons in a row: "Calming", "Non-Toxic", "Easy Clean", "Vet Approved" etc. Each: icon + 2-3 word label |
| **Schema settings** | Icon blocks (each: icon image, label), background color, icon size |
| **CSS** | `section-benefit-blocks.css` |
| **Liên kết** | Snippets: `benefit-icon-item.liquid` |

##### ⭐ `product-benefit-blocks-detailed.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Alternating image + text blocks explaining each product benefit in detail |
| **Thành phần** | Each block: large image on one side, heading + paragraph + optional bullet points on other side. Alternating left/right layout. Optional icon above heading. Scroll animation on enter |
| **Schema settings** | Blocks (each: image, heading, body text, bullet points, image position left/right, optional icon, optional CTA button), section heading, background alternating colors |
| **CSS** | `section-benefit-blocks.css`, `section-image-with-text.css` |
| **JS** | `scroll-animations.js` |

##### `product-before-after.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Before/After comparison slider hoặc side-by-side images |
| **Thành phần** | Section heading, before/after image pairs (draggable slider or side-by-side), before/after labels, optional caption per pair. Support multiple pairs as blocks |
| **Schema settings** | Heading, display mode (slider/side-by-side), pair blocks (each: before image, after image, before label, after label, caption) |
| **CSS** | `section-before-after.css` |
| **JS** | `before-after-slider.js` |
| **Liên kết** | Snippets: `before-after-item.liquid` |

##### ⭐ `product-comparison-table.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | "Us vs. Them" comparison table |
| **Thành phần** | Section heading, two-column table: our product vs competitors. Rows with checkmark/cross icons. Our column highlighted. Optional "Why We're Different" subheading |
| **Schema settings** | Heading, our product column label, competitor column label, row blocks (each: feature text, our product has it Y/N, competitor has it Y/N), highlight color |
| **CSS** | `section-comparison-table.css` |
| **Liên kết** | Snippets: `comparison-row.liquid`, `icons.liquid` (checkmark, cross) |

##### `product-how-it-works.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Numbered steps explaining how to use the product |
| **Thành phần** | Section heading, 3-4 step cards (each: step number, icon/image, title, description), visual connector line between steps |
| **Schema settings** | Heading, step blocks (each: icon/image, title, description), layout (horizontal/vertical), connector style |
| **CSS** | `section-how-it-works.css` |
| **Liên kết** | Snippets: `step-item.liquid` |

##### `product-ingredients.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Ingredient list with benefits explanation |
| **Thành phần** | Section heading, ingredient cards/list (each: ingredient name, image, benefit description, optional "clinically proven" badge) |
| **Schema settings** | Heading, subheading, ingredient blocks (each: name, image, description, badge text), layout (grid/list) |
| **CSS** | `section-ingredient-list.css` |
| **Liên kết** | Snippets: `ingredient-item.liquid` |

##### ⭐ `product-testimonials-carousel.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Rotating testimonial carousel - high social proof impact |
| **Thành phần** | Section heading + overall rating summary, carousel of testimonial cards (each: star rating, review text, reviewer name, reviewer photo, verified badge, optional product photo), navigation arrows, dot indicators, auto-play option |
| **Schema settings** | Heading, overall rating number, total review count, auto-play speed, testimonial blocks (each: stars 1-5, text, name, photo, verified toggle, product image), show navigation arrows, slides per view (desktop/mobile) |
| **CSS** | `section-testimonials-carousel.css`, `component-slider.css`, `component-rating-stars.css` |
| **JS** | `testimonial-carousel.js`, `slider-component.js` |
| **Liên kết** | Snippets: `testimonial-card.liquid`, `product-rating-stars.liquid` |

##### `product-testimonials-grid.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Static grid of testimonials (alternative to carousel) |
| **Thành phần** | Masonry or uniform grid of testimonial cards, "Load more" button optional |
| **Schema settings** | Heading, columns (2/3/4), testimonial blocks, show load more |
| **CSS** | `section-testimonials-grid.css` |
| **Liên kết** | Snippets: `testimonial-card.liquid` |

##### `product-ugc-gallery.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | User-generated content photo gallery (Instagram-style grid) |
| **Thành phần** | Section heading, photo grid (clickable to lightbox), optional @username overlay on each photo |
| **Schema settings** | Heading, image blocks (each: image, username, optional caption), columns, gap size, enable lightbox |
| **CSS** | `section-ugc-gallery.css` |
| **JS** | `modal-dialog.js` (for lightbox) |

##### `product-faq-accordion.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | FAQ section with expandable/collapsible questions |
| **Thành phần** | Section heading, accordion items (question/answer pairs), optional "Contact us" CTA at bottom, optional schema.org FAQ structured data output |
| **Schema settings** | Heading, FAQ blocks (each: question, answer rich text), show contact link, contact page URL |
| **CSS** | `section-faq-accordion.css`, `component-accordion.css` |
| **JS** | `accordion.js` |
| **Liên kết** | Snippets: `faq-item.liquid` |

##### `product-guarantee-banner.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Money-back guarantee / risk reversal banner |
| **Thành phần** | Guarantee badge icon, heading ("100% Money-Back Guarantee"), description text, optional CTA button |
| **Schema settings** | Icon image, heading, body text, background color, text color, CTA text, CTA URL |
| **CSS** | `section-guarantee-banner.css` |

##### `product-press-logos.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | "As Seen In" press/media logo strip |
| **Thành phần** | Section heading ("As Featured In"), horizontal row of grayscale logos, optional hover color effect |
| **Schema settings** | Heading, logo blocks (each: logo image, alt text, optional link URL), grayscale toggle |
| **CSS** | `section-press-logos.css` |
| **Liên kết** | Snippets: `press-logo-item.liquid` |

##### `product-social-proof-popup.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | "Someone in [City] just purchased" popup notifications |
| **Thành phần** | Small toast notification, product thumbnail, buyer first name + city, "X minutes ago" timestamp, auto-rotate through entries, slide in/out animation |
| **Schema settings** | Enable/disable, display interval, display duration, notification blocks (each: name, city, time ago), position (bottom-left/bottom-right) |
| **CSS** | `section-social-proof-popup.css` |
| **JS** | `social-proof-popup.js` |

##### `product-video-testimonial.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Video testimonial section (embedded videos from customers) |
| **Thành phần** | Section heading, video grid or carousel, each video with thumbnail, play button overlay, reviewer name |
| **Schema settings** | Heading, video blocks (each: video URL, thumbnail image, reviewer name, title) |
| **CSS** | `component-video-player.css` |
| **JS** | `deferred-media.js`, `video-player.js` |

##### `product-vet-endorsed.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Expert endorsement section (vet/doctor recommendation) |
| **Thành phần** | Expert photo, name, credentials, quote, optional clinic/organization name, endorsement badge |
| **Schema settings** | Expert photo, name, title/credentials, quote text, organization, badge image |
| **CSS** | `section-image-with-text.css` (reused with modifier class) |

---

#### ADVERTORIAL PAGE SECTIONS

##### ⭐ `advertorial-hero.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Editorial-style hero section - looks like a news article header |
| **Thành phần** | Category tag ("PET HEALTH"), large editorial headline (H1), subtitle/deck, featured hero image (full-width, editorial photography style), image caption, author name + avatar, publish date, estimated reading time |
| **Schema settings** | Category tag text, headline, subtitle, hero image, image caption, author name, author avatar image, publish date, reading time, tag color |
| **CSS** | `section-advertorial-hero.css` |

##### `advertorial-meta-bar.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Thin meta information bar below hero - adds editorial credibility |
| **Thành phần** | Publication name / source (e.g., "Pet Health Daily"), share buttons (Facebook, Twitter, Email, Copy link), reading progress indicator (thin bar), optional "Advertorial" disclosure tag (small, subtle) |
| **Schema settings** | Publication name, show share buttons, show disclosure, disclosure text |
| **CSS** | `section-advertorial-hero.css` (combined) |
| **JS** | `advertorial-progress-bar.js` |
| **Liên kết** | Snippets: `share-buttons.liquid`, `advertorial-reading-progress.liquid` |

##### ⭐ `advertorial-body-content.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | **CORE SECTION** - Main article body content. Uses block architecture for flexible editorial content layout |
| **Thành phần** | Narrow-width content column (editorial reading width ~680px), renders sequence of blocks in order. Each block type creates a different content element within the article flow |
| **Schema blocks** | `advertorial-text-block` (rich text paragraph), `advertorial-image-block` (inline image with caption), `advertorial-quote-block` (pullquote/blockquote), `advertorial-cta-block` (inline CTA button), `advertorial-product-embed` (mini product card inline), `advertorial-divider-block` (visual separator), `advertorial-highlight-box` (highlighted text box/callout) |
| **Schema settings** | Content max-width, body font size, paragraph spacing, link color |
| **CSS** | `section-advertorial-body.css` |
| **Liên kết** | All advertorial blocks from `blocks/` folder |

##### `advertorial-expert-quote.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Prominent expert/doctor quote callout - breaks up article body |
| **Thành phần** | Large quotation marks icon, quote text (large font), expert name, credentials/title, expert photo, optional organization |
| **Schema settings** | Quote text, expert name, credentials, photo, organization, background color, quote style (boxed/open) |
| **CSS** | `section-advertorial-expert-quote.css` |
| **Liên kết** | Snippets: `advertorial-expert-card.liquid`, `advertorial-pullquote.liquid` |

##### ⭐ `advertorial-product-callout.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Product feature box embedded in article - primary conversion point. Styled to feel editorial but clearly showcases the product |
| **Thành phần** | Product image (editorial style, not standard product photo), product name, key benefits list (3-5 bullet points with checkmarks), star rating + review count, price (with compare-at), prominent CTA button ("Shop Now" / "Get Yours"), optional limited-time offer text, trust badges mini strip |
| **Schema settings** | Product handle (product picker), heading override, benefits list (text blocks), CTA text, CTA URL, show price, show rating, show trust badges, urgency text, background color, border style |
| **CSS** | `section-advertorial-product-callout.css` |
| **JS** | `advertorial-inline-cta.js` |
| **Liên kết** | Snippets: `advertorial-product-mini-card.liquid`, `product-rating-stars.liquid`, `advertorial-cta-button.liquid`, `trust-badge-item.liquid` |

##### `advertorial-inline-cta.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Simple inline CTA button within article flow |
| **Thành phần** | CTA button (full-width or centered), optional urgency text above, optional guarantee text below |
| **Schema settings** | Button text, button URL, button style (primary/secondary), urgency text, sub-text, alignment |
| **CSS** | `section-advertorial-inline-cta.css` |
| **JS** | `advertorial-inline-cta.js` |
| **Liên kết** | Snippets: `advertorial-cta-button.liquid` |

##### `advertorial-image-block.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Full-width or content-width image within article with editorial caption |
| **Thành phần** | Image (responsive), caption text, optional credit line |
| **Schema settings** | Image, caption, credit, width (content/full/wide), alt text |
| **CSS** | `section-advertorial-image-block.css` |
| **Liên kết** | Snippets: `responsive-image.liquid` |

##### `advertorial-social-proof-strip.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Compact testimonials strip within article - quick social proof |
| **Thành phần** | 2-3 mini testimonials in a row (each: quote snippet, name, star rating), overall stats ("10,000+ happy dogs") |
| **Schema settings** | Heading, stat text, testimonial blocks (each: short quote, name, rating), background color |
| **CSS** | `section-advertorial-social-proof.css` |
| **Liên kết** | Snippets: `testimonial-card-minimal.liquid`, `product-rating-stars.liquid` |

##### `advertorial-before-after.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Before/after trong context editorial (reuses same visual pattern nhưng editorial styling) |
| **Thành phần** | Same as `product-before-after` nhưng styled to match advertorial typography và width |
| **Schema settings** | Same as product version + editorial caption option |
| **CSS** | `section-before-after.css`, `section-advertorial-body.css` (overrides) |
| **JS** | `before-after-slider.js` |

##### `advertorial-comment-section.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Fake comment section for social proof (common advertorial pattern) |
| **Thành phần** | "Comments (XX)" heading, comment list (each: avatar, name, timestamp, comment text, like count, optional reply), load more button |
| **Schema settings** | Comment count display, comment blocks (each: name, avatar, time ago, comment text, likes count), show load more |
| **CSS** | `section-advertorial-social-proof.css` |
| **Liên kết** | Snippets: `advertorial-fake-comment.liquid` |

##### `advertorial-related-articles.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | "Related articles" section at bottom - encourages trust and looks editorial |
| **Thành phần** | 2-3 article cards (thumbnail, title, excerpt), optional: some link to real blog posts, some to other advertorials |
| **Schema settings** | Heading, article blocks (each: image, title, excerpt, URL), columns |
| **CSS** | `section-advertorial-body.css` (reused) |

##### `advertorial-sticky-cta-bar.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Fixed bottom CTA bar on advertorial page - always visible after scroll |
| **Thành phần** | Product name (short), price, CTA button, appears after scrolling past first screen |
| **Schema settings** | Button text, button URL, product title short, show price, background color, button color |
| **CSS** | `section-advertorial-inline-cta.css` (shared), `component-sticky-bar.css` |
| **JS** | `advertorial-inline-cta.js` |

---

#### SHARED / REUSABLE SECTIONS

##### `rich-text.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | General rich text content section |
| **Schema settings** | Heading, body text (rich text), alignment, narrow/full width, background color |
| **CSS** | `section-rich-text.css` |

##### `image-with-text.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Two-column image + text section (reusable across many templates) |
| **Schema settings** | Image, heading, body text, CTA button, image position (left/right), layout ratio, background color, content alignment |
| **CSS** | `section-image-with-text.css` |

##### `video-section.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Standalone video embed section |
| **Schema settings** | Heading, video URL, cover image, autoplay, aspect ratio |
| **CSS** | `component-video-player.css` |
| **JS** | `deferred-media.js`, `video-player.js` |

##### `featured-product.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Feature a single product as a CTA section (used at bottom of sales page as final push) |
| **Schema settings** | Product picker, heading override, show price, show ATC button, background color |
| **CSS** | `section-featured-product.css` |
| **JS** | `product-form.js` |

##### `featured-collection.liquid` / `collection-list.liquid` / `multicolumn.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Standard Dawn sections for homepage and collection pages |

##### `collapsible-content.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Generic collapsible/accordion content (used for policies, general FAQ) |
| **CSS** | `component-accordion.css` |
| **JS** | `accordion.js` |

##### `newsletter.liquid` / `custom-liquid.liquid` / `spacer.liquid` / `divider.liquid`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Utility sections for layout control and custom code injection |

---

### 📁 BLOCKS/ - CHI TIẾT

#### Product Blocks (used inside `main-product.liquid`)

| Block file | Mục đích |
|---|---|
| `product-title.liquid` | Product title (H1) with optional subtitle |
| `product-price-block.liquid` | Price display with compare-at, sale badge, savings calculator |
| `product-description.liquid` | Product description (rich text from product metafield or description) |
| `product-variant-selector.liquid` | Variant picker (swatches, dropdowns, or buttons) |
| `product-quantity-selector.liquid` | Quantity +/- input |
| `product-buy-button.liquid` | Add to Cart + Buy Now buttons |
| `product-rating-block.liquid` | Star rating + review count display |
| `product-trust-strip.liquid` | Inline trust badges row (compact, within buy box) |
| `product-shipping-info.liquid` | Shipping estimate text ("Free shipping • Arrives in 3-5 days") |
| `product-collapsible-tab.liquid` | Collapsible tab (Details, Shipping, Returns, etc.) |
| `product-custom-text.liquid` | Custom text block (for promotional messages) |
| `product-icon-with-text.liquid` | Small icon + text pair (for inline features) |

#### Advertorial Blocks (used inside `advertorial-body-content.liquid`)

| Block file | Mục đích |
|---|---|
| `advertorial-text-block.liquid` | Rich text paragraph block (main article content) |
| `advertorial-image-block.liquid` | Inline image with caption |
| `advertorial-quote-block.liquid` | Pullquote / blockquote styling |
| `advertorial-cta-block.liquid` | CTA button inline |
| `advertorial-product-embed.liquid` | Mini product card embedded in article flow |
| `advertorial-divider-block.liquid` | Visual divider (line, space, decorative) |
| `advertorial-highlight-box.liquid` | Highlighted text box / callout box |

---

### 📁 SNIPPETS/ - CHI TIẾT

#### Core Snippets

| Snippet | Mục đích | Used by |
|---|---|---|
| `head-meta-tags.liquid` | All `<meta>` tags: charset, viewport, description, OG tags, Twitter cards, canonical URL | `theme.liquid`, `theme.advertorial.liquid` |
| `head-structured-data.liquid` | Conditional inclusion of JSON-LD snippets based on template | `theme.liquid` |
| `head-preload.liquid` | `<link rel="preload">` for critical fonts, hero images, CSS | `theme.liquid` |
| `head-critical-css.liquid` | Inline critical CSS for above-the-fold rendering | `theme.liquid` |
| `css-variables.liquid` | CSS custom properties generated from theme settings (colors, fonts, spacing) | `theme.liquid`, `theme.advertorial.liquid` |
| `icons.liquid` | SVG icon sprite/symbol system. Render specific icons by name | Throughout all sections |
| `social-icons.liquid` | Social media icon links (Facebook, Instagram, TikTok, etc.) | `footer.liquid` |

#### Product Snippets

| Snippet | Mục đích | Used by |
|---|---|---|
| `product-card.liquid` | Product card component (image, title, price, badge) for grids | `featured-collection.liquid`, `main-collection.liquid` |
| `product-media-image.liquid` | Single product image with zoom capability | `product-media-gallery.liquid` |
| `product-media-video.liquid` | Product video with play/pause controls | `product-media-gallery.liquid` |
| `product-media-gallery.liquid` | Full media gallery (thumbnails + main image) | `main-product.liquid`, `product-hero-media.liquid` |
| `product-price.liquid` | Price display component (handles multi-currency, compare-at) | Multiple product sections |
| `product-compare-at-price.liquid` | Strikethrough compare-at price | `product-price.liquid` |
| `product-badge-sale.liquid` | "SALE" or "Save X%" badge | Product sections |
| `product-badge-bestseller.liquid` | "BESTSELLER" badge | Product sections |
| `product-variant-options.liquid` | Variant option rendering (swatch, button, dropdown) | `product-variant-picker.liquid`, `main-product.liquid` |
| `product-buy-buttons.liquid` | ATC + dynamic checkout button group | Product sections |
| `product-quantity-input.liquid` | Quantity +/- input field | Product sections |
| `product-quantity-break-tier.liquid` | Single quantity break tier card | `product-quantity-breaks.liquid`, `product-info-panel.liquid` |
| `product-rating-stars.liquid` | Star rating display (filled/empty stars) | Multiple sections |
| `product-review-count.liquid` | "(XXX Reviews)" text link | Product sections |
| `product-shipping-estimate.liquid` | "Free Shipping • Arrives by [date]" | Product sections |
| `product-stock-countdown.liquid` | "Only X left in stock!" urgency element | `product-info-panel.liquid` |

#### UI Component Snippets

| Snippet | Mục đích | Used by |
|---|---|---|
| `button.liquid` | Reusable button component with variants (primary, secondary, outline, sizes) | Throughout |
| `badge.liquid` | Generic badge component | Throughout |
| `trust-badge-item.liquid` | Single trust badge (icon + text) | `product-trust-badges.liquid`, `product-info-panel.liquid` |
| `testimonial-card.liquid` | Full testimonial card (photo, stars, text, name, verified) | Testimonial sections |
| `testimonial-card-minimal.liquid` | Compact testimonial (text + name only) | `advertorial-social-proof-strip.liquid` |
| `benefit-icon-item.liquid` | Single benefit icon + label | `product-benefit-icons.liquid` |
| `before-after-item.liquid` | Single before/after image pair | Before/after sections |
| `faq-item.liquid` | Single FAQ accordion item (question + answer) | `product-faq-accordion.liquid` |
| `comparison-row.liquid` | Single row in comparison table | `product-comparison-table.liquid` |
| `ingredient-item.liquid` | Single ingredient card | `product-ingredients.liquid` |
| `step-item.liquid` | Single how-it-works step | `product-how-it-works.liquid` |
| `press-logo-item.liquid` | Single press/media logo | `product-press-logos.liquid` |
| `countdown-timer.liquid` | Countdown timer component | Announcement bar, product sections |
| `progress-bar.liquid` | Progress bar component (free shipping, reading progress) | Cart, advertorial |
| `loading-spinner.liquid` | Loading spinner animation | Throughout |
| `image-lazy.liquid` | Lazy-loaded image with placeholder | Throughout |
| `responsive-image.liquid` | `<picture>` element with srcset for responsive images | Throughout |
| `video-embed.liquid` | Video embed wrapper (YouTube, Vimeo, hosted) | Video sections |
| `modal-wrapper.liquid` | Reusable modal dialog wrapper | Throughout |

#### Advertorial Snippets

| Snippet | Mục đích | Used by |
|---|---|---|
| `advertorial-paragraph.liquid` | Styled paragraph with editorial typography | `advertorial-body-content.liquid` |
| `advertorial-pullquote.liquid` | Large pullquote with quotation marks | `advertorial-expert-quote.liquid`, `advertorial-body-content.liquid` |
| `advertorial-expert-card.liquid` | Expert info card (photo, name, credentials) | `advertorial-expert-quote.liquid` |
| `advertorial-cta-button.liquid` | CTA button styled for editorial context | Advertorial CTA sections |
| `advertorial-product-mini-card.liquid` | Compact product card for inline embedding | `advertorial-product-callout.liquid` |
| `advertorial-fake-comment.liquid` | Single fake comment (avatar, name, text, likes) | `advertorial-comment-section.liquid` |
| `advertorial-source-citation.liquid` | Source citation / reference link styling | `advertorial-body-content.liquid` |
| `advertorial-reading-progress.liquid` | Reading progress bar (thin line at top of page) | `theme.advertorial.liquid` |

#### Cart Snippets

| Snippet | Mục đích | Used by |
|---|---|---|
| `cart-line-item.liquid` | Single cart line item (image, title, variant, quantity, price, remove) | `cart-drawer.liquid`, `main-cart.liquid` |
| `cart-upsell-item.liquid` | Upsell product suggestion in cart | `cart-drawer.liquid`, `main-cart.liquid` |
| `cart-free-shipping-bar.liquid` | Progress bar toward free shipping threshold | `cart-drawer.liquid`, `main-cart.liquid` |
| `cart-discount-code.liquid` | Discount code input field | `cart-drawer.liquid`, `main-cart.liquid` |
| `cart-totals.liquid` | Subtotal, discounts, shipping estimate, total | `cart-drawer.liquid`, `main-cart.liquid` |

#### Utility / SEO Snippets

| Snippet | Mục đích | Used by |
|---|---|---|
| `json-ld-product.liquid` | Product structured data (Schema.org Product) | `main-product.liquid`, product templates |
| `json-ld-article.liquid` | Article structured data (Schema.org Article) | `article.json`, advertorial template |
| `json-ld-breadcrumb.liquid` | BreadcrumbList structured data | `head-structured-data.liquid` |
| `json-ld-organization.liquid` | Organization structured data | `theme.liquid` |
| `pagination.liquid` | Pagination component | Collection, blog pages |
| `breadcrumbs.liquid` | Visual breadcrumb navigation | Product, collection pages |
| `share-buttons.liquid` | Social share buttons | Product, article, advertorial pages |

---

### 📁 ASSETS/ - CSS CHI TIẾT

#### Foundation CSS

| File | Mục đích | Loaded |
|---|---|---|
| `base.css` | Core styles: box-sizing, body defaults, container classes, grid system, responsive breakpoints, focus styles, print styles | Global (via `theme.liquid`) |
| `reset.css` | CSS reset / normalize | Global (inlined or first load) |
| `typography.css` | Font face declarations, heading styles (h1-h6), body text, links, lists, blockquotes, code | Global |
| `variables.css` | Fallback CSS custom properties (overridden by `css-variables.liquid` from theme settings) | Global |
| `utilities.css` | Utility classes: visually-hidden, clearfix, text-align, display, spacing helpers, color helpers | Global |
| `animations.css` | Keyframe animations: fade-in, slide-up, slide-in-right, pulse, shake, skeleton-loading | Global |

#### Component CSS (loaded on-demand by sections that use them)

| File | Components styled |
|---|---|
| `component-card.css` | Generic card component: border, shadow, padding, hover states |
| `component-badge.css` | Badge/tag component: sale badge, bestseller badge, trust badge |
| `component-button.css` | Button variants: primary, secondary, outline, sizes, loading state, disabled state |
| `component-modal.css` | Modal dialog: overlay, content box, close button, transitions |
| `component-accordion.css` | Accordion: question row, answer panel, open/close animation, icon rotation |
| `component-slider.css` | Slider/carousel: track, slides, navigation arrows, dots, responsive |
| `component-drawer.css` | Drawer: overlay, slide panel, header, body, footer |
| `component-loading-overlay.css` | Loading overlay: full-screen spinner, section-level spinner |
| `component-quantity-selector.css` | Quantity input: +/- buttons, input field, inline layout |
| `component-price.css` | Price display: regular, sale, compare-at, currency format |
| `component-rating-stars.css` | Star rating: filled stars, empty stars, half star, sizes |
| `component-progress-bar.css` | Progress bar: track, fill, animated, with text |
| `component-countdown-timer.css` | Countdown: digit boxes, separators, responsive |
| `component-sticky-bar.css` | Sticky bar: fixed positioning, shadow, slide animation |
| `component-announcement-bar.css` | Announcement bar: slim bar, text styling, close button |
| `component-tooltip.css` | Tooltip: positioning, arrow, content |
| `component-video-player.css` | Video: container, play button overlay, aspect ratio |

---

### 📁 ASSETS/ - JAVASCRIPT CHI TIẾT

#### Core JS

| File | Mục đích | Pattern |
|---|---|---|
| `global.js` | Global utilities: debounce, throttle, fetchConfig, trapFocus, removeTrapFocus, pauseAllMedia. Custom element base class. Cart API wrapper (add, update, change). Global event handlers | Module, immediately executed |
| `pubsub.js` | Publish/Subscribe event system for cross-component communication. Events: `variant:change`, `cart:update`, `cart:add`, `quantity:change` | Module |

#### Product JS

| File | Mục đích | Custom Element |
|---|---|---|
| `product-form.js` | Handles product form submission, AJAX add-to-cart, error handling, loading states | `<product-form>` |
| `product-variant-picker.js` | Variant selection logic: updates price, images, availability, URL. Handles option combinations | `<variant-selects>`, `<variant-radios>` |
| `product-image-gallery.js` | Image gallery: thumbnail navigation, main image swap, zoom on hover/click, touch swipe on mobile | `<product-gallery>` |
| `product-media.js` | Media type handling: image, video, 3D model. Pause/play on visibility | `<product-media>` |
| `quantity-selector.js` | Quantity +/- buttons logic, min/max validation, input sanitization | `<quantity-input>` |
| `quantity-breaks.js` | Quantity break tier selection: updates quantity, recalculates price, highlights selected tier, syncs with product form | `<quantity-breaks>` |
| `price-calculator.js` | Dynamic price calculation based on quantity, variant, and discount tiers. Updates displayed price, savings, compare-at | Helper module, imported by `quantity-breaks.js` |

#### Cart JS

| File | Mục đích | Custom Element |
|---|---|---|
| `sticky-add-to-cart.js` | Intersection Observer watches main ATC button; shows/hides sticky bar. Handles sticky bar ATC click | `<sticky-add-to-cart>` |
| `cart-drawer.js` | Cart drawer open/close, renders cart contents via AJAX (Section Rendering API), updates cart count badges | `<cart-drawer>` |
| `cart-notification.js` | Toast notification after successful add-to-cart | `<cart-notification>` |
| `cart-items.js` | Cart line item quantity changes, remove item, update totals via Fetch API | `<cart-items>` |

#### UI Component JS

| File | Mục đích | Custom Element |
|---|---|---|
| `accordion.js` | Accordion open/close with animation, optional single-open-at-a-time mode | `<accordion-component>` |
| `slider-component.js` | Generic slider/carousel: touch support, snap scrolling, autoplay, infinite loop option | `<slider-component>` |
| `testimonial-carousel.js` | Extends slider-component for testimonial-specific features: autoplay with pause on hover, review count update | `<testimonial-carousel>` |
| `modal-dialog.js` | Modal open/close, focus trap, escape key close, body scroll lock | `<modal-dialog>` |
| `drawer-component.js` | Generic drawer: slide from left/right, overlay, focus trap | `<drawer-component>` |
| `details-disclosure.js` | Enhanced `<details>` element with animation | `<details-disclosure>` |
| `deferred-media.js` | Lazy-load videos: shows poster image until play clicked, then injects iframe/video | `<deferred-media>` |
| `video-player.js` | Video playback controls, intersection observer auto-pause when out of view | `<video-player>` |
| `countdown-timer.js` | Countdown timer logic: calculates remaining time, updates display, handles expiry | `<countdown-timer>` |
| `before-after-slider.js` | Before/after image comparison: draggable divider, touch support, keyboard accessible | `<before-after-slider>` |
| `social-proof-popup.js` | Rotation logic for fake purchase notifications: timing, animation, randomization | `<social-proof-popup>` |
| `announcement-bar.js` | Auto-rotate multiple announcements, dismissible with cookie, countdown integration | `<announcement-bar>` |
| `smooth-scroll.js` | Smooth scroll to anchor links (used by CTA buttons targeting sections) | Global utility |
| `lazy-image.js` | Lazy loading images with IntersectionObserver, blur-up placeholder | `<lazy-image>` |
| `intersection-observer.js` | Reusable IntersectionObserver wrapper for scroll-triggered behaviors | Helper module |
| `scroll-animations.js` | Scroll-triggered CSS class additions for entrance animations | Global, uses `intersection-observer.js` |

#### Advertorial JS

| File | Mục đích |
|---|---|
| `advertorial-progress-bar.js` | Reading progress bar: calculates scroll position relative to article body, updates progress bar width |
| `advertorial-inline-cta.js` | CTA button click tracking, optional scroll-to-product behavior, analytics event firing |

---

### 📁 LOCALES/

#### `en.default.json`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Default English translations cho tất cả hardcoded strings trong theme |
| **Key sections** | `general` (pagination, search, social, accessibility), `products` (add to cart, sold out, unavailable, price labels, quantity, compare at), `cart` (title, empty, subtotal, checkout, shipping, free shipping bar messages), `sections` (section-specific strings: FAQ heading defaults, guarantee text defaults, trust badge defaults), `accessibility` (skip to content, close, open, menu), `advertorial` (read more, share, comments, related articles) |

#### `en.default.schema.json`
| Thuộc tính | Mô tả |
|---|---|
| **Mục đích** | Translations for all section schema labels visible in Theme Editor |
| **Key sections** | Labels for every section name, setting label, block name, and setting option across all sections |

---

### 📁 DEV-DOCS/

#### `README.md`
| Nội dung | Getting started guide, theme architecture overview, development setup (Shopify CLI), deployment instructions, key customization points |

#### `SECTIONS-MAP.md`
| Nội dung | Visual map showing which sections are used by which templates. Cross-reference table. Section dependency chart |

#### `STYLE-GUIDE.md`
| Nội dung | Design tokens (colors, typography, spacing), component patterns, naming conventions (BEM-inspired), responsive breakpoints, accessibility requirements |

#### `DEPLOYMENT.md`
| Nội dung | Shopify CLI commands, environment setup, theme publishing workflow, version control strategy |

---

## SECTION → TEMPLATE MAPPING

```
┌─────────────────────────────────┬─────────────┬──────────────────┬───────────────┐
│         SECTION                 │ product.    │ product.sales-   │ page.         │
│                                 │ json        │ page.json        │ advertorial   │
├─────────────────────────────────┼─────────────┼──────────────────┼───────────────┤
│ main-product                    │     ✅      │                  │               │
│ product-hero-media              │             │       ✅         │               │
│ product-info-panel              │             │       ✅         │               │
│ product-quantity-breaks         │             │       ✅         │               │
│ product-sticky-add-to-cart      │             │       ✅         │               │
│ product-trust-badges            │     ✅      │       ✅         │               │
│ product-benefit-icons           │             │       ✅         │               │
│ product-benefit-blocks-detailed │             │       ✅         │               │
│ product-how-it-works            │             │       ✅         │               │
│ product-before-after            │             │       ✅         │               │
│ product-comparison-table        │             │       ✅         │               │
│ product-ingredients             │             │       ✅         │               │
│ product-testimonials-carousel   │             │       ✅         │               │
│ product-testimonials-grid       │     ✅      │                  │               │
│ product-ugc-gallery             │             │       ✅         │               │
│ product-video-testimonial       │             │       ✅         │               │
│ product-vet-endorsed            │             │       ✅         │               │
│ product-faq-accordion           │     ✅      │       ✅         │               │
│ product-guarantee-banner        │             │       ✅         │               │
│ product-press-logos             │             │       ✅         │               │
│ product-social-proof-popup      │             │       ✅         │               │
│ featured-product                │             │       ✅         │               │
│ advertorial-hero                │             │                  │      ✅       │
│ advertorial-meta-bar            │             │                  │      ✅       │
│ advertorial-body-content        │             │                  │      ✅       │
│ advertorial-expert-quote        │             │                  │      ✅       │
│ advertorial-product-callout     │             │                  │      ✅       │
│ advertorial-inline-cta          │             │                  │      ✅       │
│ advertorial-image-block         │             │                  │      ✅       │
│ advertorial-social-proof-strip  │             │                  │      ✅       │
│ advertorial-before-after        │             │                  │      ✅       │
│ advertorial-comment-section     │             │                  │      ✅       │
│ advertorial-related-articles    │             │                  │      ✅       │
│ advertorial-sticky-cta-bar      │             │                  │      ✅       │
└─────────────────────────────────┴─────────────┴──────────────────┴───────────────┘
```

---

## FILE COUNT SUMMARY

| Category | Count |
|---|---|
| **CSS files** | 48 |
| **JavaScript files** | 32 |
| **Section files** | 52 |
| **Snippet files** | 54 |
| **Block files** | 19 |
| **Template files** | 23 |
| **Layout files** | 3 |
| **Config files** | 2 |
| **Locale files** | 2 |
| **Static assets (SVG/icons)** | 21 |
| **Documentation** | 4 |
| **TOTAL FILES** | **~260** |

---

## KEY ARCHITECTURE DECISIONS

```
1. DUAL LAYOUT SYSTEM
   └── theme.liquid          → Standard ecommerce pages
   └── theme.advertorial.liquid → Editorial/advertorial pages
       Lý do: Advertorial cần chrome hoàn toàn khác (no nav, 
       minimal header, reading progress bar, sticky CTA)

2. ALTERNATE TEMPLATES
   └── product.json              → Standard product page
   └── product.sales-page.json   → Long-form sales page
   └── page.advertorial.json     → Advertorial page
       Lý do: Cùng product có thể dùng 2 layouts khác nhau.
       Assign template qua Shopify Admin.

3. BLOCK ARCHITECTURE
   └── main-product.liquid uses blocks/ for flexible content ordering
   └── advertorial-body-content.liquid uses blocks/ for editorial flow
       Lý do: Theme Editor drag-and-drop ordering.
       Merchants có thể reorder content without code.

4. CSS STRATEGY
   └── Global: base, reset, typography, variables, utilities, animations
   └── Component: loaded by sections that need them ({% stylesheet %} tag
       or asset_url in section file)
   └── Section: scoped to specific section
   └── Template: page-level overrides
       Lý do: Performance - chỉ load CSS cần thiết per page.

5. JS STRATEGY
   └── Web Components (Custom Elements) pattern
   └── Global.js loaded everywhere (small, core utilities)
   └── Component JS loaded on-demand by sections
   └── PubSub for cross-component communication
       Lý do: Follows Dawn pattern. Encapsulated, no jQuery dependency.

6. SNIPPET COMPOSITION
   └── Sections compose UI from snippets
   └── Snippets are atomic, reusable components
   └── Consistent API: pass variables via {% render %} with params
       Lý do: DRY, maintainable, consistent UI.
```