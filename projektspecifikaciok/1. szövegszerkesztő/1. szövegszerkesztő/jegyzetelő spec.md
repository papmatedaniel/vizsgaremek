**Jegyzetelő alkalmazás specifikáció**

**1\. Célkitűzés**

Egy olyan nyílt forráskódú, ingyenes, offline és online módban is működő, multiplatformos jegyzetelő alkalmazás fejlesztése, amely a jegyzetelés minden aspektusát lefedi: struktúrált tartalomkezelés, valósidejű kollaboráció, szinkronizációs megbízhatóság és AI-alapú kézírásfelismerés.

**2\. Alapfunkciók**

**2.1 Jegyzetelés**

- Rich text szerkesztő
- Beágyazott elemek: képek, linkek, listák, checkboxok, kódrészletek
- Címkézés, mappákba rendezés
- Drag & drop jegyzet-átrendezés

**2.2 Offline működés**

- Teljes funkcionalitás internetkapcsolat nélkül
- Lokális adattárolás (pl. SQLite, IndexedDB)
- Offline-változatok üsszehangolása szinkron után

**2.3 Szinkronizáció**

- Automatikus és kézi szinkron mód
- Konfliktuskezelés (CRDT, last-write-wins vagy merge rendszer)
- Szerveroldali biztonságos tárolás (opcionális)

**2.4 Felhasználói testreszabás**

- Funkciók ki-/bekapcsolhatósága
- Használati komplexitás szint (1-10): kevesebb funkció, egyszerűbb felület, haladó beállítások

**3\. Haladó funkciók**

**3.1 Valósidejű kollaboráció**

- Egy jegyzet többen is szerkeszthetik egyszerre
- Módosítások azonnal láthatóak mindenkinél
- Ki szerkeszt éppen kijelzés
- Változatkövetés, history

**3.2 Megosztás**

- Link alapú megosztás (olvasás/szerkesztés jogosultsággal)
- Meghívás emaillel/profilszinten
- Megosztott mappák, projektek

**3.3 AI-alapú funkciók**

- Kézírás-felismerés
  - Offline futó OCR motor (pl. Tesseract, TensorFlow Lite)
  - Magyar, angol, kínai nyelvi támogatás
  - Egyéni íráskép tanítása
  - Fotó alapún jegyzet beszkennelése
- Szövegkihúzás PDF-ből, weboldalról, dokumentumból

**4\. Technológiai követelmények**

**4.1 Platformtámogatás**

- Android (API 21+, Samsung, Huawei, stb.)
- iOS (iPhone 7+)
- Linux (Debian/Ubuntu alap)
- Windows 10+
- macOS (Catalina+)
- Böngészős webapp (Chrome, Firefox, Safari, Edge)

**4.2 Technológiák**

- Flutter vagy React Native (mobilra)
- Electron vagy Tauri (asztali verzió)
- React + Node.js + WebSocket (webes és backend szinkron)
- SQLite vagy PouchDB lokális adattár
- Git vagy CRDT-alapú valósidejű motor
- OCR: TensorFlow Lite / Tesseract (offline)

**5\. Adatbiztonság és mentés**

- Titkosított adattárolás (AES-256)
- Lokális és felhős mentési lehetőség
- Export és import funkciók (Markdown, PDF, HTML)

**6\. Tervezett fejlesztési fázisok**

**Fázis 1 - MVP**

- Jegyzetelés alapfunkciói
- Offline működés
- Egyszerű szinkronizálás egy eszköz és a webapp között

**Fázis 2**

- Felhasználói profilok, beállítások
- Megosztás, jogosultságkezelés
- Multiplatformos build

**Fázis 3**

- Valósidejű kollaboráció
- AI-alapú OCR
- Testreszabható felhasználói felület

**7\. Licencelés és közösségi bevonás**

- Nyílt forráskód (pl. MIT vagy GPLv3)
- Közösségi fejlesztés GitHub-on keresztül
- Dokumentáció, issue tracker, feature request rendszer

**8\. Célközönség**

- Diákok
- Tanárok
- Tartalomkészítők
- Fejlesztők és tech mániások
- Jegyzetelni szerető átlagfelhasználók

**9\. Küldött cél**

Egy olyan eszköz létrehozása, amely képes kiváltani a jelenlegi Notion, Obsidian és hasonló platformokat, de úgy, hogy a bonyolultságot lecseréljük intuitivitásra, az online-only működést lecseréljük teljes kontrollra, és a korlátokat lehetőségekké alakítjuk.