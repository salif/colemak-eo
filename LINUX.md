# Install on Linux

In other languages: [English](LINUX.md), [Esperanto](LINUX.eo.md), [Есперанто](LINUX.eo-cyrl.md), [𐑧𐑕𐑐𐑧𐑮𐑨𐑵𐑑𐑩](LINUX.eo-shaw.md)

---

Open `/usr/share/X11/xkb/symbols/epo` and append the following text block at the end of the file

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

Open `/usr/share/X11/xkb/rules/evdev.xml` and insert the following text block after the `Esperanto (legacy)` variant

```
<variant>
  <configItem>
    <name>colemak_eo</name>
    <description>Esperanto (Colemak)</description>
  </configItem>
</variant>
```

Then add `Esperanto (Colemak)` via the settings of your desktop environment

If unsuccessful, submit an issue to this git repository at [GitHub.com](https://github.com/salif/colemak-eo/issues/new/choose)
