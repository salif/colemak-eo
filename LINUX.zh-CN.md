# 在 Linux 上安装

<span><svg xmlns="http://www.w3.org/2000/svg" width="15" height="15" fill="none"
style="vertical-align: sub;" viewBox="0 0 24 24" stroke="currentColor"
stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path
class="st0" d="M2,16c0.1,0,8-5,9-7c0.6-1.3,1-5,1-5h3H1h7V1" /><line
class="st0" x1="4" y1="8" x2="12" y2="16" /><polygon class="st0"
points="15,19 21,19 23,23 18,11 13,23 " /></svg> : [english](LINUX.md), [esperanto](LINUX.eo.md), [español](LINUX.es.md), [العربية](LINUX.ar.md), [português](LINUX.pt.md), [русский](LINUX.ru.md), [bahasa](LINUX.id.md), [türkçe](LINUX.tr.md), [български](LINUX.bg.md)</span>

---

首先，备份一些文件。运行这些命令:

```shell
cp /usr/share/X11/xkb/symbols/epo /usr/share/X11/xkb/symbols/epo.old
cp /usr/share/X11/xkb/rules/evdev.xml /usr/share/X11/xkb/rules/evdev.xml.old
```

打开文件 `/usr/share/X11/xkb/symbols/epo` 并将以下文本块附加到文件末尾

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

打开文件 `/usr/share/X11/xkb/rules/evdev.xml` 并在后面插入以下文本块 `Esperanto (legacy)` variant.

```xml
<variant>
  <configItem>
    <name>colemak_eo</name>
    <description>Esperanto (Colemak)</description>
  </configItem>
</variant>
```

然后加 `Esperanto (Colemak)` 通过桌面环境的设置.

## 正在卸载

要卸载，请撤消您所做的一切或恢复旧文件:

```
mv /usr/share/X11/xkb/symbols/epo.old /usr/share/X11/xkb/symbols/epo
mv /usr/share/X11/xkb/rules/evdev.xml.old /usr/share/X11/xkb/rules/evdev.xml
```

## 正在更新

卸载旧版本并安装新版本.

---

此页面包含自动翻译的文本

---

[← 返回](./README.zh-CN.md)
