# 在 Linux 上安装

翻译： [english](LINUX.md), [esperanto](LINUX.eo.md), [español](LINUX.es.md), [العربية](LINUX.ar.md), [português](LINUX.pt.md), [русский](LINUX.ru.md), [bahasa](LINUX.id.md), [türkçe](LINUX.tr.md), [български](LINUX.bg.md)

---

我不是安装键盘布局的专家，这些说明可能不适用于所有 Linux 用户.

## 请遵循这些说明

**1.** 首先，通过运行这些命令备份一些文件:

```bash
cp /usr/share/X11/xkb/symbols/epo /usr/share/X11/xkb/symbols/epo.old
cp /usr/share/X11/xkb/rules/evdev.xml /usr/share/X11/xkb/rules/evdev.xml.old
```

如果出现错误，请首先运行以下命令： `su -l root`, 然后尝试再次运行命令，或将“cp”替换为“sudo cp”.

**2.** 打开文件 `/usr/share/X11/xkb/symbols/epo` 并将以下文本块附加到文件末尾:

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

**3.** 打开文件 `/usr/share/X11/xkb/rules/evdev.xml` 并在变体后面插入以下文本块 `Esperanto (legacy)`:

```xml
<variant>
  <configItem>
    <name>colemak_eo</name>
    <description>Esperanto (Colemak)</description>
  </configItem>
</variant>
```

**4.** 然后加 `Esperanto (Colemak)` 通过桌面环境的设置.

## 正在卸载

要卸载，请恢复旧文件或撤消您所做的一切:

```bash
mv /usr/share/X11/xkb/symbols/epo.old /usr/share/X11/xkb/symbols/epo
mv /usr/share/X11/xkb/rules/evdev.xml.old /usr/share/X11/xkb/rules/evdev.xml
```

## 正在更新

卸载旧版本并安装新版本.

---

此页面包含自动翻译的文本

---

[← 返回](./README.zh-CN.md)
