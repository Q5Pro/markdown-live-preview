# 📝 Markdown Live Preview

Yazarken sağ tarafta **anında** önizlemesini gösteren, tek dosyalık,
bağımlılıksız bir Markdown editörü. İnternet bağlantısı veya kurulum
gerektirmez.

## Özellikler

- ⚡ Anlık önizleme (her tuş vuruşunda güncellenir)
- 📐 Başlıklar, kalın/italik/üstü çizili metin
- 💻 Satır içi kod ve dil etiketli kod blokları
- 🔗 Linkler ve görseller
- 📋 Sıralı ve sıralı olmayan listeler
- 📊 Tablolar
- 💬 Alıntı blokları (blockquote)
- ➖ Yatay çizgiler
- 💾 İçeriği `.md` dosyası olarak indirme
- 📏 Anlık kelime/karakter sayacı
- 📱 Mobil uyumlu (dar ekranlarda paneller alt alta dizilir)

## Kullanım

Kurulum gerekmez:

```bash
open index.html        # macOS
xdg-open index.html     # Linux

# veya
python3 -m http.server 8000
```

Sol paneldeki metin kutusuna Markdown yazın, sağ panelde anında
biçimlendirilmiş halini görün. "İndir (.md)" butonuyla içeriği dosya
olarak kaydedebilirsiniz.

## Neden bağımlılıksız bir Markdown ayrıştırıcı?

Çoğu Markdown editörü `marked.js`, `markdown-it` gibi kütüphanelere
bağımlıdır. Bu proje, **sıfırdan yazılmış, ~150 satırlık hafif bir
ayrıştırıcı** içerir — eğitim amaçlı olarak Markdown'ın nasıl
ayrıştırılabileceğini göstermek ve hiçbir `npm install` adımı
gerektirmeden tek dosya olarak çalışabilmek için.

**Not:** Bu ayrıştırıcı, yaygın kullanılan Markdown söz dizimini
kapsar ama CommonMark spesifikasyonunun tam bir uygulaması değildir
(örn. iç içe listeler, HTML blokları gibi kenar durumlar
desteklenmeyebilir). Üretim ortamında tam uyumluluk gerekiyorsa
`marked` veya `markdown-it` gibi olgun kütüphaneler tercih edilmelidir.

## Teknik notlar

- Saf JavaScript, framework yok, harici kütüphane yok
- XSS koruması için tüm kullanıcı girdisi `escapeHtml()` ile kaçırılır
  (kod blokları ve inline kod dahil)
- Kod span'leri (`` `kod` ``), inline biçimlendirme (kalın/italik)
  uygulanmadan önce geçici olarak korunur, böylece kod içindeki `*`
  veya `_` karakterleri yanlışlıkla biçimlendirilmez

## Lisans

MIT
