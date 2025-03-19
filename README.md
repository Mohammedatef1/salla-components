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

```json
{
  "key": "6a7a1006-c65e-4156-bb2c-af37c5c5b4b7",
  "title": "البنر الرئيسي",
  "icon": "sicon-store",
  "path": "home.main-banner",
  "fields": [
      {
          "id": "description",
          "type": "static",
          "format": "description",
          "label": "Description",
          "value": "<img src='https://placehold.co/600x400' />",
          "variant": "h1",
          "icon": "sicon-format-size"
      },
      {
          "id": "is_banner_image",
          "type": "boolean",
          "format": "switch",
          "label": "البانر عبارة عن صورة",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-toggle-off",
          "value": true,
          "selected": false,
          "required": false
      },
      {
          "id": "speed",
          "type": "number",
          "format": "slider",
          "inputType": "range",
          "label": "زمن التحريك",
          "description": "الزمن بالثوانى",
          "labelHTML": null,
          "icon": "sicon-pin",
          "value": "0.3",
          "required": false,
          "step": ".1",
          "minimum": "0",
          "maximum": "5"
      },
      {
          "id": "auto_play",
          "type": "boolean",
          "format": "switch",
          "label": "تشغيل تلقائى للسلايدر",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-toggle-off",
          "value": true,
          "selected": false,
          "required": false
      },
      {
          "id": "slider_delay",
          "type": "number",
          "format": "slider",
          "inputType": "range",
          "label": "زمن الdelay",
          "description": "تحديد زمن التأخير في شريط التمرير  بمعني ضبط المدة الزمنية بين كل انتقال أو شريحة وأخرى.",
          "labelHTML": null,
          "icon": "sicon-pin",
          "value": "0.4",
          "required": false,
          "step": ".2",
          "minimum": "0",
          "maximum": "10",
          "conditions": [
              {
                  "id": "auto_play",
                  "operation": "=",
                  "value": true
              }
          ]
      },
      {
          "id": "is_pagination",
          "type": "boolean",
          "format": "switch",
          "label": "اظهار الpagination",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-toggle-off",
          "value": true,
          "selected": true,
          "required": false
      },
      {
          "id": "banners",
          "type": "collection",
          "format": "collection",
          "label": "البنرات",
          "description": null,
          "labelHTML": null,
          "item_label": null,
          "icon": "sicon-list-add",
          "fields": [
              {
                  "id": "banners.bg_color",
                  "type": "string",
                  "format": "color",
                  "labelHTML": null,
                  "inputType": "color",
                  "label": "لون الخلفية",
                  "description": null,
                  "icon": "sicon-format-fill",
                  "value": "#b5e935",
                  "required": false
              },
              {
                  "id": "banners.background_shape",
                  "type": "string",
                  "format": "image",
                  "label": "اضاقة شكل للخلفية",
                  "description": null,
                  "labelHTML": null,
                  "placeholder": "e.g. https://hostname.com/image.png",
                  "icon": "sicon-image",
                  "value": null,
                  "required": false
              },
              {
                  "id": "banners.side_image",
                  "type": "string",
                  "format": "image",
                  "label": "صورة جانبية",
                  "description": null,
                  "labelHTML": null,
                  "placeholder": "e.g. https://hostname.com/image.png",
                  "icon": "sicon-image",
                  "value": "https://cdn.salla.sa/form-builder/LG22rXtt2taVufvB5hu706S0S05faBdBndYpUkz7.png",
                  "required": false
              },
              {
                  "id": "banners.primary_label",
                  "type": "string",
                  "format": "text",
                  "label": "عنوان رئيسي",
                  "description": "ضع النص التوضيحي بين %",
                  "labelHTML": null,
                  "placeholder": "Placeholder text ..",
                  "icon": "sicon-format-text-alt",
                  "value": "اكتشفي أحدث  صيحات الموضة وكن دائمًا في المقدمة مع تشكيلتنا الفريدة",
                  "multilanguage": false,
                  "required": false,
                  "minLength": "2",
                  "maxLength": "200"
              },
              {
                  "id": "banners.primary_label_color",
                  "type": "string",
                  "format": "color",
                  "inputType": "color",
                  "label": "لون العنوان الرئيسي",
                  "description": null,
                  "labelHTML": null,
                  "icon": "sicon-format-fill",
                  "value": "#3b3b3b",
                  "required": false
              },
              {
                  "id": "banners.text_coloractive",
                  "type": "string",
                  "format": "color",
                  "inputType": "color",
                  "label": "لون النص التوضيحي",
                  "description": null,
                  "labelHTML": null,
                  "icon": "sicon-format-fill",
                  "value": "#004956",
                  "required": false
              },
              {
                  "id": "banners.secondary_label",
                  "type": "string",
                  "format": "text",
                  "label": "عنوان فرعي",
                  "description": null,
                  "labelHTML": null,
                  "placeholder": "Placeholder text ..",
                  "icon": "sicon-format-text-alt",
                  "value": "أكتشفي مجموعة الجمال الخالية من الكيماويات الضارة",
                  "multilanguage": false,
                  "required": false,
                  "minLength": "2",
                  "maxLength": "200"
              },
              {
                  "id": "banners.secondary_label_color",
                  "type": "string",
                  "format": "color",
                  "inputType": "color",
                  "label": "لون العنوان الفرعي",
                  "description": null,
                  "labelHTML": null,
                  "icon": "sicon-format-fill",
                  "value": "#4a4a4a",
                  "required": false
              },
              {
                  "id": "banners.btn_label",
                  "type": "string",
                  "format": "text",
                  "label": "نص الزر",
                  "description": null,
                  "labelHTML": "<style>.form--collection-item.mb-8, [class*=form--].mb-8 {margin-bottom: 8px !important;}</style>",
                  "placeholder": "Placeholder text ..",
                  "icon": "sicon-format-text-alt",
                  "value": "تسوق الان",
                  "multilanguage": false,
                  "required": false,
                  "minLength": "2",
                  "maxLength": "200"
              },
              {
                  "id": "banners.btn_label_color",
                  "type": "string",
                  "format": "color",
                  "inputType": "color",
                  "label": "لون نص الزر",
                  "description": null,
                  "labelHTML": null,
                  "icon": "sicon-format-fill",
                  "value": "#ffffff",
                  "required": false
              },
              {
                  "id": "banners.btn_bg_color",
                  "type": "string",
                  "format": "color",
                  "inputType": "color",
                  "label": "لون خلفية الزر",
                  "description": null,
                  "labelHTML": null,
                  "icon": "sicon-format-fill",
                  "value": "#3b3b3b",
                  "required": false
              },
              {
                  "id": "banners.btn_link",
                  "type": "string",
                  "format": "text",
                  "label": "رابط زر الإجراء",
                  "description": null,
                  "labelHTML": "<style>.form--collection-item.mb-8, [class*=form--].mb-8 {margin-bottom: 8px !important;}</style>",
                  "placeholder": "Placeholder text ..",
                  "icon": "sicon-format-text-alt",
                  "value": null,
                  "multilanguage": false,
                  "required": false,
                  "minLength": "2",
                  "maxLength": "200"
              }
          ],
          "value": [],
          "minLength": 1,
          "maxLength": "12",
          "conditions": [
              {
                  "id": "is_banner_image",
                  "operation": "=",
                  "value": false
              }
          ]
      },
      {
          "id": "images",
          "type": "collection",
          "format": "collection",
          "label": "images",
          "description": null,
          "labelHTML": null,
          "item_label": null,
          "icon": "sicon-list-add",
          "fields": [
              {
                  "id": "images.banner_image",
                  "type": "string",
                  "format": "image",
                  "label": "صورة البانر",
                  "description": null,
                  "labelHTML": null,
                  "placeholder": "e.g. https://hostname.com/image.png",
                  "icon": "sicon-image",
                  "value": null,
                  "required": false
              },
              {
                  "id": "images.banner_link",
                  "type": "string",
                  "format": "text",
                  "label": "لينك البانر",
                  "description": null,
                  "labelHTML": null,
                  "placeholder": "Placeholder text ..",
                  "icon": "sicon-format-text-alt",
                  "value": null,
                  "multilanguage": false,
                  "required": false,
                  "minLength": "1",
                  "maxLength": "200"
              }
          ],
          "value": [],
          "minLength": 1,
          "maxLength": "12",
          "conditions": [
              {
                  "id": "is_banner_image",
                  "operation": "=",
                  "value": true
              }
          ]
      }
  ]
}
```

# Articles

## General
- **Title**: احدث المقالات
- **Path**: home.R-articles

### Settings
- **ID:** `articles`
  - **Label:** أضف المقالات
  - **Type:** Items (Dropdown List)
  - **Key Features:** Allows selecting multiple articles from the blog articles source; searchable and optional.

- **ID:** `article_name_color`
  - **Label:** لون عنوان المقال
  - **Type:** String (Color)
  - **Key Features:** Sets the color of the article title.

- **ID:** `author_name_color`
  - **Label:** لون تفاصيل المقال
  - **Type:** String (Color)
  - **Key Features:** Defines the color for article details.

- **ID:** `article_color`
  - **Label:** لون النص الأساسي للمقال
  - **Type:** String (Color)
  - **Key Features:** Specifies the primary text color for the article.

- **ID:** `article_name_color_dark`
  - **Label:** لون عنوان المقال دارك مود
  - **Type:** String (Color)
  - **Key Features:** Defines the article title color in dark mode.

- **ID:** `author_name_color_dark`
  - **Label:** لون تفاصيل المقال دارك مود
  - **Type:** String (Color)
  - **Key Features:** Sets the color for article details in dark mode.

- **ID:** `article_color_dark`
  - **Label:** لون النص الأساسي للمقال دارك مود
  - **Type:** String (Color)
  - **Key Features:** Defines the primary article text color in dark mode.

- **ID:** `btn_text`
  - **Label:** نص الزر
  - **Type:** String (Text)
  - **Key Features:** Sets the text displayed on the button, with a placeholder option.

- **ID:** `btn_text_color`
  - **Label:** لون الزر
  - **Type:** String (Color)
  - **Key Features:** Specifies the button color in light mode.

- **ID:** `btn_text_color_dark`
  - **Label:** لون الزر دارك مود
  - **Type:** String (Color)
  - **Key Features:** Defines the button color in dark mode.

```json
{
  "key": "24f77f07-e4f3-4569-8928-9c8a6a26b5cc",
  "title": "احدث المقالات",
  "icon": "sicon-store",
  "image": "https://i.postimg.cc/y8NRxwzf/Screenshot-from-2025-01-05-14-11-19.png",
  "path": "home.R-articles",
  "fields": [
      {
          "id": "description",
          "type": "static",
          "format": "description",
          "label": "Description",
          "value": "<img src='https://placehold.co/600x400' />",
          "variant": "h1",
          "icon": "sicon-format-size"
      },
      {
          "id": "articles",
          "type": "items",
          "format": "dropdown-list",
          "label": "أضف المقالات",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-keyboard_arrow_down",
          "selected": [],
          "options": [],
          "source": "blog_articles",
          "multichoice": true,
          "searchable": true,
          "required": false,
          "value": []
      },
      {
          "id": "article_name_color",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون عنوان المقال",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#1f1f1f",
          "required": false
      },
      {
          "id": "author_name_color",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون تفاصيل المقال",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#1f1f1f",
          "required": false
      },
      {
          "id": "article_color",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون النص الأساسي للمقال",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#1f1f1f",
          "required": false
      },
      {
          "id": "article_name_color_dark",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون عنوان المقال دارك مود",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#ffffff",
          "required": false
      },
      {
          "id": "author_name_color_dark",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون تفاصيل المقال دارك مود",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#ffffff",
          "required": false
      },
      {
          "id": "article_color_dark",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون النص الأساسي للمقال دارك مود",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#ffffff",
          "required": false
      },
      {
          "id": "btn_text",
          "type": "string",
          "format": "text",
          "label": "نص الزر",
          "description": null,
          "labelHTML": null,
          "placeholder": "Placeholder text ..",
          "icon": "sicon-format-text-alt",
          "value": "",
          "multilanguage": false,
          "required": false,
          "minLength": "0",
          "maxLength": "300"
      },
      {
          "id": "btn_text_color",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون الزر",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#2e2e2e",
          "required": false
      },
      {
          "id": "btn_text_color_dark",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون الزر دارك مود",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#ffffff",
          "required": false
      }
  ]
}
```

# Store Map

## General
- **Title**: خريطة المتجر
- **Path**: home.R-store-map

### Settings
- **ID:** `main_heading`
  - **Label:** عنوان رئيسي
  - **Type:** String (Text)
  - **Key Features:** Defines the main heading text.

- **ID:** `main_heading_color`
  - **Label:** لون العنوان الرئيسي
  - **Type:** String (Color)
  - **Key Features:** Sets the color of the main heading.

- **ID:** `main_heading_color_dark`
  - **Label:** لون العنوان الرئيسي دارك مود
  - **Type:** String (Color)
  - **Key Features:** Defines the main heading color in dark mode.

- **ID:** `sub_heading`
  - **Label:** عنوان فرعي
  - **Type:** String (Text)
  - **Key Features:** Defines the subheading text.

- **ID:** `sub_heading_color`
  - **Label:** لون العنوان الفرعي
  - **Type:** String (Color)
  - **Key Features:** Sets the color of the subheading.

- **ID:** `sub_heading_color_dark`
  - **Label:** لون العنوان الفرعي دارك مود
  - **Type:** String (Color)
  - **Key Features:** Defines the subheading color in dark mode.

- **ID:** `location_text`
  - **Label:** وصف الموقع
  - **Type:** String (Text)
  - **Key Features:** Provides a description for the store location.

- **ID:** `location_text_color`
  - **Label:** لون نص الموقع
  - **Type:** String (Color)
  - **Key Features:** Sets the color of the location text.

- **ID:** `location_text_color_dark`
  - **Label:** لون نص الموقع دارك مود
  - **Type:** String (Color)
  - **Key Features:** Defines the location text color in dark mode.

- **ID:** `reach_methods_switch`
  - **Label:** تشغيل طرق الوصول
  - **Type:** Boolean (Switch)
  - **Key Features:** Enables or disables reach methods.

- **ID:** `location_url`
  - **Label:** رابط موقعك
  - **Type:** String (URL)
  - **Key Features:** Allows setting a URL for the store location.

- **ID:** `reach_methods`
  - **Label:** نص رئيسي
  - **Type:** String (Text)
  - **Key Features:** Sets the main text for reach methods.

- **ID:** `explaination_text`
  - **Label:** نص توضيحي
  - **Type:** String (Text)
  - **Key Features:** Provides an explanatory text.

- **ID:** `icon_background_color`
  - **Label:** لون خلفية الأيقونات
  - **Type:** String (Color)
  - **Key Features:** Sets the background color for icons.

- **ID:** `icon_background_color_dark`
  - **Label:** لون خلفية الأيقونات دارك مود
  - **Type:** String (Color)
  - **Key Features:** Defines the icon background color in dark mode.

```json
{
  "key": "735ed3e4-4fcb-46d9-a390-9e81e9dfe4c0",
  "title": "خريطة المتجر",
  "icon": "sicon-store",
  "path": "home.R-store-map",
  "fields": [
      {
          "id": "description",
          "type": "static",
          "format": "description",
          "label": "Description",
          "value": "<img src='https://placehold.co/600x400' />",
          "variant": "h1",
          "icon": "sicon-format-size"
      },
      {
          "id": "main_heading",
          "type": "string",
          "format": "text",
          "label": "عنوان رئيسي",
          "description": null,
          "labelHTML": null,
          "placeholder": "Placeholder text ..",
          "icon": "sicon-format-text-alt",
          "value": "",
          "multilanguage": false,
          "required": false,
          "minLength": "1",
          "maxLength": "500"
      },
      {
          "id": "main_heading_color",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون العنوان الرئيسي",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#000000",
          "required": false
      },
      {
          "id": "main_heading_color_dark",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون العنوان الرئيسي دارك مود",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#ffffff",
          "required": false
      },
      {
          "id": "sub_heading",
          "type": "string",
          "format": "text",
          "label": "عنوان فرعي",
          "description": null,
          "labelHTML": null,
          "placeholder": "Placeholder text ..",
          "icon": "sicon-format-text-alt",
          "value": "",
          "multilanguage": false,
          "required": false,
          "minLength": "1",
          "maxLength": "500"
      },
      {
          "id": "sub_heading_color",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون العنوان الفرعي",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#000000",
          "required": false
      },
      {
          "id": "sub_heading_color_dark",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون العنوان الفرعي دارك مود",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#ffffff",
          "required": false
      },
      {
          "id": "location_text",
          "type": "string",
          "format": "text",
          "label": "وصف الموقع",
          "description": null,
          "labelHTML": null,
          "placeholder": "Placeholder text ..",
          "icon": "sicon-format-text-alt",
          "value": "",
          "multilanguage": false,
          "required": false,
          "minLength": "1",
          "maxLength": "500"
      },
      {
          "id": "location_text_color",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون نص الموقع",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#000000",
          "required": false
      },
      {
          "id": "location_text_color_dark",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون نص الموقع دارك مود",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#ffffff",
          "required": false
      },
      {
          "id": "reach_methods_switch",
          "type": "boolean",
          "format": "switch",
          "label": "تشغيل طرق الوصول",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-toggle-off",
          "value": true,
          "selected": true,
          "required": false
      },
      {
          "id": "location_url",
          "type": "string",
          "format": "url",
          "inputType": "url",
          "label": "رابط موقعك",
          "description": null,
          "labelHTML": null,
          "placeholder": "e.g. https://salla.sa",
          "icon": "sicon-link",
          "value": "",
          "required": false,
          "minLength": "1",
          "maxLength": "1000"
      },
      {
          "id": "reach_methods",
          "type": "string",
          "format": "text",
          "label": "نص رئيسي",
          "description": null,
          "labelHTML": null,
          "placeholder": "Placeholder text ..",
          "icon": "sicon-format-text-alt",
          "value": "",
          "multilanguage": false,
          "required": false,
          "minLength": "1",
          "maxLength": "300"
      },
      {
          "id": "explaination_text",
          "type": "string",
          "format": "text",
          "label": "نص توضيحي",
          "description": null,
          "labelHTML": null,
          "placeholder": "Placeholder text ..",
          "icon": "sicon-format-text-alt",
          "value": "",
          "multilanguage": false,
          "required": false,
          "minLength": "1",
          "maxLength": "300"
      },
      {
          "id": "icon_background_color",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون خلفية الأيقونات",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#b5e935",
          "required": false
      },
      {
          "id": "icon_background_color_dark",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون خلفية الأيقونات دارك مود",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#b5e935",
          "required": false
      }
  ]
}
```

# Customer Reviews

## General
- **Title**: آراء العملاء
- **Path**: home.R_customer_reviews

### Settings
- **ID:** section_title
  - **Label:** عنوان القسم
  - **Type:** String (Text)
  - **Key Features:** Defines the section title text.

- **ID:** section_title_color
  - **Label:** لون عنوان القسم
  - **Type:** String (Color)
  - **Key Features:** Specifies the color of the section title.

- **ID:** section_title_color_dark
  - **Label:** لون عنوان القسم دارك مود
  - **Type:** String (Color)
  - **Key Features:** Sets the section title color in dark mode.

- **ID:** sub_text
  - **Label:** العنوان التوضيحي
  - **Type:** String (Text)
  - **Key Features:** Defines the subtitle or description text.

- **ID:** sub_text_color
  - **Label:** لون النص التوضيحي
  - **Type:** String (Color)
  - **Key Features:** Specifies the subtitle text color.

- **ID:** sub_text_color_dark
  - **Label:** لون النص التوضيحي دارك مود
  - **Type:** String (Color)
  - **Key Features:** Defines the subtitle text color in dark mode.

- **ID:** section_background
  - **Label:** لون خلفية القسم
  - **Type:** String (Color)
  - **Key Features:** Defines the background color for the section.

- **ID:** section_background_dark
  - **Label:** لون خلفية القسم دارك مود
  - **Type:** String (Color)
  - **Key Features:** Sets the background color for dark mode.

- **ID:** card_background
  - **Label:** لون خلفية العنصر
  - **Type:** String (Color)
  - **Key Features:** Specifies the background color of each review card.

- **ID:** card_background_dark
  - **Label:** لون خلفية العنصر دارك مود
  - **Type:** String (Color)
  - **Key Features:** Defines the background color of the review card in dark mode.

- **ID:** cust_review
  - **Label:** آراء العملاء
  - **Type:** Collection (List)
  - **Key Features:** Allows adding multiple customer reviews, including name, image, rating, and review text.

  - **ID:** cust_review.cust_img
    - **Label:** صورة العميل
    - **Type:** String (Image URL)
    - **Key Features:** Defines the customer profile image.

  - **ID:** cust_review.cust_name
    - **Label:** اسم العميل
    - **Type:** String (Text)
    - **Key Features:** Specifies the customer's name.

  - **ID:** cust_review.cust_name_color
    - **Label:** لون اسم العميل
    - **Type:** String (Color)
    - **Key Features:** Sets the text color of the customer's name.

  - **ID:** cust_review.cust_name_color_dark
    - **Label:** لون اسم العميل دارك مود
    - **Type:** String (Color)
    - **Key Features:** Defines the customer's name color in dark mode.

  - **ID:** cust_review.rating
    - **Label:** التقييم
    - **Type:** Number (0-5)
    - **Key Features:** Specifies the customer's rating from 0 to 5.

  - **ID:** cust_review.review
    - **Label:** رأي العميل
    - **Type:** String (Text)
    - **Key Features:** Stores the customer's written review.

  - **ID:** cust_review.cust_review_color
    - **Label:** لون رأي العميل
    - **Type:** String (Color)
    - **Key Features:** Defines the text color of the customer's review.

  - **ID:** cust_review.cust_review_color_dark
    - **Label:** لون رأي العميل دارك مود
    - **Type:** String (Color)
    - **Key Features:** Specifies the review text color in dark mode.

### Code

```json
{
  "key": "538ca030-7a3f-4952-baa8-96cebbd2176a",
  "title": "اراء العملاء",
  "icon": "sicon-store",
  "path": "home.R_customer_reviews",
  "fields": [
      {
          "id": "description",
          "type": "static",
          "format": "description",
          "label": "Description",
          "value": "<img src='https://placehold.co/600x400' />",
          "variant": "h1",
          "icon": "sicon-format-size"
      },
      {
          "id": "section_title",
          "type": "string",
          "format": "text",
          "label": "عنوان القسم",
          "description": null,
          "labelHTML": null,
          "placeholder": "Placeholder text ..",
          "icon": "sicon-format-text-alt",
          "value": "",
          "multilanguage": false,
          "required": false,
          "minLength": "0",
          "maxLength": "200"
      },
      {
          "id": "section_title_color",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون عنوان القسم",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#2e2e2e",
          "required": false
      },
      {
          "id": "section_title_color_dark",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون عنوان القسم دارك مود",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#2e2e2e",
          "required": false
      },
      {
          "id": "sub_text",
          "type": "string",
          "format": "text",
          "label": "العنوان التوضيحي",
          "description": null,
          "labelHTML": null,
          "placeholder": "Placeholder text ..",
          "icon": "sicon-format-text-alt",
          "value": "",
          "multilanguage": false,
          "required": false,
          "minLength": "0",
          "maxLength": "200"
      },
      {
          "id": "sub_text_color",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون النص التوضيحي",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#2e2e2e",
          "required": false
      },
      {
          "id": "sub_text_color_dark",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون النص التوضيحي دارك مود",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#2e2e2e",
          "required": false
      },
      {
          "id": "section_background",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون خلفية القسم",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#f3f3f3",
          "required": false
      },
      {
          "id": "section_background_dark",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون خلفية القسم دارك مود",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#f3f3f3",
          "required": false
      },
      {
          "id": "card_background",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون خلفية العنصر",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#ffffff",
          "required": false
      },
      {
          "id": "card_background_dark",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون خلفية العنصر دارك مود",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#ffffff",
          "required": false
      },
      {
          "id": "cust_review",
          "type": "collection",
          "format": "collection",
          "label": "راي العميل",
          "description": null,
          "labelHTML": null,
          "item_label": null,
          "icon": "sicon-list-add",
          "fields": [
              {
                  "id": "cust_review.cust_img",
                  "type": "string",
                  "format": "image",
                  "label": "صورة العميل",
                  "description": null,
                  "labelHTML": null,
                  "placeholder": "e.g. https://hostname.com/image.png",
                  "icon": "sicon-image",
                  "value": "",
                  "required": false
              },
              {
                  "id": "cust_review.cust_name",
                  "type": "string",
                  "format": "text",
                  "label": "اسم العميل",
                  "description": null,
                  "labelHTML": null,
                  "placeholder": "Placeholder text ..",
                  "icon": "sicon-format-text-alt",
                  "value": "",
                  "multilanguage": false,
                  "required": false,
                  "minLength": "1",
                  "maxLength": "200"
              },
              {
                  "id": "cust_review.cust_name_color",
                  "type": "string",
                  "format": "color",
                  "inputType": "color",
                  "label": "لون اسم العميل",
                  "description": null,
                  "labelHTML": null,
                  "icon": "sicon-format-fill",
                  "value": "#000000",
                  "required": false
              },
              {
                  "id": "cust_review.cust_name_color_dark",
                  "type": "string",
                  "format": "color",
                  "inputType": "color",
                  "label": "دارك مود لون اسم العميل",
                  "description": null,
                  "labelHTML": null,
                  "icon": "sicon-format-fill",
                  "value": "#ffffff",
                  "required": false
              },
              {
                  "id": "cust_review.rating",
                  "type": "number",
                  "format": "float",
                  "inputType": "number",
                  "label": "التقييم",
                  "description": null,
                  "labelHTML": null,
                  "placeholder": null,
                  "icon": "sicon-hashtag",
                  "value": 3,
                  "required": false,
                  "step": "1",
                  "minimum": "0",
                  "maximum": "5"
              },
              {
                  "id": "cust_review.review",
                  "type": "string",
                  "format": "text",
                  "label": "راي العميل",
                  "description": null,
                  "labelHTML": null,
                  "placeholder": "Placeholder text ..",
                  "icon": "sicon-format-text-alt",
                  "value": "",
                  "multilanguage": false,
                  "required": false,
                  "minLength": "0",
                  "maxLength": "500"
              },
              {
                  "id": "cust_review.cust_review_color",
                  "type": "string",
                  "format": "color",
                  "inputType": "color",
                  "label": "لون راي العميل",
                  "description": null,
                  "labelHTML": null,
                  "icon": "sicon-format-fill",
                  "value": "#000000",
                  "required": false
              },
              {
                  "id": "cust_review.cust_review_color_dark",
                  "type": "string",
                  "format": "color",
                  "inputType": "color",
                  "label": "لون راي العميل دارك مود",
                  "description": null,
                  "labelHTML": null,
                  "icon": "sicon-format-fill",
                  "value": "#ffffff",
                  "required": false
              }
          ],
          "value": [],
          "minLength": 1,
          "maxLength": "10"
      }
  ]
}
```

# Store Features

## General
- **Title**: مميزات المتجر
- **Path**: home.R-feature-section

### Settings
- **ID:** feature
  - **Label:** الميزة
  - **Type:** Collection
  - **Key Features:** Allows adding multiple features with customizable properties such as icons, animations, and descriptions.

- **ID:** feature_name_color
  - **Label:** لون اسم الميزة
  - **Type:** String (Color)
  - **Key Features:** Sets the color of the feature name.

- **ID:** feature_desc_color
  - **Label:** لون وصف الميزة
  - **Type:** String (Color)
  - **Key Features:** Defines the color for the feature description.

- **ID:** feature_name_color_dark
  - **Label:** لون اسم الميزة دارك مود
  - **Type:** String (Color)
  - **Key Features:** Defines the feature name color in dark mode.

- **ID:** feature_desc_color_dark
  - **Label:** لون وصف الميزة دارك مود
  - **Type:** String (Color)
  - **Key Features:** Sets the color for the feature description in dark mode.

- **ID:** feature.feature_img
  - **Label:** صورة الميزة
  - **Type:** String (Image URL)
  - **Key Features:** Allows setting an image for each feature.

- **ID:** feature.animation
  - **Label:** الانيميشن
  - **Type:** String (Text)
  - **Key Features:** Defines an animation from external sources like Lordicon.

- **ID:** feature.main_animation_color
  - **Label:** لون الانيميشن الأساسي
  - **Type:** String (Color)
  - **Key Features:** Sets the primary color of the animation.

- **ID:** feature.secondary_animation_color
  - **Label:** لون الانيميشن الثانوي
  - **Type:** String (Color)
  - **Key Features:** Defines the secondary animation color.

- **ID:** feature.icon
  - **Label:** الأيقونة
  - **Type:** String (Text)
  - **Key Features:** Specifies an icon for each feature.

- **ID:** feature.icon_color
  - **Label:** لون الأيقونة
  - **Type:** String (Color)
  - **Key Features:** Defines the color of the feature icon.

- **ID:** feature.feature_name
  - **Label:** اسم الميزة
  - **Type:** String (Text)
  - **Key Features:** Sets the name of the feature.

- **ID:** feature.feature_desc
  - **Label:** وصف الميزة
  - **Type:** String (Text)
  - **Key Features:** Provides a brief description of the feature.

- **ID:** one_feature_in_moblie
  - **Label:** وضع ميزة واحدة في وضع الموبايل
  - **Type:** Boolean (Switch)
  - **Key Features:** Enables displaying one feature at a time on mobile devices.

### Code

```json
{
  "key": "ed4d0b50-3507-4955-84a5-0bbe18647132",
  "title": "مميزات المتجر",
  "icon": "sicon-store",
  "path": "home.R-feature-section",
  "fields": [
      {
          "id": "description",
          "type": "static",
          "format": "description",
          "label": "Description",
          "value": "<img src='https://placehold.co/600x400' />",
          "variant": "h1",
          "icon": "sicon-format-size"
      },
      {
          "id": "feature",
          "type": "collection",
          "format": "collection",
          "label": "الميزة",
          "description": null,
          "labelHTML": null,
          "item_label": null,
          "icon": "sicon-list-add",
          "fields": [
              {
                  "id": "feature.feature_img",
                  "type": "string",
                  "format": "image",
                  "label": "صورة الميزة",
                  "description": null,
                  "labelHTML": null,
                  "placeholder": "e.g. https://hostname.com/image.png",
                  "icon": "sicon-image",
                  "value": "https://i.ibb.co/Jtnhq4d/5758be28d489ce0b4149bf58b95912f0.gif",
                  "required": false
              },
              {
                  "id": "feature.animation",
                  "type": "string",
                  "format": "text",
                  "label": "الانيميشن",
                  "description": "https://lordicon.com/",
                  "labelHTML": null,
                  "placeholder": "Placeholder text ..",
                  "icon": "sicon-format-text-alt",
                  "value": "",
                  "multilanguage": false,
                  "required": false,
                  "minLength": "0",
                  "maxLength": "200"
              },
              {
                  "id": "feature.main_animation_color",
                  "type": "string",
                  "format": "color",
                  "inputType": "color",
                  "label": "لون الانيميشن الاساسي",
                  "description": null,
                  "labelHTML": null,
                  "icon": "sicon-format-fill",
                  "value": "#b5e935",
                  "required": false
              },
              {
                  "id": "feature.secondary_animation_color",
                  "type": "string",
                  "format": "color",
                  "inputType": "color",
                  "label": "لون الانيميشن الثانوي",
                  "description": null,
                  "labelHTML": null,
                  "icon": "sicon-format-fill",
                  "value": "#2e2e2e",
                  "required": false
              },
              {
                  "id": "feature.icon",
                  "type": "string",
                  "format": "text",
                  "label": "الايقون",
                  "description": "https://codepen.io/jamalla2/pen/WNKWJPm",
                  "labelHTML": null,
                  "placeholder": "Placeholder text ..",
                  "icon": "sicon-format-text-alt",
                  "value": "",
                  "multilanguage": false,
                  "required": false,
                  "minLength": "0",
                  "maxLength": "300"
              },
              {
                  "id": "feature.icon_color",
                  "type": "string",
                  "format": "color",
                  "inputType": "color",
                  "label": "لون الايقون",
                  "description": null,
                  "labelHTML": null,
                  "icon": "sicon-format-fill",
                  "value": "#2e2e2e",
                  "required": false
              },
              {
                  "id": "feature.feature_name",
                  "type": "string",
                  "format": "text",
                  "label": "اسم الميزة",
                  "description": null,
                  "labelHTML": null,
                  "placeholder": "Placeholder text ..",
                  "icon": "sicon-format-text-alt",
                  "value": "جودة عالية",
                  "multilanguage": false,
                  "required": false,
                  "minLength": "0",
                  "maxLength": "200"
              },
              {
                  "id": "feature.feature_desc",
                  "type": "string",
                  "format": "text",
                  "label": "وصف الميزة",
                  "description": null,
                  "labelHTML": null,
                  "placeholder": "Placeholder text ..",
                  "icon": "sicon-format-text-alt",
                  "value": "تسوق منتجات موثوقة وعالية الجودة",
                  "multilanguage": false,
                  "required": false,
                  "minLength": "0",
                  "maxLength": "200"
              }
          ],
          "value": [],
          "minLength": 1,
          "maxLength": "10"
      },
      {
          "id": "feature_name_color",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون اسم الميزة",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#2e2e2e",
          "required": false
      },
      {
          "id": "feature_desc_color",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون وصف الميزة",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#2e2e2e",
          "required": false
      },
      {
          "id": "feature_name_color_dark",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون اسم الميزة دارك مود",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#FFFFFF",
          "required": false
      },
      {
          "id": "feature_desc_color_dark",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون وصف الميزة دارك مود",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#FFFFFF",
          "required": false
      },
      {
          "id": "one_feature_in_moblie",
          "type": "boolean",
          "format": "switch",
          "label": "وضع ميزة واحدة في وضع الموبايل",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-toggle-off",
          "value": true,
          "selected": true,
          "required": false
      }
  ]
}
```

# FAQ Section

## General
- **Title**: الاسئلة الشائعة
- **Path**: home.R-seq-section

### Settings
- **ID:** questions
  - **Label:** الاسئلة
  - **Type:** Collection
  - **Key Features:** Allows adding multiple FAQ items, each containing a question and an answer.

- **ID:** question_color
  - **Label:** لون السؤال
  - **Type:** String (Color)
  - **Key Features:** Sets the color for questions.

- **ID:** answer_color
  - **Label:** لون الاجابة
  - **Type:** String (Color)
  - **Key Features:** Defines the color for answers.

- **ID:** background_img
  - **Label:** خلفية القسم
  - **Type:** String (Image)
  - **Key Features:** Allows setting a background image for the section.

- **ID:** background_color
  - **Label:** لون الخلفيه
  - **Type:** String (Color)
  - **Key Features:** Specifies the background color of the section.

- **ID:** sub_background_color
  - **Label:** لون الخلفية الجزئية
  - **Type:** String (Color)
  - **Key Features:** Defines a secondary background color.

- **ID:** section_name
  - **Label:** العنوان الرئيسي الأيمن
  - **Type:** String (Text)
  - **Key Features:** Defines the right-side main heading.

- **ID:** section_name_color
  - **Label:** لون العنوان الرئيسي الأيمن
  - **Type:** String (Color)
  - **Key Features:** Sets the color for the right-side heading.

- **ID:** section_decs
  - **Label:** النص التوضيحي الايمن
  - **Type:** String (Text)
  - **Key Features:** Allows adding a right-side description.

- **ID:** section_decs_color
  - **Label:** لون النص التوضيحي الايمن
  - **Type:** String (Color)
  - **Key Features:** Sets the color for the right-side description.

- **ID:** head_section
  - **Label:** العنوان الرئيسي الأيسر
  - **Type:** String (Text)
  - **Key Features:** Defines the left-side main heading.

- **ID:** head_section_color
  - **Label:** لون العنوان الرئيسي الأيسر
  - **Type:** String (Color)
  - **Key Features:** Sets the color for the left-side heading.

- **ID:** btn_text
  - **Label:** نص الزر
  - **Type:** String (Text)
  - **Key Features:** Sets the text displayed on the button.

- **ID:** btn_text_color
  - **Label:** لون نص الزر
  - **Type:** String (Color)
  - **Key Features:** Defines the text color of the button.

- **ID:** btn_color
  - **Label:** لون الزر
  - **Type:** String (Color)
  - **Key Features:** Specifies the button color.

- **ID:** btn_url
  - **Label:** رابط الزر
  - **Type:** String (URL)
  - **Key Features:** Allows setting a hyperlink for the button.

- **ID:** video_url
  - **Label:** رابط الفيديو
  - **Type:** String (URL)
  - **Key Features:** Enables adding a video link to the section.

### Code

```json
{
  "key": "bce54d7f-69b7-4d9b-980e-865671b3602e",
  "title": "الاسئلة الشائعة",
  "icon": "sicon-store",
  "path": "home.R-seq-section",
  "fields": [
      {
          "id": "description",
          "type": "static",
          "format": "description",
          "label": "Description",
          "value": "<img src='https://placehold.co/600x400' />",
          "variant": "h1",
          "icon": "sicon-format-size"
      },
      {
          "id": "background_img",
          "type": "string",
          "format": "image",
          "label": "خلفية القسم",
          "description": null,
          "labelHTML": null,
          "placeholder": "e.g. https://hostname.com/image.png",
          "icon": "sicon-image",
          "value": "",
          "required": false
      },
      {
          "id": "video_url",
          "type": "string",
          "format": "url",
          "inputType": "url",
          "label": "رابط الفيديو",
          "description": null,
          "labelHTML": null,
          "placeholder": "e.g. https://salla.sa",
          "icon": "sicon-link",
          "value": null,
          "required": false,
          "minLength": "0",
          "maxLength": "300"
      },
      {
          "id": "background_color",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون الخلفيه",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#00d4fa",
          "required": false
      },
      {
          "id": "section_name",
          "type": "string",
          "format": "text",
          "label": "العنوان الرئيسي الأيمن",
          "description": null,
          "labelHTML": null,
          "placeholder": "Placeholder text ..",
          "icon": "sicon-format-text-alt",
          "value": "",
          "multilanguage": false,
          "required": false,
          "minLength": "0",
          "maxLength": "50"
      },
      {
          "id": "section_name_color",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون العنوان الرئيسي الأيمن",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#ffffff",
          "required": false
      },
      {
          "id": "section_decs",
          "type": "string",
          "format": "text",
          "label": "النص التوضيحي الايمن",
          "description": null,
          "labelHTML": null,
          "placeholder": "Placeholder text ..",
          "icon": "sicon-format-text-alt",
          "value": "نحن سعيدون بالرد على أسئلتكم",
          "multilanguage": false,
          "required": false,
          "minLength": "0",
          "maxLength": "100"
      },
      {
          "id": "section_decs_color",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون النص التوضيحي الايمن",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#ffffff",
          "required": false
      },
      {
          "id": "btn_url",
          "type": "string",
          "format": "url",
          "inputType": "url",
          "label": "رابط الزر",
          "description": null,
          "labelHTML": null,
          "placeholder": "e.g. https://salla.sa",
          "icon": "sicon-link",
          "value": "",
          "required": false,
          "minLength": "0",
          "maxLength": "200"
      },
      {
          "id": "btn_color",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون الزر",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#b5e935",
          "required": false
      },
      {
          "id": "btn_text",
          "type": "string",
          "format": "text",
          "label": "نص الزر",
          "description": null,
          "labelHTML": null,
          "placeholder": "Placeholder text ..",
          "icon": "sicon-format-text-alt",
          "value": "",
          "multilanguage": false,
          "required": false,
          "minLength": "0",
          "maxLength": "100"
      },
      {
          "id": "btn_text_color",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون نص الزر",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#000000",
          "required": false
      },
      {
          "id": "head_section",
          "type": "string",
          "format": "text",
          "label": "العنوان الرئيسي الأيسر",
          "description": null,
          "labelHTML": null,
          "placeholder": "Placeholder text ..",
          "icon": "sicon-format-text-alt",
          "value": "",
          "multilanguage": false,
          "required": false,
          "minLength": "0",
          "maxLength": "100"
      },
      {
          "id": "head_section_color",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون العنوان الرئيسي الأيسر",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#b5e935",
          "required": false
      },
      {
          "id": "questions",
          "type": "collection",
          "format": "collection",
          "label": "الاسئلة",
          "description": null,
          "labelHTML": null,
          "item_label": null,
          "icon": "sicon-list-add",
          "fields": [
              {
                  "id": "questions.question",
                  "type": "string",
                  "format": "text",
                  "label": "السؤال",
                  "description": null,
                  "labelHTML": null,
                  "placeholder": "Placeholder text ..",
                  "icon": "sicon-format-text-alt",
                  "value": "",
                  "multilanguage": false,
                  "required": false,
                  "minLength": "0",
                  "maxLength": "200"
              },
              {
                  "id": "questions.answer",
                  "type": "string",
                  "format": "text",
                  "label": "الاجابه",
                  "description": null,
                  "labelHTML": null,
                  "placeholder": "Placeholder text ..",
                  "icon": "sicon-format-text-alt",
                  "value": "",
                  "multilanguage": false,
                  "required": false,
                  "minLength": "0",
                  "maxLength": "200"
              }
          ],
          "value": [],
          "minLength": "0",
          "maxLength": "100"
      },
      {
          "id": "question_color",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون السؤال",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#ffffff",
          "required": false
      },
      {
          "id": "answer_color",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون الاجابة",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#ffffff",
          "required": false
      },
      {
          "id": "sub_background_color",
          "type": "string",
          "format": "color",
          "inputType": "color",
          "label": "لون الخلفية الجزئية",
          "description": null,
          "labelHTML": null,
          "icon": "sicon-format-fill",
          "value": "#ffffff",
          "required": false
      }
  ]
}
```