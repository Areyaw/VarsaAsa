# VARSA ASA: REYAMAW — Episode 1: Aku Adalah Dirimu
Prototype visual novel PC (HTML/CSS/JS murni, tanpa backend).

## Menjalankan
- Cepat: buka `index.html` di Chrome/Edge.
- Disarankan: `python -m http.server 8000` lalu buka http://localhost:8000
- GitHub Pages: Settings → Pages → Branch `main` / root.

## Struktur
- `data/ep01_scene01.js` — seluruh dialog (edit di sini untuk menulis adegan)
- `js/engine.js` dialog, pilihan, ekspresi, transisi · `js/main.js` menu & input · `js/audio.js` · `js/save.js` (localStorage)
- `assets/` — video menu, background, karakter, audio

## Penamaan aset (huruf kecil, underscore, tanpa spasi)
- `assets/video/menu_bg.mp4` (1920x1080, H.264, tanpa suara, loop) + `menu_bg_poster.jpg`
- `assets/backgrounds/bg_room_dusk.jpg` (1920x1080)
- `assets/characters/mawmaw/mawmaw_<ekspresi>.png` · `assets/characters/innerchild/innerchild_<ekspresi>.png` (PNG transparan, ukuran kanvas sama)
- Ekspresi Maw Maw: neutral happy smirk confused shocked embarrassed annoyed sad serious laughing
- Ekspresi inner child: neutral happy excited confused crying angry determined mischievous worried hopeful
- Audio: `assets/audio/music/bgm_*.mp3`, `assets/audio/sfx/sfx_*.ogg` (belum dipakai; audio saat ini disintesis)

## Memakai gambar asli
Di `js/engine.js` ubah `USE_IMAGES={bg:true,chars:true}`.

## Save
Progres otomatis di `localStorage` (satu browser, satu perangkat). Hapus data browser = save hilang.
