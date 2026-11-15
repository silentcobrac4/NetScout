# NetScout | نت سكاوت

**العربية** · [English](#english)

تطبيق أندرويد مجاني ومفتوح المصدر وبدون إعلانات، يساعدك على معرفة ما يحدث داخل شبكة الواي فاي عندك: من المتصل بها، هل الراوتر آمن، وكيف حال الإنترنت. يعمل كله على جهازك ولا يحتاج حساباً ولا يرسل بياناتك إلى أي خادم.

> مشروع مستقل، وغير تابع لأي تطبيق تجاري مشابه.

## الفكرة
كثير من تطبيقات فحص الشبكات مليئة بالإعلانات أو تقفل أدواتها خلف اشتراك. NetScout يجمع الأدوات الأساسية في تطبيق واحد خفيف، وكل شيء فيه مجاني.

## المميزات
- **الأجهزة:** اكتشاف كل الأجهزة المتصلة (ping sweep، DNS العكسي، mDNS، NetBIOS، SSDP/UPnP)، تخمين نوع الجهاز والشركة المصنّعة، أسماء وملاحظات مخصصة، وأول وآخر ظهور.
- **تنبيه المتطفلين:** عَلِّم أجهزتك كمعروفة، وسيصلك إشعار عند ظهور جهاز جديد (فحص دوري بالخلفية).
- **الأدوات:** Ping، Traceroute، DNS، WHOIS، فاحص منافذ، Wake-on-LAN، فحص HTTP، ماسح Bluetooth LE، مولّد كلمات مرور قوية.
- **أدوات متقدمة:** فاحص شهادة SSL، حاسبة الشبكات الفرعية، قارئ بانر الخدمات، مقارنة سرعة خوادم DNS، أفضل قناة واي فاي، معلومات IP، الشركة المصنّعة للـMAC، وعدّاد حركة الشبكة المباشر.
- **خريطة الإشارة والسرعة:** قِس قوة الواي فاي وسرعة التحميل الفعلية في كل غرفة وشاهد المناطق الضعيفة.
- **جدار ناري للتطبيقات:** احجب الإنترنت عن تطبيقات محددة عبر VPN محلي، مع سجل بمحاولات الاتصال المحجوبة.
- **استهلاك البيانات لكل تطبيق:** أي التطبيقات تستهلك واي فاي وبيانات الجوال (اليوم/7 أيام/30 يوماً).
- **رادار التجسس والمتعقّبات:** كشف متعقّبات BLE (AirTag وTile وSmartTag) وشبكات واي فاي مشبوهة (توأم مزيف، فخاخ، فيض شبكات وهمية). كشف فقط، لا يرسل شيئاً.
- **كاشف الكاميرات:** يُظهر كاميرات المراقبة وأجهزة DVR/NVR على الشبكة (ONVIF، منافذ RTSP، أسماء الشركات). لا يحاول تسجيل الدخول.
- **مشاركة الملفات:** إرسال واستقبال الملفات بين أجهزة NetScout على نفس الشبكة، مع قبول يدوي لكل ملف.
- **لوحة HTML قابلة للمشاركة، ودجت للشاشة الرئيسية، وزر سريع في الإعدادات السريعة.**
- **الأمان:** فحص الراوتر (Telnet وFTP وUPnP والمنافذ الخطرة).
- **الواي فاي:** معلومات الاتصال الحالي، وتحليل الشبكات القريبة (القنوات، الإشارة، التشفير).
- **الإنترنت:** اختبار سرعة (تحميل/رفع/زمن استجابة)، IP العام، ورسم بياني لسجل النتائج.
- **التقارير:** تصدير CSV وPDF.
- **الواجهة:** عربي/إنجليزي مع RTL، وضع فاتح/داكن، و6 ألوان أساسية.

## حدود يجب معرفتها
- أندرويد 10 وما بعده يمنع قراءة عناوين MAC في الغالب، لذلك قد لا يظهر MAC لبعض الأجهزة. الأجهزة التي تستخدم MAC عشوائياً (أغلب الهواتف) تظهر كـ"عنوان خاص" بلا شركة مصنّعة.
- الفحص الدوري بالخلفية قد يتأخر بسبب توفير البطارية.
- اختبار السرعة وDNS يستخدمان خوادم Cloudflare، وIP العام يستخدم ipinfo.io. لا يُرسل شيء آخر.
- لا يوجد جهاز Fing Box ولا حسابات سحابية.
- الجدار الناري يحجب التطبيقات فقط ولا يراقب وجهات الاتصال لبقية التطبيقات، ولا يدعم أجهزة الراديو (RTL-SDR/HackRF) ولا كشف الـdeauth.

## التثبيت
نزّل ملف APK من صفحة **Releases**، ثم فعّل "التثبيت من مصادر غير معروفة". النسخة موقّعة بمفتاح إصدار ثابت، فيمكن تحديثها فوق النسخ التالية.

## البناء من المصدر
المتطلبات: JDK 17 وGradle 8.9 وAndroid SDK 35.
```bash
gradle assembleDebug
```
الناتج في `app/build/outputs/apk/debug/`. أو شغّل `build.yml` من تبويب Actions في GitHub (يبني ويوقّع وينشر Release تلقائياً عند إنشاء وسم `v*`). قاعدة الشركات الكاملة تُنزّل من IEEE أثناء البناء.

## التقنيات
Kotlin، Jetpack Compose (Material 3)، Coroutines، WorkManager.

## الترخيص
MIT

---

## English

A free, open-source, ad-free Android app that shows what is going on inside your Wi-Fi network: who is connected, whether your router is safe, and how your internet is doing. Everything runs on your device. No account is needed and nothing is sent to a server.

> Independent project, not affiliated with any commercial app.

### Features
- **Devices:** discovery (ping sweep, reverse DNS, mDNS, NetBIOS, SSDP/UPnP), device type and vendor guess, nicknames and notes, first/last seen.
- **Intruder alerts:** mark your devices as known and get a notification when a new one appears (periodic background check).
- **Tools:** Ping, Traceroute, DNS, WHOIS, port scanner, Wake-on-LAN, HTTP check, Bluetooth LE scanner, password generator.
- **Advanced tools:** SSL certificate inspector, subnet calculator, service banner grabber, DNS speed benchmark, best Wi-Fi channel, IP lookup, MAC vendor lookup, live traffic meter.
- **Signal & speed map:** measure Wi-Fi strength and real download speed room by room.
- **App firewall:** cut chosen apps off the internet using a local VPN, with a log of blocked connection attempts.
- **Data usage per app:** which apps use Wi-Fi and mobile data (today / 7 / 30 days).
- **Surveillance radar:** detects BLE trackers (AirTag, Tile, SmartTag) and suspicious Wi-Fi (fake twins, honeypots, fake-network floods). Detection only, nothing is transmitted.
- **Camera finder:** shows IP cameras and DVR/NVR recorders on your network (ONVIF, RTSP ports, vendor names). It never tries to log in.
- **File sharing:** send and receive files between NetScout devices on the same network, with manual accept for every file.
- **Shareable HTML dashboard, home-screen widget and Quick Settings tile.**
- **Security:** router check (Telnet, FTP, UPnP, risky ports).
- **Wi-Fi:** current connection info and nearby network analyzer (channels, signal, encryption).
- **Internet:** speed test (down/up/latency), public IP, and a history chart.
- **Reports:** CSV and PDF export.
- **UI:** Arabic/English with RTL, light/dark mode, 6 accent colors.

### Limitations
- Android 10+ usually blocks reading MAC addresses, so some devices show no MAC. Devices using randomized MACs (most phones) are shown as "private address" with no vendor.
- Background checks can be delayed by battery optimization.
- Speed test and DNS use Cloudflare; public IP uses ipinfo.io. Nothing else is sent.
- No Fing Box hardware and no cloud accounts.
- The firewall only blocks apps; it does not capture the destinations of other apps, and there is no radio hardware support (RTL-SDR/HackRF) or deauth detection.

### Install
Download the APK from **Releases** and allow installs from unknown sources. Builds are signed with a fixed release key, so updates install over each other.

### Build
Requires JDK 17, Gradle 8.9, Android SDK 35.
```bash
gradle assembleDebug
```
Output: `app/build/outputs/apk/debug/`. Or run `build.yml` from the Actions tab (it builds, signs and publishes a Release when a `v*` tag is created). The full vendor list is downloaded from IEEE at build time.

### Tech
Kotlin, Jetpack Compose (Material 3), Coroutines, WorkManager.

### License
MIT
