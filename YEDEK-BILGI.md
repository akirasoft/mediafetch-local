# LOCAL (Windows) Yedek — MediaFetch

Bu klasör, projenin **sunucuya taşınmadan önceki** Windows/localhost sürümünün
birebir kopyasıdır. Tarih: 2026-09-27

## İçerik
- `server.js` — 127.0.0.1:3434 dinleyen, Windows'a özel (yt-dlp.exe, ffmpeg.exe,
  WinGet taraması, `explorer`, `start http://...`) orijinal sürüm.
- `extension/` — sadece `http://localhost:3434` adresine bağlanan orijinal eklenti.
- `public/` — web arayüzü (yeni tasarım).
- `bin/yt-dlp.exe` — Windows ikilisi.
- `_eski-arayuz-yedek/` — projedeki eski arayüz yedeği (dokunulmadı).

## Dahil edilmeyenler
- `node_modules/` → `npm install` ile geri gelir.
- `.git/` → asıl klasörde duruyor.
- `downloads/` → indirilen dosyalar.

## Bu yedeği çalıştırma
```
npm install
node server.js
```
Tarayıcı otomatik olarak http://localhost:3434 adresinde açılır.

## Neden duruyor?
Asıl klasördeki sürüm; Ubuntu + Pterodactyl + uzak sunucu (Chrome eklentisi
uzaktaki sunucuya bağlanacak şekilde) için dönüştürüldü. Bir şey ters giderse
bu klasör, çalışan Windows sürümüne dönmek için referanstır.
