# Установка в Linux

Перевод: [english](LINUX.md), [esperanto](LINUX.eo.md), [中文](LINUX.zh-CN.md), [español](LINUX.es.md), [العربية](LINUX.ar.md), [português](LINUX.pt.md), [bahasa](LINUX.id.md), [türkçe](LINUX.tr.md), [български](LINUX.bg.md)

---

Я не эксперт в установке раскладок клавиатуры, эти инструкции могут подойти не всем пользователям Linux.

## Следуйте этим инструкциям

**1.** Сначала создайте резервную копию некоторых файлов, выполнив эти команды:

```bash
cp /usr/share/X11/xkb/symbols/epo /usr/share/X11/xkb/symbols/epo.old
cp /usr/share/X11/xkb/rules/evdev.xml /usr/share/X11/xkb/rules/evdev.xml.old
```

Если вы получили сообщение об ошибке, сначала запустите эту команду: `su root`, затем попробуйте выполнить команды еще раз или замените `cp` на `sudo cp`.

**2.** Открыть файл `/usr/share/X11/xkb/symbols/epo` и добавьте следующий текстовый блок в конец файла:

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

**3.** Открыть файл `/usr/share/X11/xkb/rules/evdev.xml` и вставьте следующий текстовый блок после варианта `Esperanto (legacy)`:

```xml
<variant>
  <configItem>
    <name>colemak_eo</name>
    <description>Esperanto (Colemak)</description>
  </configItem>
</variant>
```

**4.** Затем добавьте `Esperanto (Colemak)` через настройки среды рабочего стола.

## Удаление

Чтобы удалить, восстановите старые файлы или отмените все, что вы сделали:

```bash
mv /usr/share/X11/xkb/symbols/epo.old /usr/share/X11/xkb/symbols/epo
mv /usr/share/X11/xkb/rules/evdev.xml.old /usr/share/X11/xkb/rules/evdev.xml
```

## Обновление

Удалите старую версию и установите новую версию.

---

Эта страница содержит автоматически переведенный текст

---

[← Назад](./README.ru.md)
