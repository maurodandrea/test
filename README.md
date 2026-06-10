# VidGen — Generatore di video per YouTube

SaaS 100% gratuito che genera video "faceless" per YouTube direttamente nel browser. Nessun server, nessuna API a pagamento, nessuna registrazione.

## Funzionalità

- **Editor a scene**: scrivi lo script, una scena per paragrafo
- **3 stili visivi**: foto reali con effetto Ken Burns, gradienti animati, dark con particelle
- **Musica royalty-free** generata proceduralmente (Web Audio API): ambient, misteriosa o allegra
- **Render in browser**: Canvas + MediaRecorder → file WebM 1280×720 pronto per YouTube
- **Generatore di miniature** 1280×720 in 3 stili (PNG)
- **Helper SEO**: titoli alternativi, descrizione con capitoli/timestamp, tag
- **Progetti salvati** in localStorage
- **Anteprima TTS** dello script (voce del browser, italiano)

## Tecnologie (tutte gratuite)

| Componente | Servizio | Costo |
|---|---|---|
| Immagini di sfondo | picsum.photos (no API key) | 0 € |
| Musica | Web Audio API (procedurale) | 0 € |
| Render video | Canvas + MediaRecorder | 0 € |
| Hosting | GitHub Pages | 0 € |

## Deploy su GitHub Pages (5 minuti)

1. Crea un repository su GitHub (es. `vidgen`), pubblico
2. Carica `index.html` nel repository (drag & drop da web o `git push`)
3. Vai su **Settings → Pages**
4. In **Source** scegli `Deploy from a branch`, branch `main`, cartella `/ (root)`, poi **Save**
5. Dopo ~1 minuto il sito è online su `https://TUO-USERNAME.github.io/vidgen/`

## Uso

1. Scrivi titolo e script (scene separate da riga vuota)
2. Scegli stile, seed immagini, durata e musica
3. **Anteprima** per controllare, poi **Genera video**
4. Scarica il `.webm` e caricalo su YouTube (formato supportato nativamente)
5. Genera miniatura e suggerimenti SEO dalle altre schede

## Note

- Il render avviene in tempo reale: un video di 30 s richiede 30 s
- Non chiudere/minimizzare la scheda durante la registrazione
- Per convertire in MP4 (opzionale): `ffmpeg -i video.webm video.mp4`
- Browser consigliati: Chrome o Edge
