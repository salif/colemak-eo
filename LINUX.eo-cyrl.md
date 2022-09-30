# Инстали ен Линуксо

Ен алиай лингвой: [English](LINUX.md), [Esperanto](LINUX.eo.md), [Есперанто](LINUX.eo-cyrl.md), [𐑧𐑕𐑐𐑧𐑮𐑨𐑵𐑑𐑩](LINUX.eo-shaw.md)

---

Малферму на `/usr/share/X11/xkb/symbols/epo` кай алдону ла секван текстоблокон ал ла фино де ла досиеро

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

Малферму на `/usr/share/X11/xkb/rules/evdev.xml` кай енигу ла секван текстоблокон пост ла варианто `Esperanto (legacy)`

```
<variant>
  <configItem>
    <name>colemak_eo</name>
    <description>Esperanto (Colemak)</description>
  </configItem>
</variant>
```

Посте алдону на `Esperanto (Colemak)` пер ла агордой де виа фенестрило \(DE\)

Се малсукцесе, сенду проблемон \(issue\) ал чи тиу гит депонейо че [GitHub.com](https://github.com/salif/colemak-eo/issues/new/choose)

[Малантаўен](./README.eo-cyrl.md)
