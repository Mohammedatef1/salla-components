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


# Articles

## General
- **Title**: احدث المقالات
- **Path**: home.R-articles

### Settings
- **ID:** articles
  - **Label:** أضف المقالات
  - **Type:** Items (Dropdown List)
  - **Key Features:** Allows selecting multiple articles from the blog articles source; searchable and optional.

- **ID:** article_name_color
  - **Label:** لون عنوان المقال
  - **Type:** String (Color)
  - **Key Features:** Sets the color of the article title.

- **ID:** author_name_color
  - **Label:** لون تفاصيل المقال
  - **Type:** String (Color)
  - **Key Features:** Defines the color for article details.

- **ID:** article_color
  - **Label:** لون النص الأساسي للمقال
  - **Type:** String (Color)
  - **Key Features:** Specifies the primary text color for the article.

- **ID:** article_name_color_dark
  - **Label:** لون عنوان المقال دارك مود
  - **Type:** String (Color)
  - **Key Features:** Defines the article title color in dark mode.

- **ID:** author_name_color_dark
  - **Label:** لون تفاصيل المقال دارك مود
  - **Type:** String (Color)
  - **Key Features:** Sets the color for article details in dark mode.

- **ID:** article_color_dark
  - **Label:** لون النص الأساسي للمقال دارك مود
  - **Type:** String (Color)
  - **Key Features:** Defines the primary article text color in dark mode.

- **ID:** btn_text
  - **Label:** نص الزر
  - **Type:** String (Text)
  - **Key Features:** Sets the text displayed on the button, with a placeholder option.

- **ID:** btn_text_color
  - **Label:** لون الزر
  - **Type:** String (Color)
  - **Key Features:** Specifies the button color in light mode.

- **ID:** btn_text_color_dark
  - **Label:** لون الزر دارك مود
  - **Type:** String (Color)
  - **Key Features:** Defines the button color in dark mode.
