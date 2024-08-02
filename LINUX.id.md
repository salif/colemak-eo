# Menginstal di Linux

Terjemahan: [english](LINUX.md), [esperanto](LINUX.eo.md), [中文](LINUX.zh-CN.md), [español](LINUX.es.md), [العربية](LINUX.ar.md), [português](LINUX.pt.md), [русский](LINUX.ru.md), [türkçe](LINUX.tr.md), [български](LINUX.bg.md)

---

Saya bukan ahli dalam memasang tata letak keyboard, petunjuk ini mungkin tidak berfungsi untuk semua pengguna Linux.

## Ikuti petunjuk ini

**1.** Pertama, buat cadangan beberapa file dengan menjalankan perintah ini:

```bash
cp /usr/share/X11/xkb/symbols/epo /usr/share/X11/xkb/symbols/epo.old
cp /usr/share/X11/xkb/rules/evdev.xml /usr/share/X11/xkb/rules/evdev.xml.old
```

Jika Anda mendapatkan kesalahan, jalankan perintah ini terlebih dahulu: `su -l root`, lalu coba jalankan kembali perintahnya, atau ganti `cp` dengan `sudo cp`.

**2.** Membuka file `/usr/share/X11/xkb/symbols/epo` dan tambahkan blok teks berikut di akhir file:

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

**3.** Membuka file `/usr/share/X11/xkb/rules/evdev.xml` dan masukkan blok teks berikut setelah varian `Esperanto (legacy)`:

```xml
<variant>
  <configItem>
    <name>colemak_eo</name>
    <description>Esperanto (Colemak)</description>
  </configItem>
</variant>
```

**4.** Lalu tambahkan `Esperanto (Colemak)` melalui pengaturan lingkungan desktop Anda.

## Menghapus instalasi

Untuk menghapus instalan, pulihkan file lama atau batalkan semua yang Anda lakukan:

```bash
mv /usr/share/X11/xkb/symbols/epo.old /usr/share/X11/xkb/symbols/epo
mv /usr/share/X11/xkb/rules/evdev.xml.old /usr/share/X11/xkb/rules/evdev.xml
```

## Memperbarui

Copot pemasangan versi lama dan pasang versi baru.

---

Halaman ini berisi teks yang diterjemahkan secara otomatis

---

[← Kembali](./README.id.md)
