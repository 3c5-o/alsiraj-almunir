# السراج المنير

Telegram Mini App ديني متوافق مع الهاتف، يضم القرآن الكريم نصًا وصوتًا، خطة ختمة، مواقيت الصلاة، القبلة، الأذكار، المفضلة، ولوحة إدارة محمية بهوية Telegram.

## البنية

- `index.html` واجهة Telegram Mini App.
- `assets/styles.css` التصميم المتجاوب RTL.
- `assets/app.js` تكامل Telegram WebApp والواجهة.
- `worker/src/index.js` Backend على Cloudflare Workers والتحقق من Telegram `initData`.
- `worker/wrangler.toml` إعداد Worker وD1.
- `database/schema.sql` مخطط قاعدة البيانات.

## الأمان

لا يتم وضع Bot Token أو Quran API secrets داخل المستودع أو الواجهة. تُحفظ كمفاتيح سرية في Cloudflare Worker.

المتغيرات المطلوبة عند النشر:

- `TELEGRAM_BOT_TOKEN` (Secret)
- `ADMIN_TELEGRAM_ID`
- `QURAN_CLIENT_ID` (Secret عند الحاجة)
- `QURAN_CLIENT_SECRET` (Secret)

## الحالة

المرحلة الحالية: تأسيس الهيكل الآمن للمشروع وربط Telegram Mini App. يليها ربط القرآن والصوت، ثم الختمة والصلاة والأذكار ولوحة الإدارة.
