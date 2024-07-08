# Инсталиране в Linux

Превод: [english](LINUX.md), [esperanto](LINUX.eo.md), [中文](LINUX.zh-CN.md), [español](LINUX.es.md), [العربية](LINUX.ar.md), [português](LINUX.pt.md), [русский](LINUX.ru.md), [bahasa](LINUX.id.md), [türkçe](LINUX.tr.md)

---

Първо архивирайте някои файлове. Изпълнете тези команди:

```bash
cp /usr/share/X11/xkb/symbols/epo /usr/share/X11/xkb/symbols/epo.old
cp /usr/share/X11/xkb/rules/evdev.xml /usr/share/X11/xkb/rules/evdev.xml.old
```

Отворете файла `/usr/share/X11/xkb/symbols/epo` и добавете следния текстов блок в края на файла

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

Отворете файла `/usr/share/X11/xkb/rules/evdev.xml` и вмъкнете следния текстов блок след варианта `Esperanto (legacy)`.

```xml
<variant>
  <configItem>
    <name>colemak_eo</name>
    <description>Esperanto (Colemak)</description>
  </configItem>
</variant>
```

След това добавете `Esperanto (Colemak)` чрез настройките на вашата работна среда.

## Деинсталиране

За да деинсталирате, отменете всичко, което сте направили, или възстановете старите файлове:

```bash
mv /usr/share/X11/xkb/symbols/epo.old /usr/share/X11/xkb/symbols/epo
mv /usr/share/X11/xkb/rules/evdev.xml.old /usr/share/X11/xkb/rules/evdev.xml
```

## Актуализиране

Деинсталирайте старата версия и инсталирайте новата версия.

---

Тази страница съдържа автоматично преведен текст

---

[← Назад](./README.bg.md)
