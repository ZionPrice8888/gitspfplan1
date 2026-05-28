# 🐾 KẾ HOẠCH MIGRATE: Waggier → Companion DefaultTheme

**Mục tiêu:** Clone 1:1 nội dung, layout, media và tính năng từ Waggier vào DefaultTheme Shopify  
**Store:** companion-9700.myshopify.com 
**Permanent link:** jugjjq-1m.myshopify.com
**Theme đích:** `D:\OneDrive\livetobuild\companionspf\DefaultTheme`

---

## 📋 TỔNG QUAN 3 PHASE

| Phase | Trang | Tham chiếu | Template đích |
|-------|-------|-----------|---------------|
| 1 | Homepage | `waggier-homepage.html` | `templates/index.json` |
| 2 | Product Page | `waggier-pacebowl-2-product.html` | `templates/product.json` |
| 3 | Advertorial Page | `waggier-advertorial-page.html` | `templates/page.advertorial.json` + custom liquid |

---

## ⚙️ SETUP & CÔNG CỤ

```bash
# Dev server
shopify theme dev --store companion-9700.myshopify.com --path DefaultTheme

# Push theme
shopify theme push --path DefaultTheme --store companion-9700.myshopify.com

# Auth
shopify auth login --store companion-9700.myshopify.com
```

> [!IMPORTANT]
> Dùng file `.graphql` riêng biệt để push product/page qua Admin API — tránh lỗi cú pháp khi inline trong CLI.

---

## PHASE 1 — HOMEPAGE

### Layout Tổng Quan (từ HTML thực tế)

```
[HEADER GROUP — sections--19451233698020]
  ├── [1] Announcement Ticker (header-group)
  │     ID: horizontal_ticker_4U3wL7
  │     Nội dung: "Vet Approved · 10,000+ Happy Dogs · Free Shipping · 90-Day Refund"
  │     Style: dark bg (#2e2a39), white text, scrolling marquee
  │
  └── [2] Sticky Header (sections--19451233698020__header)
        ├── Logo (trái): Waggier logo PNG
        ├── Nav (giữa): Home · Shop Waggier · Contact Us · Track Order
        └── Icons (phải): Search · Account · Cart

[MAIN CONTENT — #MainContent, template--19451233370340]
  │
  ├── [S1] Hero Slideshow (cfca4268-6358-426c-98ab-d292aeef11e5)
  │     Layout: Full-width banner, banner--medium, 1 slide
  │     Image: 76a76a66-1bd9-4fba-a1c3-94a0896235e0.png (full-width, overlay opacity 0.3)
  │     Text (center, desktop-transparent box):
  │       h2 <strong>: "From 30-Second Gulping to 5-Minute Healthy Meals"
  │       highlight color: #ffffff
  │     CTA button: "Shop PaceBowl Now" → /products/waggier-pacebowl-2
  │
  ├── [S2] Logo Ticker (horizontal_ticker_maWmz4)
  │     Layout: Full-width horizontal scroll, color-accent-1 bg
  │     Speed: 30s animation, gap 17px mobile / 30px desktop
  │     Image height: 2.6rem mobile / 4.5rem desktop
  │     Items (loop): AKC logo ✦ petMD logo ✦ The Dodo logo ✦ Chewy logo ✦ (repeat x4)
  │
  ├── [S3] Section Divider (section_divider_U8wTNR)
  │     Shape: waves, transform: scaleX(1) scaleY(-1) (flipped)
  │     Shape color: #dd1d1d (accent red)
  │     BG color: #ffffff
  │
  ├── [S4] Image+Text — Benefit 1 (image_with_text_LYyAFU)
  │     Layout: 2-col desktop (50/50), stacked mobile
  │     Image col (LEFT): placeholder SVG (no image set — cần upload)
  │     Text col (RIGHT):
  │       bg: color-background-1 (#fff)
  │       Content card bg: #2e2a39 (dark), fg: #fff, btn: #dd1d1d
  │       h2 (highlight #339b43): "Prevents Deadly Bloat & Digestive Issues"
  │       Body: "Slowing eating from 30 seconds to 5 minutes dramatically reduces
  │              the risk of gastric bloat (GDV) - a condition that kills 30% of
  │              affected dogs. Plus eliminates vomiting, choking, and painful gas
  │              that plague fast eaters."
  │     Note: image col hiện là placeholder SVG, cần điền ảnh thực
  │
  ├── [S5] Image+Text — Benefit 2 (image_with_text_H7ELbL)
  │     Layout: 2-col desktop (50/50), REVERSED (image RIGHT)
  │     Image col (RIGHT): 3.jpg (1500×1500, square)
  │     Text col (LEFT):
  │       Content card bg: #2e2a39, fg: #fff, btn: #dd1d1d
  │       h2 (highlight #339b43): "Transforms Dangerous Gulping into Healthy Eating"
  │       Body: "Your dog finally chews their food properly, improving nutrient
  │              absorption and digestion. No more scary choking sounds, post-meal
  │              vomiting, or emergency vet visits. Every meal becomes safe and comfortable."
  │       CTA button: "Shop PaceBowl Now" → /products/waggier-pacebowl-2
  │
  ├── [S6] FAQ Collapsible (collapsible_content_4YQ43m)
  │     Layout: centered, narrow container, single column
  │     BG: #ffffff, fg: #2e2a39
  │     Heading: "FAQs" (h1, highlight #57bdf7)
  │     Style: accordion with check_box icon + caret arrow
  │     9 items (details/summary):
  │       1. Will this work for my flat-faced dog?
  │       2. My dog is really smart - won't they figure out how to eat fast anyway?
  │       3. What if my dog gets frustrated and stops eating?
  │       4. Is 2-4 cups enough for my medium/large dog?
  │       5. How do I clean the maze sections?
  │       6. Will the bowl slide around while my dog eats?
  │       7. What if my dog only eats wet food?
  │       8. My dog is already a slow eater - do I need this?
  │       9. Can I return it if it doesn't work for my dog?
  │
  └── [S7] Image+Text — CTA (image_with_text_GgRByD)
        Layout: 2-col desktop (50/50), image LEFT
        Image col (LEFT): product-in-use.jpg (1500×1500, square)
        Text col (RIGHT):
          Content card bg: #2e2a39, fg: #fff, btn: #dd1d1d
          h2 (highlight #57bdf7): "Ready to Transform Your Dog's Mealtime?"
          Body: "Your dog deserves to eat without choking. You deserve peace of
                 mind at every meal. Get your PaceBowl today and see the difference
                 in the very first meal."
          CTA button: "Shop PaceBowl Now" → /products/waggier-pacebowl-2

[FOOTER GROUP — sections--19451233665252]
  ├── [F1] Section Divider (section_divider_iXMaUU)
  ├── [F2] Footer Ticker (horizontal_ticker_DzgrVq) — trust badges lặp lại
  ├── [F3] Newsletter (newsletter_daGB6M) — "Join the Waggier Pack!"
  └── [F4] Footer — links + contact info + payment icons
```

### Sections cần clone (theo thứ tự từ `waggier-home-layout.json`)

| # | Section | Nội dung chính |
|---|---------|----------------|
| 1 | Announcement Ticker (header) | "Vet Approved · 10,000+ Happy Dogs · Free Shipping · 90-Day Refund" |
| 2 | Hero Banner | Heading: "From 30-Second Gulping to 5-Minute Healthy Meals" · CTA "Shop PaceBowl Now" |
| 3 | Header/Nav | Logo + Nav: Home, Shop Waggier, Contact Us, Track Order |
| 4 | Logo Ticker | AKC · petMD · The Dodo · Chewy |
| 5 | Section Divider | Waves shape |
| 6 | Image+Text — Benefit 1 | "Prevents Deadly Bloat & Digestive Issues" + "Slowing eating from 30 seconds to 5 minutes dramatically reduces the risk of gastric bloat (GDV) - a condition that kills 30% of affected dogs. Plus eliminates vomiting, choking, and painful gas that plague fast eaters."| 
| 7 | Image+Text — Benefit 2 | "Transforms Dangerous Gulping into Healthy Eating" + "Your dog finally chews their food properly, improving nutrient absorption and digestion. No more scary choking sounds, post-meal vomiting, or emergency vet visits. Every meal becomes safe and comfortable." + CTA (Shop PeaceBowl Now) |
| 8 | FAQ Collapsible | 9 FAQs về PaceBowl - ```"#### **1. Will this work for my flat-faced dog (pug, bulldog, etc.)?**
*   **Nội dung:** Yes! The honeycomb design is actually easier for flat-faced breeds than spiral mazes. The hexagonal compartments are shallow enough for pugs and bulldogs to access comfortably while still slowing them down effectively. We have hundreds of happy flat-faced customers.

#### **2. My dog is really smart - won't they figure out how to eat fast anyway?**
*   **Nội dung:** Even the smartest dogs can't physically bypass the honeycomb barriers. Unlike simple raised bumps they can eat around, our maze requires them to use their tongue to access each section individually. Studies show dogs may adapt slightly but still eat 8-10x slower than with regular bowls.

#### **3. What if my dog gets frustrated and stops eating?**
*   **Nội dung:** This rarely happens! 98% of dogs adapt within their first meal. The honeycomb design provides challenge without frustration. If your dog seems hesitant, try mixing in a small amount of wet food or treats initially. Our 90-day guarantee means you can return it if your dog truly won't use it.

#### **4. Is 2-4 cups enough for my medium/large dog?**
*   **Nội dung:** The 2-4 cup capacity is per meal, not per day. Most medium dogs eat 1.5-3 cups per meal, making this perfect. For larger dogs (over 60 lbs), you may need to split meals or consider buying two bowls. The slower eating actually helps dogs feel fuller with less food.

#### **5. How do I clean the maze sections?**
*   **Nội dung:** Super easy! The stainless steel is completely dishwasher safe - just place it on the top rack. For hand washing, the smooth steel surface rinses clean easily. No hidden crevices where food gets stuck like with plastic maze bowls. Most customers just rinse and dishwasher it daily.

#### **6. Will the bowl slide around while my dog eats?**
*   **Nội dung:** No! The heavy-duty rubber base grips your floor firmly. The bowl's weight (perfect for stability) combined with the anti-slip base means even aggressive eaters can't push it around. No more chasing bowls across the kitchen.

#### **7. What if my dog only eats wet food?**
*   **Nội dung:** Perfect for wet food too! The honeycomb design works great with pâté, chunks in gravy, or raw food. Wet food actually spreads into the compartments nicely, making dogs work to lick each section clean. Many customers use it for both wet and dry food.

#### **8. My dog is already a slow eater - do I need this?**
*   **Nội dung:** If your dog takes 5+ minutes to eat without gulping, you probably don't need this. However, many "slow" eaters still benefit from the mental stimulation and portion control the maze provides. Our bowl also prevents food aggression and anxiety around mealtime.

#### **9. Can I return it if it doesn't work for my dog?**
*   **Nội dung:** Absolutely! We offer a 90-day money-back guarantee. If your dog doesn't adapt or you're not completely satisfied, return it for a full refund. No questions asked, no forms to fill out. We're that confident your dog will thrive with PaceBowl." |
| 9 | Image+Text — CTA | "Ready to Transform Your Dog's Mealtime?" + "Your dog deserves to eat without choking. You deserve peace of mind at every meal. Get your PaceBowl today and see the difference in the very first meal." + CTA (Shop PeaceBowl Now)```|
| 10 | Footer Ticker | Trust badges lặp lại |
| 11 | Newsletter | "Join the Waggier Pack!" |
| 12 | Footer | Links + contact info |

### Media URLs — Homepage

```
Hero image:    https://waggier.com/cdn/shop/files/76a76a66-1bd9-4fba-a1c3-94a0896235e0.png
Logo:          https://waggier.com/cdn/shop/files/21-Transparent.png
Benefit 2 img: https://waggier.com/cdn/shop/files/3.jpg
CTA img:       https://waggier.com/cdn/shop/files/product-in-use.jpg
AKC logo:      https://waggier.com/cdn/shop/files/American_Kennel_Club_Logo_copy-fix_1dda7c8c-d682-40c4-93d8-1ea81b95e9bd.png
petMD logo:    https://waggier.com/cdn/shop/files/petMD_d25ed3e7-64c6-4a6e-b43d-edb5b8f066cd.png
The Dodo logo: https://waggier.com/cdn/shop/files/The_Dodo_logo_copy_2.png
Chewy logo:    https://waggier.com/cdn/shop/files/Chewy-Emblem_a8db9b87-8d80-487d-9b43-d8906a978c93.png
```

### Mapping `index.json` — Homepage

| Section Key DefaultTheme | Action | Nội dung |
|--------------------------|--------|---------|
| `cfca4268...` (slideshow) | Update slide | Hero heading + image + CTA |
| `horizontal_ticker_maWmz4` | Enable + điền ảnh | 4 logos + ✦ separators |
| `section_divider_U8wTNR` | Giữ nguyên | waves_3, flip_vertical: true |
| `image_with_text_LYyAFU` | Update heading + text | Benefit 1 |
| `image_with_text_H7ELbL` | Update heading + text + image + button | Benefit 2 + CTA |
| `collapsible_content_4YQ43m` | Update 9 FAQ blocks | FAQ content từ HTML |
| `image_with_text_GgRByD` | Update heading + text + button | "Ready to Transform..." |

### Design Tokens — Waggier

```json
{
  "dark_bg": "#2e2a39",
  "heading_highlight": "#8b1a2f",
  "cta_button": "#dd1d1d",
  "text_on_dark": "#ffffff"
}
```

### ✅ Checklist Phase 1

- [ ] Upload media assets lên Shopify Files
- [ ] `index.json` — hero: heading, image, CTA text
- [ ] `index.json` — logo ticker: enable, 4 images
- [ ] `index.json` — Benefit 1: heading + body text + image
- [ ] `index.json` — Benefit 2: heading + body text + image + button
- [ ] `index.json` — 9 FAQ blocks
- [ ] `index.json` — CTA section cuối
- [ ] `header-group.json` — nav links + logo image
- [ ] `footer-group.json` — contact info + links + newsletter
- [ ] `shopify theme push`
- [ ] Verify preview link
- [ ] Fix bugs

---

## PHASE 2 — PRODUCT PAGE (PaceBowl)

### Layout Tổng Quan (từ HTML thực tế)

```
[HEADER GROUP]
  ├── Sticky Header: Logo trái | Nav giữa (Home/Shop/Contact/Track) | Icons phải (search/account/cart)
  └── Announcement Ticker: "Vet Approved · 10,000+ Happy Dogs · Free Shipping · 90-Day Refund No Question Asked"

[MAIN CONTENT — #MainContent]
  └── Section: main (2-col grid, page-width)
        ├── [LEFT COL] Media Gallery (sticky, ~55% width)
        │     ├── Main slider: 6 media items (1 bundle PNG + 1 video MP4 + 4 product JPGs)
        │     │     Slide 1: Kaching-Bundles-1_bowl.png  ← hero image
        │     │     Slide 2: Video (61a2197...mp4)       ← product video
        │     │     Slide 3: front-food.jpg
        │     │     Slide 4: close-up.jpg
        │     │     Slide 5: product-in-use.jpg
        │     │     Slide 6: back-full.jpg
        │     └── Thumbnail slider: 6 thumbs bên dưới
        │
        └── [RIGHT COL] Product Info (sticky, ~45% width)
              ├── Rating stars: ★★★★★ 4.7 | 1802 Reviews (link → testimonials)
              ├── Badge pill: [👍 VETERINARY APPROVED DESIGN] (bg #2D5F3F, white text)
              ├── Product text box (bg #f3f3f3): "Prevents Deadly Bloat & Digestive Issues"
              ├── Product tagline: "With Waggier™ PaceBowl"
              ├── Price: $29.95 USD (accent color)
              ├── Stock indicator: 🟢 In stock
              ├── Emoji benefits:
              │     ⏰ 10x slower eating time
              │     🥇 304 stainless steel - dishwasher safe
              │     🐕 Holds 2-4 cups food or 25oz water
              ├── [ADD TO CART] button (full-width, dark green #2D5F3F)
              ├── Trust badges row: [Vet Approved] [Free Shipping] [90-Day Refund]
              └── Mini reviews carousel: Sarah M. / Michael C. / Jennifer W. (1-slide at a time)

[BELOW FOLD — Sections sau product form]
  ├── S1: Logo Ticker (AKC · petMD · The Dodo · Chewy)
  ├── S2: Image+Text — "Make Every Meal Last 10X Longer For A Healthy Life"
  ├── S3: Image+Text — "Transforms Dangerous Gulping into Healthy Eating"
  ├── S4: Custom Columns (4 features: Steel / Maze / Anti-Slip / Capacity)
  ├── S5: Testimonials (3 cards: Emma / Ashley / Maria với ảnh + 5★)
  ├── S6: FAQ Collapsible (9 items)
  └── S7: Image+Text CTA — "Ready to Transform Your Dog's Mealtime?"
```

### Thông tin sản phẩm cốt lõi

```
Tên:    Waggier™ PaceBowl
Rating: 4.7 | 1,802 Reviews
Badge:  "VETERINARY APPROVED DESIGN"
Tiêu đề: Prevents Deadly Bloat & Digestive Issues
Tagline: With Waggier™ PaceBowl
Giá:    $29.95 USD
Stock:  In stock
```

**Emoji benefits:**
```
⏰ 10x slower eating time
🥇 304 stainless steel - dishwasher safe
🐕 Holds 2-4 cups food or 25oz water
```

**Trust badges:** Vet Approved · Free Shipping · 90-Day Refund

### Product images (5 ảnh)

```
1. https://waggier.com/cdn/shop/files/Kaching-Bundles-1_bowl.png
2. https://waggier.com/cdn/shop/files/front-food.jpg
3. https://waggier.com/cdn/shop/files/close-up.jpg
4. https://waggier.com/cdn/shop/files/product-in-use.jpg
5. https://waggier.com/cdn/shop/files/back-full.jpg
```

### 3 Reviews mẫu

```
Sarah M.    — "My 11-year-old lab acts like a puppy again! No more vomiting after meals..."
Michael C.  — "Vet said this probably added years to my beagle's life. No more bloat scares..."
Jennifer W. — "Bought 3 bowls after seeing the difference in my golden. She's 13 and healthier..."
```

### Sections sau product form

| # | Section | Nội dung |
|---|---------|---------|
| 1 | Logo Ticker | AKC, petMD, The Dodo, Chewy |
| 2 | Image+Text | "Make Every Meal Last 10X Longer For A Healthy Life" + "Slowing eating from 30 seconds to 5 minutes dramatically reduces the risk of gastric bloat (GDV) - a condition that kills 30% of affected dogs. Plus eliminates vomiting, choking, and painful gas that plague fast eaters." |
| 3 | Image+Text | "Transforms Dangerous Gulping into Healthy Eating" + "Your dog finally chews their food properly, improving nutrient absorption and digestion. No more scary choking sounds, post-meal vomiting, or emergency vet visits. Every meal becomes safe and comfortable." |
| 4 | Custom Columns | "What Makes PaceBowl Different - Premium materials and thoughtful design for years of healthy meals" — 4 features |
| 5 | Testimonials | 3 reviews với ảnh (Emma, Ashley, Maria) |
| 6 | FAQ | 9 FAQ blocks |
| 7 | Image+Text CTA | "Ready to Transform?" + ADD TO CART + rating |

**4 PaceBowl features (custom_columns):**
```
✓ Premium 304 Stainless Steel — Medical-grade material that's bacteria-resistant, dishwasher safe, and lasts forever. No rust, no toxins, no replacement needed.
✓ Perfectly Sized Honeycomb Maze — Hexagonal patterns slow eating by 10x without frustration. Works for all snout shapes from pugs to collies.
✓ Anti-Slip Rubber Base — Heavy-duty rubber keeps bowl firmly in place. No sliding, no noise, no mess - even with aggressive eaters.
✓ Optimal 2-4 Cup Capacity — Perfect for small to medium dogs. Low 1.6" height prevents neck strain. Wide 8.6" diameter ensures comfortable eating.
```

**3 Testimonials chi tiết:**
```
Emma Rodriguez  — "No More Midnight Vomit Wake-Ups! - My beagle Bailey used to throw up every night from eating too fast. First night with PaceBowl - NOTHING! It's been 3 months and not a single incident. He actually chews now! The honeycomb design is genius. Easy to clean too. Worth every penny for peaceful nights." ★★★★★
Ashley Chen     — "Vet Shocked at Her Weight Loss! - My corgi Bella dropped 8 pounds in 2 months just from this bowl! She went from inhaling food in 20 seconds to actually working for it. Now takes her 6-7 minutes. No diet change, just slower eating. My vet asked what I did differently. Buying another for my mom's dog!" ★★★★★
Maria Thompson  — "Finally - A Bowl That Actually Works! - Tried 3 other slow feeders. My lab figured them all out. This honeycomb design? Game changer. Takes her full 5 minutes every meal now. No more bloat scares, no more anxiety watching her eat. She seems happier too - like she's playing a game. Already recommended to my whole dog park group!" ★★★★★
```

**Testimonial images:**
```
Emma photo:  https://waggier.com/cdn/shop/files/4.jpg
Ashley photo: https://waggier.com/cdn/shop/files/2.jpg
Maria photo:  https://waggier.com/cdn/shop/files/3.jpg
```

### Mapping `product.json`

| Block Key | Action | Nội dung |
|-----------|--------|---------|
| `a6eb81db` (rating_stars) | Update label | "4.7 \| 1802 Reviews" |
| `custom_liquid_fagfYn` | Update badge | "VETERINARY APPROVED DESIGN" |
| `text_YkAbhX` | Update | "Prevents Deadly Bloat & Digestive Issues With Waggier™ PaceBowl" |
| `emoji_benefits_AcTHmj` | Update | 3 emoji bullets |
| `icon_with_text_CigGfx` | Update | Vet Approved, Free Shipping, 90-Day Refund |
| `reviews_eAtdGq` | Update | 3 reviews |
| `collapsible_tab_wrcnex` | Update | Vet-Approved Benefits body |
| `collapsible_tab_pkkj8t` | Update | Shipping info |
| `collapsible_tab_LdEBMx` | Update | 90-Day guarantee |
| `image_with_text_DzyLRg` | Update | "Make Every Meal Last 10X Longer" |
| `image_with_text_UkqP8t` | Update + image | "Transforms Dangerous Gulping" |
| `custom_columns_AAnMLF` | Update | 4 features |
| `testimonials_wU7ngk` | Update | 3 testimonials + images |
| `collapsible_content_7Ddkx4` | Update | 9 FAQs |
| `image_with_text_KTAXCh` | Update | CTA + ADD TO CART button |

### GraphQL — Push Product

```graphql
# File: push-product.graphql
mutation productUpdate($input: ProductInput!) {
  productUpdate(input: $input) {
    product { id title }
    userErrors { field message }
  }
}

# Variables:
{
  "input": {
    "id": "gid://shopify/Product/...",
    "title": "Waggier™ PaceBowl",
    "descriptionHtml": "<p>...</p>",
    "images": [{ "src": "..." }]
  }
}
```

### ✅ Checklist Phase 2

- [ ] Upload 5 product images + 3 testimonial images
- [ ] Update product title, description, price (GraphQL)
- [ ] `product.json` — rating block (4.7 | 1802 Reviews)
- [ ] `product.json` — VETERINARY APPROVED badge
- [ ] `product.json` — title + emoji benefits
- [ ] `product.json` — trust icons (3 badges)
- [ ] `product.json` — 3 reviews
- [ ] `product.json` — collapsible tabs (3 tabs)
- [ ] `product.json` — 2 image+text benefit sections
- [ ] `product.json` — custom_columns (4 features)
- [ ] `product.json` — testimonials (3)
- [ ] `product.json` — FAQ (9 items)
- [ ] `product.json` — CTA section cuối
- [ ] `shopify theme push`
- [ ] Verify product page preview
- [ ] Fix bugs

---

## PHASE 3 — ADVERTORIAL PAGE

### Thông tin trang

```
URL:    /pages/dog-owner-exposes-hidden-truth
Title:  "Dog Owner Exposes Hidden Truth: The 30-Minute Timer That Nearly Killed Her Corgi"
Date:   August 05 2025 at 9:17 AM PST
Author: Jennifer Thompson
```

### Layout Tổng Quan (từ HTML thực tế — GemPages rebuilt as custom Liquid)

```
[HEADER — minimal]
  └── Waggier logo (waggier.com/cdn/shop/files/gempages_...f16b6ad4.png, 149×51)
      + navigation logos row (25% width mỗi logo)

[CONTENT WRAPPER — max-width: 1240px, grid 8fr/4fr desktop, 12fr mobile]

  ┌─── LEFT COLUMN (8fr) — Blog Article ───────────────────────────────┐
  │                                                                      │
  │  [ARTICLE HEADER]                                                   │
  │    h1 desktop (40px, bold): "Dog Owner Exposes Hidden Truth:        │
  │         The 30-Minute Timer That Nearly Killed Her Corgi"           │
  │    h1 mobile (30px, bold): same text                                │
  │    Date (italic, 16px): "August 05 2025 at 9:17 AM PST"            │
  │                                                                      │
  │  [PULL QUOTE BOX] (bg: #EBFEFB, pl:16px)                           │
  │    "My vet circled the timer on the wall: 'If your dog's            │
  │     stomach flips, you have 30 minutes or she dies.'"               │
  │                                                                      │
  │  [HERO IMAGE] (border-radius: 16px)                                 │
  │    gempages_...-18501f23-4284-41f3-a748-fc95e99157ac.jpg            │
  │                                                                      │
  │  [SUB-HEADING] "I thought Sophie just loved her food." (24px bold)  │
  │                                                                      │
  │  [BODY TEXT BLOCK 1] (18px, line-height 300% desktop)               │
  │    "Turns out I'd been playing Russian roulette..."                 │
  │    "If your dog wolfs down their meals in under 60 seconds..."      │
  │    "If you've ever joked about them being a 'vacuum cleaner'..."    │
  │    "If you think fast eating is just enthusiasm for food..."        │
  │    "Then what I'm about to share could save your dog's life."       │
  │                                                                      │
  │  [STAT CALLOUT] (18px bold)                                         │
  │    "Every single day, 30% of dogs who develop bloat                 │
  │     die—even WITH emergency treatment."                             │
  │                                                                      │
  │  --- (continuing narrative sections) ---                            │
  │  • "The Race Against Time" section + vet image                      │
  │  • "The Shocking Truth" + science data                              │
  │  • "The Hidden Trigger" + dog eating images                         │
  │  • Product introduction + honeycomb maze explanation                │
  │  • Video embed (Vimeo lite thumbnail)                               │
  │  • Science references block                                         │
  │  • Multiple [CTA BOX] + Button:                                     │
  │       "Apply Discount & Check Availability"                         │
  │       (links to /products/waggier-pacebowl-2)                       │
  │                                                                      │
  └──────────────────────────────────────────────────────────────────────┘

  ┌─── RIGHT COLUMN (4fr) — Sticky Sidebar ─────────────────────────────┐
  │  Product card (sticky)                                               │
  │    • Product image                                                   │
  │    • Price + CTA button                                             │
  │    • Trust badges                                                    │
  └──────────────────────────────────────────────────────────────────────┘

[FOOTER]
  Copyright © Waggier
  "THIS IS AN ADVERTISEMENT" disclaimer
  Privacy Policy | Terms of Service
```

### Typography & Style (từ GemPages CSS vars)

```css
/* Fonts */
--g-font-heading: 'Open Sans', sans-serif;  /* h1 */
--g-font-body:    'Poppins', sans-serif;    /* body */

/* Spacing desktop */
body font-size: 18px; line-height: 300%;
/* Spacing mobile */
body font-size: 16px; line-height: 200%;

/* Pull quote box */
background: #EBFEFB; padding: 8px 8px 8px 16px;

/* Article max-width */
max-width: 800px; /* for blog column */
```

### Media Assets — Advertorial

```
Logo:   .../gempages_579706557655155460-f16b6ad4-a54f-4746-8c4e-82ed9f484654.png (149×51)
Img 1:  .../gempages_579706557655155460-18501f23-4284-41f3-a748-fc95e99157ac.jpg (748×416)
Img 2:  .../gempages_579706557655155460-f3d242cb-53cb-4379-b5ee-de99ffa52915.jpg (748×511)
Img 3:  .../gempages_579706557655155460-006dd5d4-3e9b-460e-b7b6-8aa6bc738940.jpg (748×374)
Img 4:  .../gempages_579706557655155460-128f3ef8-b8b8-4e5e-aa75-424d668d58e3.jpg (748×512)
Img 5:  .../gempages_579706557655155460-0bbe880e-2af7-4ea7-9b9b-813d1b551b51.jpg (748×615)
Img 6:  .../gempages_579706557655155460-8ea82762-ec6a-4899-af0f-cab4da319c89.jpg (748×748)
Video:  .../gempages_579706557655155460-c9da892a-bf6a-4802-bae0-330e9ae1d851.jpg (thumbnail)
```

### Cách triển khai

> [!TIP]
> **Phương án A (Recommended):** Tạo custom Liquid section

```
1. Tạo: sections/advertorial-content.liquid
   - Clone HTML/CSS từ waggier-advertorial-page.html
   - Blog-style layout: max-width 800px, centered
   - Serif font cho body text

2. Tạo: templates/page.advertorial.json
   - Reference section advertorial-content

3. Push theme

4. Tạo Shopify Page qua GraphQL:
```

```graphql
# File: push-advertorial-page.graphql
mutation pageCreate($input: PageInput!) {
  pageCreate(input: $input) {
    page { id handle title }
    userErrors { field message }
  }
}
# Variables:
{
  "input": {
    "title": "Dog Owner Exposes Hidden Truth",
    "handle": "dog-owner-exposes-hidden-truth",
    "templateSuffix": "advertorial",
    "bodyHtml": ""
  }
}
```

### ✅ Checklist Phase 3

- [ ] Download + upload tất cả media assets advertorial (đang dùng CDN URL tạm)
- [x] Tạo `sections/advertorial-content.liquid` — full HTML
- [x] Style CSS blog-style (max-width 800px, typography)
- [x] Implement Vimeo lite video embed
- [x] Tạo `templates/page.advertorial.json`
- [ ] `shopify theme push`
- [ ] Tạo Shopify Page qua GraphQL
- [ ] Assign template `page.advertorial`
- [ ] Verify CTAs link đến product page (`/products/waggier-pacebowl-2`)
- [ ] Test video embed
- [ ] Fix bugs

---

## 🔄 VÒNG LẶP MỖI PHASE

```
Trích xuất HTML tham chiếu
        ↓
Lập Index Mapping + Checklist
        ↓
Sửa theme files (JSON / Liquid)
        ↓
shopify theme dev (preview local)
        ↓
shopify theme push
        ↓
Verify preview link
        ↓
Fix bugs → lặp lại từ bước dev
        ↓
✅ Hoàn thành phase
```

---

## 📁 FILES CẦN SỬA

```
DefaultTheme/
├── templates/
│   ├── index.json                  ← Phase 1
│   ├── product.json                ← Phase 2
│   └── page.advertorial.json       ← Phase 3 (NEW)
├── sections/
│   ├── header-group.json           ← Phase 1
│   ├── footer-group.json           ← Phase 1
│   └── advertorial-content.liquid  ← Phase 3 (NEW)
└── config/
    └── settings_data.json          ← Design tokens
```

---

## 📊 THEO DÕI TIẾN ĐỘ

| Phase | Trích xuất | Mapping | Sửa theme | Push | Verify | Status |
|-------|-----------|---------|-----------|------|--------|--------|
| 1 — Homepage | ✅ | ✅ | ✅ | ✅ | ⬜ | 🟡 Đã push — cần verify |
| 2 — Product | ✅ | ✅ | ✅ | ✅ | ⬜ | 🟡 Đã sửa + push — cần verify và upload media Shopify Files |
| 3 — Advertorial | ✅ | ✅ | ✅ | ⬜ | ⬜ | 🟡 Đã tạo section + template — cần push + tạo page |

---

## ⚠️ LƯU Ý QUAN TRỌNG

> [!WARNING]
> Media URLs từ Waggier CDN chỉ dùng tạm trong dev. Cần upload vào Shopify Files trước khi production push.

> [!NOTE]
> Advertorial dùng class CSS `gp-*` (GemPages) — cần recreate thủ công bằng custom Liquid, không thể import trực tiếp.

> [!IMPORTANT]
> Sau mỗi `shopify theme push`, CLI báo preview URL dạng `?preview_theme_id=XXX`. Copy link này để verify.
