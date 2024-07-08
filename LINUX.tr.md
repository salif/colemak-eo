# Linux'ta kurulum

Tercüme: [english](LINUX.md), [esperanto](LINUX.eo.md), [中文](LINUX.zh-CN.md), [español](LINUX.es.md), [العربية](LINUX.ar.md), [português](LINUX.pt.md), [русский](LINUX.ru.md), [bahasa](LINUX.id.md), [български](LINUX.bg.md)

---

Öncelikle bazı dosyaları yedekleyin. Bu komutları çalıştırın:

```bash
cp /usr/share/X11/xkb/symbols/epo /usr/share/X11/xkb/symbols/epo.old
cp /usr/share/X11/xkb/rules/evdev.xml /usr/share/X11/xkb/rules/evdev.xml.old
```

Açık dosya `/usr/share/X11/xkb/symbols/epo` ve aşağıdaki metin bloğunu dosyanın sonuna ekleyin

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

Açık dosya `/usr/share/X11/xkb/rules/evdev.xml` ve değişkenden sonra aşağıdaki metin bloğunu ekleyin `Esperanto (legacy)`.

```xml
<variant>
  <configItem>
    <name>colemak_eo</name>
    <description>Esperanto (Colemak)</description>
  </configItem>
</variant>
```

Sonra Ekle `Esperanto (Colemak)` masaüstü ortamınızın ayarları aracılığıyla.

## Kaldırma

Kaldırmak için yaptığınız her şeyi geri alın veya eski dosyaları geri yükleyin:

```bash
mv /usr/share/X11/xkb/symbols/epo.old /usr/share/X11/xkb/symbols/epo
mv /usr/share/X11/xkb/rules/evdev.xml.old /usr/share/X11/xkb/rules/evdev.xml
```

## Güncelleniyor

Eski sürümü kaldırın ve yeni sürümü yükleyin.

---

Bu sayfa otomatik olarak çevrilmiş metin içermektedir

---

[← Geri](./README.tr.md)
