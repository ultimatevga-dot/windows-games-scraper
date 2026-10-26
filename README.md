# Windows Games Scraper

A portable, Zero-API Python scraper for PC games (Batocera/RetroBat/EmulationStation). It downloads metadata, clear logos, covers, and high-quality YouTube gameplays automatically, without needing API keys or user accounts.

## Características / Features
* **Zero API:** No requiere claves de SteamGridDB, RAWG ni de YouTube. Totalmente anónimo.
* **Interfaz Oscura Nativa:** Interfaz gráfica desarrollada en Tkinter con un tema oscuro y sin dependencias externas complejas.
* **Multi-idioma:** Soporte integrado para Español, Inglés, Italiano, Francés y Portugués.
* **Descarga de Gameplays Inteligente:** Usa `yt-dlp` para extraer resultados rápidos y `ffmpeg` para descargar, recortar a 30 segundos (con audio) y convertir a `.mp4` (H.264/AAC).
* **Filtros Anti-Spoilers:** Descarta automáticamente tráileres de películas, vídeos de consolas (PS5, Switch) y canciones.

## Cómo usarlo / How to use
1. Coloca tu archivo `gamelist.xml` en la misma carpeta que el programa.
2. Ejecuta `scraper.exe`.
3. Selecciona tu idioma en el menú desplegable.
4. Haz clic en **Iniciar Scraping**.
5. El programa te irá preguntando de forma interactiva qué vídeos quieres descargar para cada juego.

## Compilación / Build
Si deseas compilar el código fuente tú mismo usando PyInstaller, necesitas tener `ffmpeg.exe` y `ffprobe.exe` en la carpeta y usar el siguiente comando para incrustarlos en el binario final:
`pyinstaller --noconsole --onefile --add-binary "ffmpeg.exe;." --add-binary "ffprobe.exe;." scraper.py`
