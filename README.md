# Main Banner 

## General
- **Title**: البنر الرئيسي
- **Path**: home.main-banner

### Settings
- **ID**: `is_banner_image`
  - **Label**: البانر عبارة عن صورة
  - **Type**: Boolean (Switch)
- **ID**: `speed`
  - **Label**: زمن التحريك
  - **Type**: Number (Slider, 0 - 5s, step 0.1)
- **ID**: `auto_play`
  - **Label**: تشغيل تلقائى للسلايدر
  - **Type**: Boolean (Switch)
- **ID**: `slider_delay`
  - **Label**: زمن الـ Delay
  - **Type**: Number (Slider, 0 - 10s, step 0.2, requires auto-play)
- **ID**: `is_pagination`
  - **Label**: اظهار الـ Pagination
  - **Type**: Boolean (Switch)

### Collections
#### Banners (Structured Content, 1-12 items)
- **ID**: `banners.bg_color`
  - **Label**: لون الخلفية
  - **Type**: String (Color Picker)
- **ID**: `banners.background_shape`
  - **Label**: اضافة شكل للخلفية
  - **Type**: String (Image URL)
- **ID**: `banners.side_image`
  - **Label**: صورة جانبية
  - **Type**: String (Image URL)
- **ID**: `banners.primary_label`
  - **Label**: عنوان رئيسي
  - **Type**: String (Text, 2-200 chars)
- **ID**: `banners.primary_label_color`
  - **Label**: لون العنوان الرئيسي
  - **Type**: String (Color Picker)
- **ID**: `banners.secondary_label`
  - **Label**: عنوان فرعي
  - **Type**: String (Text, 2-200 chars)
- **ID**: `banners.secondary_label_color`
  - **Label**: لون العنوان الفرعي
  - **Type**: String (Color Picker)
- **ID**: `banners.btn_label`
  - **Label**: نص الزر
  - **Type**: String (Text, 2-200 chars)
- **ID**: `banners.btn_label_color`
  - **Label**: لون نص الزر
  - **Type**: String (Color Picker)
- **ID**: `banners.btn_bg_color`
  - **Label**: لون خلفية الزر
  - **Type**: String (Color Picker)
- **ID**: `banners.btn_link`
  - **Label**: رابط زر الإجراء
  - **Type**: String (Text, 2-200 chars)

#### Images (1-12 items, for image-based banners)
- **ID**: `images.banner_image`
  - **Label**: صورة البانر
  - **Type**: String (Image URL)
- **ID**: `images.banner_link`
  - **Label**: لينك البانر
  - **Type**: String (Text, 1-200 chars)

## Conditions
- `is_banner_image = true` → Uses `images` collection
- `is_banner_image = false` → Uses `banners` collection
- `auto_play = true` → Enables `slider_delay` control