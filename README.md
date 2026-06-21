## 🎵 لینک مستقیم پخش زنده رادیو جوان (بدون فیلتر) | Radio Javan Live Stream Direct Link

[![Stars](https://img.shields.io/github/stars/s-30j/radiojavan-live-stream?style=flat-square&color=00d4ff)](https://github.com/s-30j/radiojavan-live-stream/stargazers)
[![Forks](https://img.shields.io/github/forks/s-30j/radiojavan-live-stream?style=flat-square&color=8a2be2)](https://github.com/s-30j/radiojavan-live-stream/network/members)
[![License](https://img.shields.io/github/license/s-30j/radiojavan-live-stream?style=flat-square)](LICENSE)
[![Last Commit](https://img.shields.io/github/last-commit/s-30j/radiojavan-live-stream?style=flat-square)](https://github.com/s-30j/radiojavan-live-stream/commits/main)

**لینک مستقیم پخش زنده رادیو جوان (Radio Javan TV)** به‌صورت HLS (`m3u8`) — بدون فیلتر، بدون VPN، و بدون نیاز به دسترسی به سایت اصلی که در ایران مسدود است. این ریپازیتوری چند لینک مستقیم استریم + یک اسکریپت Node.js برای راه‌اندازی سرور واسط (Forwarder) ارائه می‌دهد.


## 📡 لینک‌های مستقیم پخش زنده

| نوع لینک | آدرس |
|---|---|
| 🔵 لینک اول (با کلودفلر) | `https://radio.sr-api.ir/hls/stream.m3u8` |
| 🟣 لینک دوم | `https://radio2.sr-api.ir/hls/stream.m3u8` |
| 🌐 سرور اصلی (ممکن است روی برخی اینترنت‌ها کار نکند) | `https://51.254.225.31/hls/stream.m3u8` |
| 🚫 لینک اصلی رادیو جوان (فیلتر شده در ایران) | `https://rjtvhls.wns.live/hls/stream.m3u8` |

---

## ▶️ نحوه استفاده

این لینک‌ها با هر پلیری که از پروتکل HLS پشتیبانی کند کار می‌کنند:

- **VLC Media Player** → `Media > Open Network Stream` → لینک را پیست کنید
- پلیرهای موزیک و اپلیکیشن‌های موبایل (با پشتیبانی m3u8)
- ربات‌های دیسکورد / تلگرام برای پخش استریم
- بازی‌ها و اپلیکیشن‌های کاستوم با قابلیت پخش HLS



---
<br>
<br>
<br>

##  🚀 راه‌اندازی Forwarder روی دامنه خودتان

اگر دانش فنی کافی دارید، می‌توانید با اسکریپت `serverForward.js` یک **TCP/TLS Forwarder** روی سرور و دامنه‌ی خودتان بالا بیاورید (مثلاً برای نیم‌بها کردن ترافیک یا افزایش سرعت).

### پیش‌نیاز
نیاز به یک دامنه و دریافت ssl روی دامنه

```bash
apt install certbot
sudo certbot certonly --standalone --preferred-challenges http -d yourdomain.com
```
در اسکریپت دامنه و مسیر ssl خود را مشخص کنید و بعد از ان

### اجرا

```bash
node serverForward.js
```

> ⚠️ بعد از تفییرات مقادیر `SSL_CERT` ، `SSL_KEY` و `REMOTE_SNI` در اسکریپت و اجرا ، شما میتوانید با استفاده از لینک زیر به پخش زنده روی دامنه خودتان دسترسی داشته باشید
```bash
https://yourdomain.com:5555/hls/stream.m3u8
برای مثال در اسکریپت از دامنه زیر استفاده شده
https://radio3.sr-api.ir:5555/hls/stream.m3u8
```
---


اگر این پروژه برایتان مفید بود:

- ⭐ به ریپو **Star** بدهید — این به دیده شدن بهتر پروژه کمک می‌کند
- 🍴 آن را **Fork** کنید و پیشنهادات خود را با Pull Request ارسال کنید
- 🐛 مشکلات را در بخش [Issues](https://github.com/s-30j/radiojavan-live-stream/issues) گزارش دهید

---

<p align="center">ساخته‌شده با ❤️ برای دسترسی آزاد</p>
