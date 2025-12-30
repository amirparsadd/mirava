<div dir="rtl" align="right">

# Mirava
> لیست Mirror های ارائه‌شده توسط سایت‌های ایرانی 


---

## معرفی پروژه

یک مجموعه‌ی جامع و سریع از میرورهای عمومی نرم‌افزاری و مخازن بسته‌های نرم‌افزاری داخل کشور ایران است.  
هدف این پروژه فراهم‌کردن دسترسی آسان، سریع و پایدار به بسته‌های نرم‌افزاری به‌روزشده برای توسعه‌دهندگان، شرکت‌ها و کاربران ایرانی است.

این پروژه لیستی کامل و به‌روز از میرورهای داخلی بسته‌های نرم‌افزاری معتبر فراهم کرده که در شرایط محدودیت اینترنت بین‌الملل می‌تونه دسترسی سریع، پایداری بالا و ادامه فعالیت بدون قطعی رو ممکن کنه — به‌خصوص در شرایط نت ملی یا قطعی اینترنت خارجی.

---

## بخش های پروژه:

- فهرست دقیق و به‌روز میرورهای معتبر داخل ایران  
- اسکریپت Bash برای بررسی وضعیت دسترسی هر میرور  
- امکان همگام‌سازی با ابزارهایی مثل rsync یا wget  
- ساختار دادهٔ سبک و قابل‌توسعه با فرمت YAML  
- بررسی خودکار شبانه (قابل اتصال به CI)  
- قابل استفاده در پروژه‌های دیگر، سیستم‌عامل‌ها، و سرورهای داخلی

---

## میرورهای رسمی داخل ایران

| میرور (لینک) | توضیحات | پکیج‌های پوشش داده‌شده |
|--------------|----------|--------------------------|
| [mirror.shatel.ir](https://mirror.shatel.ir/) | میرور رسمی اوبونتو | مخازن اوبونتو، دبیان، کالی و فایل‌های نصب‌کننده |
| [mirrors.kubarcloud.com](https://mirrors.kubarcloud.com/) | میرور داخلی کوبار با پشتیبانی | سورس کرنل لینوکس و آرشیوهای متن‌باز متنوع |
| [repo-portal.ito.gov.ir](https://repo-portal.ito.gov.ir/repo/) | نگهداری شده توسط سازمان فناوری اطلاعات ایران | مخازن YUM/DNF برای CentOS، Fedora، Rocky، مخازن Python، npm، Yarn و … |
| [jamko.ir](https://jamko.ir/) | ارائه مستندات و نمونه‌های کانفیگ برای استفاده آسان‌تر | مخازن Maven، Gradle، Android SDK، APT، RPM، NuGet، Yarn، Composer، pip |
| [runflare.com/mirrors](https://runflare.com/mirrors/) | دارای راهنمای ساده و آپدیت خودکار روزانه | Composer/Packagist، PyPI، npm، Node.js |
| [hub.hamdocker.ir](https://hub.hamdocker.ir) | داکر ریجستری | Docker Registry |
| [repo.iut.ac.ir](https://repo.iut.ac.ir/) | میرور جامع دانشگاه صنعتی اصفهان با پوشش گسترده توزیع‌های لینوکسی و پروژه‌های متن‌باز | توزیع‌های Debian، Ubuntu، Mint، Arch Linux، Manjaro، Raspbian، Alpine، Rocky Linux، Fedora، OpenSUSE، OpenBSD و مخازن CTAN |
| [maven.myket.ir](https://maven.myket.ir/) | میرور جامعی از مخازن کتابخانه های اندرویدی شامل mavenCentral - googleMaven - Jitpack | Android sdk - android maven central - android jitpack - android googleMaven |
| [arvancloud.ir/dev/linux-repository](https://www.arvancloud.ir/en/dev/linux-repository) | میرور داخلی و پرسرعت از ریپازیتوری‌های محبوب‌ترین توزیع‌های گنو/لینوکس بر روی سرورهای ابر آروان| Debian, Ubuntu, CentOS, Alpine, Arch Linux, OpenSUSE, Manjaro |
| [mirror.iranserver.com](https://mirror.iranserver.com) |  میرور های داخلی پر سرعت بر روی سرور های ایران سرور | Debian, Ubuntu, CentOS |
| [docker.mobinhost.com](https://docker.mobinhost.com) | داکر ریجستری | Docker Registry |
| [mirror.mobinhost.com](https://mirror.mobinhost.com) |  میرور های داخلی پر سرعت بر روی سرور های مبین هاست | FreeBSD, Almalinux, Alpine, Archlinux, Debian, Fedora EPEL, Fedora, Manjaro, MariaDB, MongoDB, Raspbian, Ubuntu, Zabbix |
| [arvancloud.ir/fa/dev/docker](https://www.arvancloud.ir/fa/dev/docker) | میرور داخلی برای داکر | Docker Registry
---

## 🧪 دربارهٔ اسکریپت check_mirrors.sh

این اسکریپت بررسی می‌کنه که آینه‌هایی که در فایل mirrors_list.yaml تعریف شدن، واقعاً در دسترس هستند یا نه — مخصوصاً در شرایط داخل ایران.

### ویژگی‌ها:

- اجرای موازی برای افزایش سرعت بررسی  
- گرفتن IP هر میرور با dig یا getent  
- دور زدن مشکلات SSL با --insecure  
- خروجی متنی سازگار با ترمینال‌های فارسی  
- قابل اجرا روی سیستم‌های لینوکسی یا VPS داخل



---

## چطور یک میرور جدید به پروژه اضافه کنیم؟

اگر یک میرور خوب سراغ داری — مخصوصاً داخل ایران و بدون نیاز به VPN — خیلی خوشحال می‌شیم اون رو به لیست اضافه کنیم. این کار خیلی ساده‌ست:

### مراحل:

1. ریپازیتوری رو Fork کن  
2. فایل mirrors_list.yaml رو باز کن و اطلاعات میرور جدید رو اضافه کن  
3. اگه اسکریپتی برای همگام‌سازی داری (مثلاً با rsync یا wget)، بذارش داخل پوشه scripts/  
4. روی سیستم خودت تست بگیر  
5. بعدش یک Pull Request بفرست — من بررسی می‌کنم و اگه همه‌چی درست باشه، اضافه می‌شه.  

### چه جور میرورهایی به درد می‌خورن؟

- هر چیزی که داخل ایران باشه و بدون فیلتر باز شه  
- مخازن لینوکس: Debian، Ubuntu، Arch و بقیه  
- رجیستری پایتون (PyPI)، NPM، Docker، GitHub Releases و …  
- خلاصه هر سرویسی که تو شرایط نت ملّی یا تحریم به دادمون برسه

اگر فکر می‌کنی می‌تونی یه میرور معرفی کنی یا حتی خودت راه بندازی، خیلی خوشحال می‌شیم در این پروژه شریک شی. 

---
## 📢 شبکه‌های اجتماعی

- 🔗 [توییتر من](https://x.com/geedook13)
- 📣 [کانال تلگرام](https://t.me/shayangeedook)


---

## ☕ حمایت مالی

اگر از این پروژه خوشت اومده و دوست داری ازم حمایت کنی:

[Coffee](https://www.coffeete.ir/geedook)

با تشکر از حمایت‌هاتون!

---


با تشکر از آرمان طاهری [ArmanTaheriGhaleTaki](https://github.com/ArmanTaheriGhaleTaki) بابت چندین لینک میرور
