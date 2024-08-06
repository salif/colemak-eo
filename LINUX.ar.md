# التثبيت على لينكس

ترجمة: [english](LINUX.md), [esperanto](LINUX.eo.md), [中文](LINUX.zh-CN.md), [español](LINUX.es.md), [português](LINUX.pt.md), [русский](LINUX.ru.md), [bahasa](LINUX.id.md), [türkçe](LINUX.tr.md), [български](LINUX.bg.md)

---

أنا لست خبيرًا في تثبيت تخطيطات لوحة المفاتيح، وقد لا تعمل هذه التعليمات مع جميع مستخدمي Linux.

## اتبع هذه التعليمات

**1.** أولاً، قم بعمل نسخة احتياطية لبعض الملفات عن طريق تشغيل هذه الأوامر:

```bash
cp /usr/share/X11/xkb/symbols/epo /usr/share/X11/xkb/symbols/epo.old
cp /usr/share/X11/xkb/rules/evdev.xml /usr/share/X11/xkb/rules/evdev.xml.old
```

إذا حصلت على خطأ، قم أولاً بتشغيل هذا الأمر: `su root`, ثم حاول تشغيل الأوامر مرة أخرى، أو استبدل `cp` بـ`sudo cp`.

**2.** افتح الملف `/usr/share/X11/xkb/symbols/epo` وقم بإلحاق الكتلة النصية التالية في نهاية الملف:

```
// github.com/salif/colemak-eo
partial alphanumeric_keys
xkb_symbols "colemak_eo" {

  include "us(colemak)"

  name[Group1]= "Esperanto (Colemak)";

  key <AD01> {[ jcircumflex, Jcircumflex, q,            Q          ]};
  key <AD02> {[ scircumflex, Scircumflex, w,            W          ]};
  key <AD09> {[ ubreve,      Ubreve,      y,            Y          ]};
  key <AD11> {[ gcircumflex, Gcircumflex, bracketleft,  braceleft  ]};
  key <AD12> {[ hcircumflex, Hcircumflex, bracketright, braceright ]};
  key <AB02> {[ ccircumflex, Ccircumflex, x,            X          ]};

  include "level3(ralt_switch)"
};
```

**3.** افتح الملف `/usr/share/X11/xkb/rules/evdev.xml` وأدخل الكتلة النصية التالية بعد المتغير `Esperanto (legacy)`:

```xml
<variant>
  <configItem>
    <name>colemak_eo</name>
    <description>Esperanto (Colemak)</description>
  </configItem>
</variant>
```

**4.** ثم أضف `Esperanto (Colemak)` من خلال إعدادات بيئة سطح المكتب لديك.

## إلغاء التثبيت

لإلغاء التثبيت، قم باستعادة الملفات القديمة أو التراجع عن كل ما قمت به:

```bash
mv /usr/share/X11/xkb/symbols/epo.old /usr/share/X11/xkb/symbols/epo
mv /usr/share/X11/xkb/rules/evdev.xml.old /usr/share/X11/xkb/rules/evdev.xml
```

## تحديث

قم بإلغاء تثبيت الإصدار القديم وتثبيت الإصدار الجديد.

---

تحتوي هذه الصفحة على نص مترجم تلقائيًا

---

[← العودة](./README.ar.md)
