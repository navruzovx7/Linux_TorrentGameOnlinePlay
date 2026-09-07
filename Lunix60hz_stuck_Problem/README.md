# Lunix 60Hz Takılı Kalma — Profesyonel Rehber / Professional Guide

<!-- keywords: Lunix 60Hz takıldı, linux 60hz stuck, 60hz takılı kalma, refresh rate stuck linux, hyprland 60hz -->

Türkçe özet
Bu depo, Lunix/Hyprland ve genel Linux ortamlarında görülen "ekran yenileme oranının 60Hz'de takılı kalması" sorununu çözmek için yapılandırılmış, adım adım uygulanabilecek bir rehber sunar. Rehber hem teknik detayları hem de kullanıcıya yönelik komut örneklerini içerir.

English summary
This repository contains a polished, step-by-step guide to diagnose and fix the "display refresh rate stuck at 60Hz" issue on Lunix/Hyprland and similar Linux setups. It includes troubleshooting steps, configuration examples, and guidance for producing reproducible bug reports.

Repository contents
- Lunix-60Hz-stuck-fix-guide.md — Detaylı, iki dilli çözüm şablonu (ana rehber).
- images/ — Ekran görüntüleri ve diyagramlar için klasör (ekleyin: screenshot-1.png, example-setup.png).
- CONTRIBUTING.md — Nasıl katkıda bulunulur; katkı kuralları ve dosya adlandırma.
- LICENSE — Lisans dosyası (MIT önerilmektedir).

Quick start (Hazır olmak için)
1. Rehberi düzenleyin: [Lunix-60Hz-stuck-fix-guide.md](/home/nvr/Documents/Cachy/Lunix60hz_stuck_Problem/Lunix-60Hz-stuck-fix-guide.md) dosyasının "Fix (Step-by-step)" bölümüne kendi çözümünüzü ekleyin.
2. Görselleri ekleyin: images/ klasörüne ekran görüntülerinizi yükleyin (örn. `screenshot-1.png`).
3. Commit & push: Aşağıdaki örnek adımlarla yerel değişiklikleri commit edin ve kendi GitHub reposuna push edin.

Git örneği

```bash
# Değişiklikleri sahneleme
git add .
# Commit — mesaj formatı: Lunix 60Hz fix: kısa açıklama
git commit -m "Lunix 60Hz fix: apply hyprland monitor block + validation"
# Push (uzak repo eklendikten sonra)
git push origin main
```

How to make this repo visible on GitHub
- Repo adı önerisi: `lunix-60hz-fix-guide` veya `lunix-display-refresh-fix` (SEO için anahtar kelime içerir).
- README başlığına ve ilk paragrafına anahtar kelimeleri (ör. "Lunix 60Hz", "linux 60hz stuck") ekledik — bu, GitHub aramalarında görünürlüğü artırır.

Görseller (Images)
- images/ klasörüne ekleyeceğiniz dosya isimlendirme önerileri:
  - `screenshot-1.png` — xrandr / hyprctl çıktısı
  - `monitors-config-example.png` — monitors.lua konfigürasyonundan görüntü
  - `before-after-hz.png` — önce/sonra gösterimi
- Görseller README içinde `![alt metin](images/screenshot-1.png)` biçiminde referans verin.

Katkıda bulunma
Lütfen CONTRIBUTING.md dosyasını okuyun. Küçük düzeltmeler için Pull Request, geniş değişikliklerde issue açarak tartışma başlatın.

Licensing / Lisans
Bu depoda MIT lisansı önerilmiştir. Lisansın eklenmesini istiyorsanız LICENSE dosyasını güncelleyin.

