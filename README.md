# Certificates Generator / مولّد الشهادات

![GitHub repo size](https://img.shields.io/badge/status-ready-brightgreen) ![License](https://img.shields.io/badge/license-MIT-blue)

A lightweight web app to instantly generate PDF certificates from a template image and an Excel list of names.
تطبيق ويب خفيف لتوليد شهادات PDF بسرعة باستخدام صورة قالب وقائمة أسماء من ملف Excel.

---

## 📌 Table of Contents

* [Features / المميزات](#-features--المميزات)
* [Demo / المعاينة](#-demo--المعاينة)
* [Quick Start / ابدأ بسرعة](#-quick-start--ابدأ-بسرعة)
* [Usage / الاستخدام](#-usage--الاستخدام)
* [Excel format / تنسيق ملف Excel](#-excel-format--تنسيق-ملف-excel)
* [Customization / التخصيص](#-customization--التخصيص)
* [Technologies / التقنيات المستخدمة](#-technologies--التقنيات-المستخدمة)
* [Contributing / المساهمة](#-contributing--المساهمة)
* [License / الرخصة](#-license--الرخصة)

---

## ✨ Features / المميزات

* Upload an Excel file with recipient names.
  رفع ملف Excel يحتوي على أسماء المستفيدين.
* Upload any certificate template image (PNG or JPG).
  رفع صورة قالب الشهادة بأي مقاس أو نسبة.
* Live preview and drag-and-drop or input-based adjustment of the name position.
  معاينة مباشرة وتعديل مكان الاسم بالسحب والإفلات أو بالمدخلات.
* Generate a PDF for each name and download all as a ZIP.
  توليد ملف PDF لكل اسم وتحميل الكل كملف ZIP.
* Full Arabic support with Almarai font.
  دعم كامل للعربية بخط Almarai.
* Client-side only. No server required. Works in modern browsers.
  يعمل بالكامل على المتصفح. لا حاجة لسيرفر.

---

## 🚀 Demo / المعاينة

[Click here - إضغط هنا](https://mahmoud-el-tohamy.github.io/certify-me/)

---

## ⚡ Quick Start / ابدأ بسرعة

1. Clone the repo

```bash
git clone https://github.com/mahmoud-el-tohamy/certificates-creativa.git
cd certificates-creativa
```

2. Open `index.html` in any modern browser (Chrome/Edge/Firefox).
   يمكن فتح الملف مباشرة من الجهاز بدون إعدادات إضافية.

> إذا المشروع يستخدم بنية Node (مثال لبيئة تطوير محلية)

```bash
# optional: run a static server
npx http-server . -p 3000
# then open http://localhost:3000
```

---

## 🧭 Usage / الاستخدام

1. Prepare an Excel file with a single column of names (see format below).
2. Upload the Excel file using the UI.
3. Upload your certificate template image (PNG or JPG).
4. Use the live preview to position the name:

   * Drag the name box on the template, or
   * Edit X, Y, font size, and alignment inputs for precision.
5. Click "Generate Certificates" to create PDFs and download them as a ZIP.

### Example UI elements to include in your HTML

```html
<!-- file inputs -->
<input type="file" id="excelInput" accept=".xlsx,.xls,.csv" />
<input type="file" id="templateInput" accept="image/png, image/jpeg" />

<!-- preview area -->
<div id="preview">
  <img id="templateImage" src="" alt="template" />
  <div id="nameOverlay" contenteditable="true">اسم المتلقي</div>
</div>

<!-- controls -->
<input id="posX" type="number" />
<input id="posY" type="number" />
<input id="fontSize" type="number" />
<button id="generateBtn">Generate Certificates</button>
```

---

## 📄 Excel format / تنسيق ملف Excel

* Simple Excel Sheet containing Names, First row is a title.
* ملف إكسيل بسيط: عمود واحد يحتوي الأسماء، الصف الأول عنوان.

  Example:
  \| Name |
  \|------|
  \| Ahmed Mohamed |
  \| Sara Ali |
  \| Mahmoud Islam |

Accepts `.xlsx`, `.xls`, `.csv`.

---

## 🎨 Customization / التخصيص

* Font: use Almarai for Arabic. Example import:

```html
<link href="https://fonts.googleapis.com/css2?family=Almarai:wght@400;700&display=swap" rel="stylesheet">
<style>
  body { font-family: 'Almarai', sans-serif; }
</style>
```

* You can let users change:

  * font family and weight
  * font size
  * text color
  * alignment
  * rotation
  * multi-line support for titles and subtexts

---

## 🛠️ Technologies / التقنيات المستخدمة

* HTML, CSS, JavaScript
* \[SheetJS] for reading Excel files
* \[jsPDF] for generating PDFs
* \[JSZip] for zipping generated PDFs
* Google Fonts - Almarai for Arabic

Links (put these in your repo readme as live links):

* SheetJS: [https://sheetjs.com](https://sheetjs.com)
* jsPDF: [https://github.com/parallax/jsPDF](https://github.com/parallax/jsPDF)
* JSZip: [https://stuk.github.io/jszip/](https://stuk.github.io/jszip/)
* Almarai: [https://fonts.google.com/specimen/Almarai](https://fonts.google.com/specimen/Almarai)

---

## 📬 Contact / تواصل

Repo: `https://github.com/mahmoud-el-tohamy/certificates-creativa`
Email: `mahmoud.eltohamyy@gmail.com`

---

## 🧾 License / الرخصة

MIT License.
استخدمها كما تحب.
