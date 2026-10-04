# DSC Lab Persian document template

قالب فارسی گزارش، پیشنهاد فنی و مستندات سازمانی آزمایشگاه پژوهشی محاسبات توزیع‌شده و مقیاس‌پذیر، با حفظ آرم دانشگاه علم و صنعت ایران.

## ساخت PDF

از ریشه پروژه با **XeLaTeX** دو بار اجرا کنید:

```powershell
xelatex -interaction=nonstopmode -halt-on-error dsc_tmp.tex
xelatex -interaction=nonstopmode -halt-on-error dsc_tmp.tex
```

به TeX Live یا MiKTeX با بسته‌های `xepersian`، `bidi`، `geometry`، `tikz`، `tcolorbox`، `titlesec` و سایر بسته‌های معرفی‌شده در فایل سبک نیاز است. فونت‌های فارسی در `fonts/` نگهداری شده‌اند؛ مانند نسخه اولیه، Roboto و DejaVu Sans باید روی سیستم نصب باشند. موتور pdfLaTeX مناسب این قالب نیست.

## شخصی‌سازی

- `document-info.tex`: نام و نوع سند، مخاطب، تهیه‌کننده، شناسه، نسخه، تاریخ و سطح دسترسی.
- `sections/introduction.tex`: متن معرفی و اطلاعات تماس آزمایشگاه.
- `sections/sample-report.tex`: نمونه ساختار گزارش؛ با محتوای پروژه جایگزین شود.
- `styles/dsclab.sty`: رنگ‌ها، جلد، تیترها، سربرگ، پابرگ و کادرها.
- `iust_logo.png`: آرم اصلی دانشگاه؛ حفظ شده است.

فونت‌های BNazanin، BNazaninBold، BTitr و مقیاس Roboto مطابق قالب اولیه هستند. معرفی و جدول‌های نمونه ادعای تأییدشده درباره توانمندی آزمایشگاه یا تعهد قراردادی نیستند؛ پیش از انتشار تکمیل شوند.

برنچ `university-template` قالب دانشگاه و برنچ `dsclab-template` قالب آزمایشگاه را نگه می‌دارد.


خروجی کامپایل جدید `dsc_tmp.pdf` است. پس از تغییر نام، فایل‌های کمکی فهرست تازه ساخته می‌شوند؛ XeLaTeX را دو بار اجرا کنید. فایل‌های `sep_tmp.tex` و `sep_tmp.pdf` در برنچ آزمایشگاه حذف شده‌اند؛ نسخه دانشگاه در برنچ خودش باقی است.
