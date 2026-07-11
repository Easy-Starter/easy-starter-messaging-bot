<div dir="rtl" align="right">

<div align="center">

# استارتر بات پیام‌رسان

**پایه‌ی بات چندکاناله برای تلگرام، بله، واتساپ و پیام‌رسان‌های دیگر با معماری مبتنی بر Adapter.**

[![Use this template](https://img.shields.io/badge/Use%20this%20template-2ea44f?logo=github&logoColor=white)](https://github.com/easy-starter/easy-starter-messaging-bot/generate) [![CI](https://github.com/easy-starter/easy-starter-messaging-bot/actions/workflows/ci.yml/badge.svg)](https://github.com/easy-starter/easy-starter-messaging-bot/actions/workflows/ci.yml) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) ![Status: foundation](https://img.shields.io/badge/status-foundation-orange) ![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white) ![Django](https://img.shields.io/badge/Django-092E20?logo=django&logoColor=white) ![Multi-channel](https://img.shields.io/badge/Multi--channel-1f6feb) ![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)

[مستندات](https://github.com/easy-starter/easy-starter-docs) · [گزارش مشکل](https://github.com/easy-starter/easy-starter-messaging-bot/issues/new/choose)

</div>

> [!IMPORTANT]
> این ریپوزیتوری در مرحله‌ی **Foundation** است. تا انتشار اولین نسخه‌ی پایدار، آن را Production-ready در نظر نگیرید.

## چه مشکلی را حل می‌کند؟

منطق مکالمه و کسب‌وکار را از API پلتفرم‌ها جدا می‌کند تا یک محصول بات بدون تکرار هسته، چند کانال را پشتیبانی کند.

## این تمپلیت برای چه پروژه‌هایی مناسب است؟

- بات فرمانی و Workflow
- بات پشتیبانی و Human Handoff
- بات اعلان و توزیع محتوا
- دستیار AI و بات تراکنشی
- Adapter تلگرام، بله و واتساپ

**مناسب این موارد نیست:** برای تکرار Codebase به‌ازای هر پیام‌رسان یا دورزدن API رسمی پلتفرم‌ها نیست.

## امکانات پایه

- مدل پیام و مکالمه مستقل از کانال
- Interfaceهای Adapter برای Update ورودی و پیام خروجی
- مرزهای Webhook، Polling، State، Command و Middleware
- قرارداد Rate Limit، Retry، Deduplication و Observability
- ادمین، تست، Docker، CI و پروفایل استقرار

توضیحات جزئی معماری، قراردادها، پروفایل‌های استقرار و روش توسعه در [`docs/`](docs/) قرار می‌گیرند. توسعه‌ی فیچر از [`specs/`](specs/) شروع می‌شود و قوانین ایجنت‌ها در [`AGENTS.md`](AGENTS.md) نگهداری می‌شوند.

## شروع سریع

۱. روی **Use this template** بزنید یا فرمان زیر را اجرا کنید:

```bash
gh repo create my-project --template easy-starter/easy-starter-messaging-bot --private --clone
cd my-project
```

۲. نام پروژه، متادیتای پکیج و متغیرهای محیطی را تنظیم کنید.
۳. پروژه را اجرا کنید:

```bash
cp .env.example .env
make setup
make dev
make check
```

۴. اولین مشخصات فیچر را در `specs/` بنویسید.
۵. فیچر را پیاده‌سازی کنید و `make check` را سبز نگه دارید.

## قرارداد همکاری

- قبل از تغییر کد، `AGENTS.md` و Spec مرتبط را بخوانید.
- پیش از افزودن Abstraction یا Dependency جدید، از الگوهای موجود استفاده کنید.
- Credential یا داده‌ی واقعی پروداکشن را Commit نکنید.
- پیش از Pull Request تمام Quality Checkهای ریپو را اجرا کنید.
- تصمیم‌های معماری را در `docs/decisions/` ثبت کنید.

## مستندات

از `docs/getting-started.md` شروع کنید. راهنمای کامل‌تر توسعه‌ی AI-first در [Easy Starter Docs](https://github.com/easy-starter/easy-starter-docs) نگهداری می‌شود.

## مشارکت و پشتیبانی

قوانین مشارکت در [`CONTRIBUTING.md`](CONTRIBUTING.md)، روش دریافت کمک در [`SUPPORT.md`](SUPPORT.md) و گزارش مسائل امنیتی در [`SECURITY.md`](SECURITY.md) قرار دارد.

## مجوز

این پروژه تحت [مجوز MIT](LICENSE) منتشر می‌شود.

</div>
