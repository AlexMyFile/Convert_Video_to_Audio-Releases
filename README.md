Convert Video To Audio
  Un'applicazione desktop sviluppata in Python con CustomTkinter, convertita in file 
  eseguibile (.exe) con inclusi ffmpeg.exe, ffplay.exe e ffprobe.exe.
  
  👉 Funziona standalone su Windows 10/11 senza necessità di installare Python o altre librerie.
  
  Convert Video To Audio è un'applicazione desktop intuitiva e facile da usare, progettata per estrarre l'audio dai file video e salvarlo in diversi formati audio di
  alta qualità. L'interfaccia grafica moderna, basata su CustomTkinter, offre un'esperienza utente fluida e piacevole.
  
<img width="800" height="613" alt="Screenshot" src="https://github.com/user-attachments/assets/7f62af86-68c8-46aa-b6a7-aa9c3274c27f" />

  Funzionalità Principali

   - Conversione Multi-Formato: Supporta la conversione nei formati audio più popolari:
       - MP3 (con bitrate a 320k)
       - FLAC (lossless)
       - AAC (con bitrate a 256k)
       - OGG (con bitrate a 320k)
       - WAV (lossless, non compresso)

   - Interfaccia Grafica Moderna: Realizzata con customtkinter per un aspetto scuro, pulito e professionale che si integra bene con i sistemi operativi moderni.

   - Anteprima della Copertina:
       - Estrazione Automatica: L'applicazione tenta di estrarre automaticamente un fotogramma dal video per usarlo come miniatura di anteprima. Utilizza FFmpeg come
         metodo primario e OpenCV come fallback.
       - Rilevamento Fotogrammi Neri: Ignora i fotogrammi neri o vuoti, considerandoli come un'estrazione fallita per garantire anteprime significative.
       - Caricamento Manuale: Se l'estrazione automatica fallisce o se si desidera una copertina personalizzata, è possibile caricarne una manualmente dal proprio
         computer.

   - Incorporamento della Copertina:
       - La copertina (estratta o caricata) viene incorporata direttamente nei metadati dei file MP3 e FLAC, in modo da essere visualizzata nei lettori multimediali.
       - Per i formati AAC, OGG e WAV, che hanno un supporto meno standardizzato per le copertine, l'applicazione avvisa l'utente e procede con la conversione senza
         incorporare l'immagine per garantire la massima compatibilità.

   - Esperienza Utente Fluida:
       - Processi in Background: Sia l'estrazione della miniatura che la conversione audio vengono eseguite in thread separati per evitare che l'interfaccia grafica si
         blocchi ("freeze").
       - Terminale di Stato: Un terminale integrato fornisce feedback in tempo reale sullo stato delle operazioni (es. "Estrazione in corso...", "Conversione...", "File
         salvato!").
       - Feedback Cromatico: I messaggi nel terminale sono colorati per una chiara e immediata comprensione: giallo per gli avvisi, verde per il successo e rosso per gli
         errori.

   - Gestione Semplice dei File:
       - Selezione Intuitiva: Pulsanti "Sfoglia" per selezionare facilmente il file video di input e la cartella di destinazione.
       - Destinazione Predefinita: La cartella di destinazione è impostata di default sulla cartella "Musica" del sistema, con un fallback alla cartella utente se non
         esiste.
       - Accesso Rapido: Un pulsante "Apri cartella di destinazione" permette di accedere rapidamente alla cartella contenente i file convertiti.

 Tecnologie Utilizzate

   - Python: Linguaggio di programmazione principale.
   - Tkinter / CustomTkinter: Per l'interfaccia grafica.
   - FFmpeg: Per l'elaborazione audio/video.
   - Pillow (PIL): Per la gestione e il salvataggio delle immagini di copertina.
   - OpenCV: Come metodo alternativo per l'estrazione delle miniature.

   

[Convert Video To Audio] è distribuito sotto la licenza **GNU General Public License v3**.

## Licenza
- Il codice di questo progetto è rilasciato con licenza **GPLv3**.
- Una copia della licenza è disponibile nel file [LICENSE](LICENSE).

## Terze parti
Questo pacchetto include:
- **FFmpeg (ffmpeg.exe, ffplay.exe, ffprobe.exe)**  
  Rilasciato con licenza **GPL v2 o successiva**.  
  Vedi il file [NOTICE-FFmpeg.txt](NOTICE-FFmpeg.txt) per dettagli.  

## Sorgenti
Il codice sorgente corrispondente a FFmpeg è disponibile qui:  
👉 https://ffmpeg.org/download.html

