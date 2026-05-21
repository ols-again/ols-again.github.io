# JSPLAY – Modern Full Page Video Player

**Geliştirici:** oyuncunettv / OLS Develop

---

## Tanım

JSPLAY, YouTube tarzı modern, full-page video oynatıcıdır. DRM içermez ve minimalist bir tasarıma sahiptir. Tek videoyu oynatmak için tasarlanmıştır ve playlist sunmaz. Desteklenen video formatlarını Blob olarak yükleyerek basit bir gizleme sağlar ve HLS (M3U8) akışlarını doğrudan oynatır. Video dışındaki dosyalar (PDF, ZIP, TXT vb.) düz dosya olarak yüklenir. Kontroller, kullanıcı deneyimi açısından modern bir video player hissi verir ve özelleştirilebilir.

---

## Özellikler

- **Tam Sayfa Video:** Video ekranın tamamını kaplar ve responsive olarak görüntülenir.  
- **Blob Mantığı:** MP4, MKV, MOV, AVI, WebM gibi desteklenen video formatları tarayıcıda Blob olarak gösterilir.  
- **HLS Desteği:** M3U8 formatları direkt oynatılır, Blob kullanılmaz.  
- **Video Dışı Dosyalar:** PDF, ZIP, EXE gibi dosyalar düz dosya olarak yüklenir.  
- **Oynat / Durdur Butonu:** Tek butonla video oynatma ve durdurma, simge duruma göre ▶ / ⏸ değişir.  
- **İlerleme Çubuğu:** Alt kısımda klasik YouTube tarzı kontrol çubuğu; video konumu gösterir ve kaydırılarak değiştirilebilir.  
- **Ses Kontrolü:** 0–100% ses ayarı, mevcut ses kanalları korunur.  
- **Hız Kontrolü:** 0.25x – 10x arasında oynatma hızı değiştirilebilir.  
- **Ayarlar Menüsü:** Alt yazı ekleme ve gelecekte ses kanalı seçeneklerini destekler.  
- **Altyazı Desteği:** VTT/SRT/ASS formatında altyazılar eklenebilir ve varsayılan olarak aktif edilebilir.  
- **Minimal Tasarım:** Gereksiz UI öğeleri yok, modern ve temiz arayüz.  
- **DRM’siz:** Video üzerinde herhangi bir DRM veya kısıtlama yoktur.  
- **Kolay Genişletilebilir:** Tema, ek kontroller veya playlist desteği eklemek mümkündür.

---

## Kullanımı

### 1. Player Dosyasını Sunucuya Yükleyin

- JSPLAY bir HTML dosyasıdır (`player.html`).  
- Bu dosyayı sitenizin uygun bir klasörüne yükleyin, örneğin `/player/` klasörü.  

### 2. Video Dosyalarını Hazırlayın

- JSPLAY video URL’lerini parametre olarak alır.  
- Desteklenen video formatları: MP4, MKV, MOV, AVI, WebM, WMV, FLV, VOB, MPG, MPEG, DIVX, RM, RMVB, 3GP, ASF, MXF, R3D, BRAW, ARI, OGV  
- Videonuz sunucuda erişilebilir olmalı, örneğin `/videos/movie.mp4`.  

### 3. Altyazı Dosyalarını Hazırlayın (Opsiyonel)

- Desteklenen formatlar: VTT, SRT, ASS  
- SRT ve ASS dosyaları JSPLAY tarafından otomatik VTT’ye dönüştürülür.  
- Videonuzla aynı klasörde veya erişilebilir bir dizinde bulunabilir.  

### 4. Player’a Video ve Altyazı URL’si Gönderin

JSPLAY URL parametreleri ile video ve altyazıyı alır:

`/player/player.html?video=/videos/movie.mp4&sub=/subtitles/movie.vtt`

- `video` parametresi videonun sunucudaki yolunu gösterir.  
- `sub` parametresi (opsiyonel) altyazı dosyasının yolunu gösterir.  

### 5. HTML Sayfanızdan Link veya Iframe ile Açın

- **Iframe ile gömme:**

```html
<iframe src="/player/player.html?video=/videos/movie.mp4&sub=/subtitles/movie.vtt"
        width="100%" height="600px" frameborder="0" allowfullscreen>
</iframe>
```

- Ayrı izleme sayfası olarak link verme:

```<a href="/player/player.html?video=/videos/movie.mp4&sub=/subtitles/movie.vtt">Videoyu İzle</a>```

### 6. Örnek Kullanım URL'leri

- Video:

```/player/player.html?video=/videos/movie.mp4```

- Video + Alt Yazı:

```/player/player.html?video=/videos/movie.mp4&sub=/subtitles/movie.vtt```

---

© 2026 oyuncunettv / OLS Develop
