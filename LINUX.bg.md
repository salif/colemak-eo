# Инсталиране в Linux

Превод: [english](LINUX.md), [esperanto](LINUX.eo.md), [中文](LINUX.zh-CN.md), [español](LINUX.es.md), [العربية](LINUX.ar.md), [português](LINUX.pt.md), [русский](LINUX.ru.md), [bahasa](LINUX.id.md), [türkçe](LINUX.tr.md)

---

Не съм експерт в инсталирането на клавиатурни подредби, тези инструкции може да не работят за всички потребители на Linux.

## Следвайте тези инструкции

**1.** Първо архивирайте някои файлове, като изпълните тези команди:

```bash
cp /usr/share/X11/xkb/symbols/epo /usr/share/X11/xkb/symbols/epo.old
cp /usr/share/X11/xkb/rules/evdev.xml /usr/share/X11/xkb/rules/evdev.xml.old
```

Ако получите грешка, първо изпълнете тази команда: `su root`, след това опитайте да изпълните командите отново или заменете `cp` със `sudo cp`.

**2.** Отворете файла `/usr/share/X11/xkb/symbols/epo` и добавете следния текстов блок в края на файла:

```
// homepage: salif.github.io/colemak-eo
// version: 1
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

**3.** Отворете файла `/usr/share/X11/xkb/rules/evdev.xml` и вмъкнете следния текстов блок след варианта `Esperanto (legacy)`:

```xml
<variant>
  <configItem>
    <name>colemak_eo</name>
    <description>Esperanto (Colemak)</description>
  </configItem>
</variant>
```

**4.** След това добавете `Esperanto (Colemak)` чрез настройките на вашата работна среда.

## Деинсталиране

За да деинсталирате, възстановете старите файлове или отменете всичко, което сте направили:

```bash
mv /usr/share/X11/xkb/symbols/epo.old /usr/share/X11/xkb/symbols/epo
mv /usr/share/X11/xkb/rules/evdev.xml.old /usr/share/X11/xkb/rules/evdev.xml
```

## Актуализиране

Деинсталирайте старата версия и инсталирайте новата версия.

Промените, които правите във файловете в директорията `/usr/share/X11/xkb`, ще бъдат загубени, когато пакетът, притежаващ тази директория, бъде актуализиран, например в Arch Linux този пакет се нарича `xkeyboard-config`. Трябва или да правите същите промени всеки път, когато актуализирате този пакет, или да изключите актуализациите за този пакет. Също така имате възможност да направите персонализиран пакет, който съдържа тези промени и замества оригиналния пакет.

---

[← Назад](./README.bg.md)
