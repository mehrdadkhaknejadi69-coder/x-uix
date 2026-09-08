# VodiWalker 27.0.0 — Control Center Upgrade

- داشبورد و Control Center ارتقا داده شد؛ مدیریت Inbound/Client و ابزارهای مدیریتی حفظ و یکپارچه شدند.
- امکان تغییر نام کاربری و رمز حساب واردشده اضافه شد؛ username در state پایدار ذخیره می‌شود.
- نمایش username واقعی مالک در Admin Manager اصلاح شد.
- حالت English داشبورد به LTR واقعی ارتقا یافت و برای محتوای پویا MutationObserver ترجمه‌ی UI را حفظ می‌کند.
- صفحه Login دست‌نخورده باقی ماند.
- مسیر/دکمه‌ی «تمدید از ربات» از Subscription Portal حذف شد.
- همه‌ی فایل‌های Python با py_compile بررسی شدند و import کامل پروژه نیز تست شد.
# تغییرات نسخه 22

- بازطراحی کامل Subscription Portal
- Appearance Studio حرفه‌ای با فونت‌های Estedad، IBM Plex Sans Arabic، Shabnam و Yekan Bakh
- اضافه شدن ۱۰ Accent Color
- اضافه شدن Font Size، Radius، Glow، Motion و Wide Sidebar
- رفع مشکل ذخیره نشدن انتخاب فونت
- تبدیل لیست Inbound به کارت‌های مدیریتی حرفه‌ای
- اضافه شدن ابزارهای Control Center Pro
- حفظ سازگاری APIهای Subscription و Railway

## نسخه 25.0.0 — Message Center & Secure Login
- اضافه شدن «مرکز پیام» مستقل برای خطاها و هشدارها.
- ثبت خطاهای Backend و خطاهای JavaScript/Unhandled Promise در پنل.
- فیلتر خطا، هشدار و خطاهای مرورگر + پاک‌سازی امن لاگ خطا.
- بروزرسانی خودکار مرکز پیام و شمارنده خطا در ناوبری.
- ارتقای گرافیک صفحه ورود با لایه‌های نور، Grid، Scanline، وضعیت امنیتی و کارت دسترسی حرفه‌ای.
- بهبود گزارش خطاهای API برای نمایش پیام دقیق‌تر به کاربر.
- تست Health/Login/API Error انجام شد.

### تکمیل حرفه‌ای Builder — v27.1
- صفحه‌ی واسط قدیمی روت حذف شد؛ آدرس `/` مستقیماً به `/login` می‌رود و بعد از ورود به `/dashboard` هدایت می‌شود.
- Builder اینباند کاملاً تفکیک شد: **Base Protocol** در یک بخش مستقل، **Transport/Network** در بخش مستقل و **Security** در بخش مستقل.
- پروتکل‌های پایه‌ی Builder اکنون شامل VLESS، VMess، Trojan و Shadowsocks هستند.
- Transportها به‌صورت کارت‌های مستقل TCP / WebSocket / gRPC / XHTTP نمایش داده می‌شوند.
- برای Shadowsocks محدودیت TCP-only در UI اعمال شده و فیلد Method/Password اختصاصی دارد.
- فیلدهای پیشرفته فقط متناسب با انتخاب‌های کاربر نمایش داده می‌شوند و خلاصه‌ی نهایی قبل از ساخت قابل مشاهده است.
