# Instali en Linukso

En aliaj lingvoj: [English](LINUX.md), [Esperanto](LINUX.eo.md), [Есперанто](LINUX.eo-cyrl.md), [𐑧𐑕𐑐𐑧𐑮𐑨𐑵𐑑𐑩](LINUX.eo-shaw.md)

---

Malfermu `/usr/share/X11/xkb/symbols/epo` kaj aldonu la sekvan tekstoblokon al la fino de la dosiero

```
// github.com/salif/colemak-eo
partial alphanumeric_keys
xkb_symbols "colemak_eo" {

  include "us(colemak)"

  name[Group1]= "Esperanto (Colemak)";

  key <AD01> {[ jcircumflex, Jcircumflex, q,            Q          ]};
  key <AD02> {[ scircumflex, Scircumflex, w,            W          ]};
  key <AD09> {[ ubreve,      Ubreve,      y,            Y          ]};
  key <AD10> {[ gcircumflex, Gcircumflex, semicolon,    colon      ]};
  key <AC11> {[ hcircumflex, Hcircumflex, apostrophe,   quotedbl   ]};
  key <AB02> {[ ccircumflex, Ccircumflex, x,            X          ]};

  include "level3(ralt_switch)"
};
```

Malfermu `/usr/share/X11/xkb/rules/evdev.xml` kaj enigu la sekvan tekstoblokon post la varianto `Esperanto (legacy)`

```
<variant>
  <configItem>
    <name>colemak_eo</name>
    <description>Esperanto (Colemak)</description>
  </configItem>
</variant>
```

Poste aldonu `Esperanto (Colemak)` per la agordoj de via fenestrilo \(DE\)

Se malsukcese, sendu problemon \(issue\) al ĉi tiu git deponejo ĉe [GitHub.com](https://github.com/salif/colemak-eo/issues/new/choose)
