**ربات پیامرسان تلگرام**
  

---

این یک ربات تلگرام برای **ارتباط ناشناس بین کاربران و ادمین** است که با **PHP** توسعه داده شده است. کاربران می‌توانند پیام‌های خود را ارسال کنند و ادمین نیز می‌تواند از طریق **ریپلای (Reply)** پاسخ دهد.  

This is a **Telegram bot** developed in **PHP** for **anonymous communication between users and the admin**. Users can send messages, and the admin can reply using the **reply function**.

---

## 🚀 ویژگی‌ها | Features  
✅ ارسال پیام، عکس و استیکر توسط کاربران  
✅ پاسخگویی ادمین از طریق **ریپلای**  
✅ **فوروارد پیام‌ها** توسط ادمین  
✅ ذخیره‌سازی پیام‌ها در **فایل JSON**  
✅ **دکمه‌های اینلاین** برای پاسخ سریع  

✅ Users can send messages, photos, and stickers  
✅ Admin can reply using the **reply function**  
✅ **Forward messages** as an admin  
✅ Store messages in a **JSON file**  
✅ **Inline buttons** for quick responses  

---

## 📦 نیازمندی‌ها | Requirements  
- **سرور با پشتیبانی از PHP 7.4+**  
- **دسترسی به cURL**  
- **دسترسی نوشتن روی فایل‌ها (برای `message_ids.json`)**  

- **Server with PHP 7.4+ support**  
- **cURL access**  
- **Write access to files (for `message_ids.json`)**  

---

## 🛠️ راه‌اندازی | Setup  

### **1️⃣ دریافت توکن ربات | Get Bot Token**  
- با [@BotFather](https://t.me/BotFather) یک ربات جدید ایجاد کنید  
- توکن دریافتی را در خط ۲ کد جای‌گذاری کنید:  

```php
define('API_KEY', 'توکن_خود_را_اینجا_قرار_دهید');  
```

- Create a new bot using [@BotFather](https://t.me/BotFather)  
- Copy your token and paste it into **line 2** of the code:

```php
define('API_KEY', 'YOUR_BOT_TOKEN_HERE');  
```

---

### **2️⃣ تنظیم آیدی ادمین | Set Admin ID**  
- آیدی عددی تلگرام خود را در خط ۱ کد وارد کنید:  

```php
$admin = "آیدی_عدد_خود_را_اینجا_قرار_دهید";  
```

- Add your Telegram **numeric user ID** in **line 1**:  

```php
$admin = "YOUR_ADMIN_ID_HERE";  
```

---

### **3️⃣ آپلود کد | Upload the Code**  
- کد را روی **هاست** خود آپلود کنید  
- مطمئن شوید که **فایل `message_ids.json` با دسترسی نوشتن ایجاد شود**  

- Upload the code to your **hosting server**  
- Ensure that the **`message_ids.json` file has write access**  

---

### **4️⃣ تنظیم وب‌هوک | Set Webhook**  
- برای تنظیم وب‌هوک، دستور زیر را اجرا کنید (توکن و آدرس را جایگزین کنید):  

```
https://api.telegram.org/bot[TOKEN]/setWebhook?url=[URL_اسکریپت]
```

- Run the following command to set up the webhook (replace with your token and script URL):  

```
https://api.telegram.org/bot[TOKEN]/setWebhook?url=[YOUR_SCRIPT_URL]
```

---

## 🖥️ دستورالعمل استفاده | How to Use  

### **📌 برای کاربران | For Users:**  
- `/start` - نمایش پیام خوش‌آمدگویی | Shows a welcome message  
- ارسال هر پیام، عکس، یا استیکر - ارسال به ادمین | Send any message, photo, or sticker to the admin  

### **🔧 برای ادمین | For Admins:**  
- `/start` - نمایش پیام راهنما | Shows a help message  
- **ریپلای روی پیام + نوشتن پاسخ** - ارسال پاسخ به کاربر | Replying to a message with text sends a response to the user  
- **ریپلای + ارسال عکس/استیکر** - ارسال مدیا به کاربر | Replying with a photo/sticker sends media to the user  
- **استفاده از دکمه اینلاین** - برای پاسخ سریع | Use inline buttons for quick replies  

---

## ⚠️ نکات امنیتی | Security Tips  
🔒 **توکن ربات را محرمانه نگه دارید** | Keep your bot token **private**  
🔒 **آیدی ادمین را فقط به افراد معتمد بدهید** | Share admin ID only with **trusted people**  
🔒 **از HTTPS استفاده کنید** | Use **HTTPS** for secure connections  
🔒 **به‌صورت منظم از فایل JSON بکاپ بگیرید** | Regularly **backup `message_ids.json`**  

---

## 📄 ساختار فایل‌ها | File Structure  

```
├── bot.php            # فایل اصلی ربات | Main bot file
├── message_ids.json   # ذخیره ارتباط پیام‌ها | Stores message relations
└── temp.temp          # ذخیره موقت برای پاسخ اینلاین | Temporary storage for inline responses
```

---

## 📚 منابع | Resources  
- [Telegram Bot API Documentation](https://core.telegram.org/bots/api)  
- [PHP cURL Documentation](https://www.php.net/manual/en/book.curl.php)  

---

## 🤝 مشارکت | Contribution  
👥 **اگر پیشنهادی دارید، مشارکت کنید!**  

1. **Fork** کنید  
2. **Branch جدید بسازید** (`git checkout -b feature/AmazingFeature`)  
3. **Commit کنید** (`git commit -m 'Add some AmazingFeature'`)  
4. **Push کنید** (`git push origin feature/AmazingFeature`)  
5. **Pull Request ارسال کنید**  

Want to contribute? Follow these steps:  

1. **Fork** the repository  
2. **Create a new branch** (`git checkout -b feature/AmazingFeature`)  
3. **Commit your changes** (`git commit -m 'Add some AmazingFeature'`)  
4. **Push to the branch** (`git push origin feature/AmazingFeature`)  
5. **Open a Pull Request**  

---

## 📜 مجوز | License  
📄 این پروژه تحت **مجوز MIT** منتشر شده است - جزئیات در فایل [LICENSE](LICENSE)  

📄 This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.  

---

### **🛠 Developed by [CodeEpic](https://codeepic.ir) & [@theesmaeil1](https://t.me/theesmaeil1)**  
🚀 **Created with ❤️ for the Telegram community!**
