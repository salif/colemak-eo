# ๐ฆ๐ต๐๐๐จ๐ค๐ฆ ๐ง๐ต ๐ค๐ฆ๐ต๐ช๐๐๐ฉ

๐ง๐ต ๐จ๐ค๐ฆ๐จ๐ข ๐ค๐ฆ๐ต๐๐๐ฉ๐ข: [English](LINUX.md), [Esperanto](LINUX.eo.md), [ะัะฟะตัะฐะฝัะพ](LINUX.eo-cyrl.md), [๐ง๐๐๐ง๐ฎ๐จ๐ต๐๐ฉ](LINUX.eo-shaw.md)

---

๐ซ๐จ๐ค๐๐ง๐ฎ๐ซ๐ช `/usr/share/X11/xkb/symbols/epo` ๐๐จ๐ข ๐จ๐ค๐๐ฉ๐ต๐ช ๐ค๐จ ๐๐ง๐๐๐จ๐ต ๐๐ง๐๐๐๐ฉ๐๐ค๐ฉ๐๐ฉ๐ต ๐จ๐ค ๐ค๐จ ๐๐ฆ๐ต๐ฉ ๐๐ง ๐ค๐จ ๐๐ฉ๐๐ฆ๐ง๐ฎ๐ฉ

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

๐ซ๐จ๐ค๐๐ง๐ฎ๐ซ๐ช `/usr/share/X11/xkb/rules/evdev.xml` ๐๐จ๐ข ๐ง๐ต๐ฆ๐๐ช ๐ค๐จ ๐๐ง๐๐๐จ๐ต ๐๐ง๐๐๐๐ฉ๐๐ค๐ฉ๐๐ฉ๐ต ๐๐ฉ๐๐ ๐ค๐จ ๐๐จ๐ฎ๐ฆ๐จ๐ต๐๐ฉ `Esperanto (legacy)`

```
<variant>
  <configItem>
    <name>colemak_eo</name>
    <description>Esperanto (Colemak)</description>
  </configItem>
</variant>
```

๐๐ฉ๐๐๐ง ๐จ๐ค๐๐ฉ๐ต๐ช `Esperanto (Colemak)` ๐๐ง๐ฎ ๐ค๐จ ๐จ๐๐ฉ๐ฎ๐๐ฉ๐ข ๐๐ง ๐๐ฆ๐จ ๐๐ง๐ต๐ง๐๐๐ฎ๐ฆ๐ค๐ฉ \(DE\)

๐๐ง ๐ซ๐จ๐ค๐๐ช๐๐๐ง๐๐ง, ๐๐ง๐ต๐๐ช ๐๐ฎ๐ฉ๐๐ค๐ง๐ซ๐ฉ๐ต \(issue\) ๐จ๐ค ๐๐ฆ ๐๐ฆ๐ช ๐๐ฆ๐ ๐๐ง๐๐ฉ๐ต๐ง๐ข๐ฉ ๐๐ง [GitHub.com](https://github.com/salif/colemak-eo/issues/new/choose)
