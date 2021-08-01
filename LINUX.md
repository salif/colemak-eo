# Install on Linux

Put the following text block inside `/usr/share/X11/xkb/symbols/epo`

```
// github.com/salif/colemak-eo
partial alphanumeric_keys
xkb_symbols "colemak" {

  include "us(colemak)"

  name[Group1]= "Esperanto (Colemak)";

  key <AD01> {[ jcircumflex, Jcircumflex, q,            Q          ]};
  key <AD02> {[ scircumflex, Scircumflex, w,            W          ]};
  key <AD10> {[ gcircumflex, Gcircumflex, semicolon,    colon      ]};
  key <AD11> {[ ubreve,      Ubreve,      bracketleft,  braceleft  ]};
  key <AD12> {[ apostrophe,  quotedbl,    bracketright, braceright ]};
  key <AC11> {[ hcircumflex, Hcircumflex                           ]};
  key <AB02> {[ ccircumflex, Ccircumflex, x,            X          ]};

  include "level3(ralt_switch)"
};
```

Put the following text block inside `/usr/share/X11/xkb/rules/evdev.xml`

```
<variant>
  <configItem>
    <name>colemak</name>
    <description>Esperanto (Colemak)</description>
  </configItem>
</variant>
```

Then add `Esperanto (Colemak)` via your desktop environment's settings.

If it doesn't work then create an issue on this repository
