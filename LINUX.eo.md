# Instalado en Linukso

Traduko: [english](LINUX.md), [中文](LINUX.zh-CN.md), [español](LINUX.es.md), [العربية](LINUX.ar.md), [português](LINUX.pt.md), [русский](LINUX.ru.md), [bahasa](LINUX.id.md), [türkçe](LINUX.tr.md), [български](LINUX.bg.md)

---

Unue, sekurigu iujn dosierojn. Rulu ĉi tiujn komandojn:

```bash
cp /usr/share/X11/xkb/symbols/epo /usr/share/X11/xkb/symbols/epo.old
cp /usr/share/X11/xkb/rules/evdev.xml /usr/share/X11/xkb/rules/evdev.xml.old
```

Malfermu dosieron `/usr/share/X11/xkb/symbols/epo` kaj aldonu la sekvan tekstoblokon ĉe la fino de la dosiero

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

Malfermu dosieron `/usr/share/X11/xkb/rules/evdev.xml` kaj enigu la sekvan tekstoblokon post la varianto `Esperanto (legacy)`.

```xml
<variant>
  <configItem>
    <name>colemak_eo</name>
    <description>Esperanto (Colemak)</description>
  </configItem>
</variant>
```

Poste aldonu `Esperanto (Colemak)` per la agordoj de via labortabla medio.

## Malinstalado

Por malinstali malfaru ĉion, kion vi faris aŭ restarigi la malnovajn dosierojn:

```bash
mv /usr/share/X11/xkb/symbols/epo.old /usr/share/X11/xkb/symbols/epo
mv /usr/share/X11/xkb/rules/evdev.xml.old /usr/share/X11/xkb/rules/evdev.xml
```

## Ĝisdatigo

Malinstalu la malnovan version kaj instalu la novan version.

---

Ĉi tiu paĝo enhavas aŭtomate tradukitan tekston

---

[← Reen](./README.eo.md)
