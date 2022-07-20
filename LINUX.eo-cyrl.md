# Инстали ен Линуксо

Ен алиай лингвой: [English](LINUX.md), [Esperanto](LINUX.eo.md), [Есперанто](LINUX.eo-cyrl.md)

---

Малферму `/usr/share/X11/xkb/symbols/epo` кай алдону ла секван текстоблокон ал ла фино де ла досиеро

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

Малферму `/usr/share/X11/xkb/rules/evdev.xml` кай енигу ла секван текстоблокон пост ла варианто `Esperanto (legacy)`

```
<variant>
  <configItem>
    <name>colemak_eo</name>
    <description>Esperanto (Colemak)</description>
  </configItem>
</variant>
```

Посте алдону `Esperanto (Colemak)` пер ла агордой де виа фенестрило \(DE\)

Се малсукцесе, сенду проблемон \(issue\) ал чи тиу гит депонейо че [GitHub.com](https://github.com/salif/colemak-eo/issues/new/choose)
