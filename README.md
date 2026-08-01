# 🎵 My Hits (Music Timeline Game)

Ein webbasiertes, lokales Multiplayer-Partyspiel im Stil bekannter Musik-Jahreszahlen-Spiele. Spiele mit deinen Freunden an einem Gerät, errate das Erscheinungsjahr von Songs und baue deinen eigenen Zeitstrahl auf!

Das Besondere: Du bist nicht auf vorgegebene Songs beschränkt. Dank der direkten Spotify-Anbindung kannst du **jede beliebige Spotify-Playlist** nutzen!

## ✨ Features

* **Eigene Playlists:** Füge einfach den Link zu einer Spotify-Playlist ein (Voraussetzung: Du hast sie selbst erstellt oder sie ist öffentlich).
* **Lokaler Multiplayer:** Füge beliebig viele Spieler hinzu und spielt abwechselnd an einem Gerät (PC, Tablet oder Smartphone).
* **Touch-optimiert:** Einfache Klick-Mechanik zum Platzieren der Karten – perfekt für den Touchscreen am Tisch.
* **Integrierter Player:** Die Songs werden direkt im Browser über das Spotify-Widget abgespielt.
* **Sicher:** Nutzt den modernen Spotify OAuth 2.0 (PKCE) Flow. Keine Zugangsdaten werden gespeichert!

## 🚀 Installation & Setup

Damit das Spiel deine Spotify-Playlists abrufen kann, musst du es mit deiner eigenen Spotify Developer App verknüpfen.

### 1. Spotify App erstellen
1. Gehe zum [Spotify Developer Dashboard](https://developer.spotify.com/dashboard) und logge dich ein.
2. Klicke auf **"Create App"**.
3. Vergib einen Namen (z.B. "My Hits Game") und eine Beschreibung.
4. Trage unter **Redirect URIs** die genaue URL ein, unter der dein Spiel erreichbar sein wird (z.B. `http://localhost:5500` für lokale Tests oder `https://Silvihi95.github.io/my-hits/` für GitHub Pages).
5. Klicke auf Save.

### 2. Client ID eintragen
1. Kopiere im Spotify Dashboard in den Einstellungen deiner App die **Client ID**.
2. Öffne die `index.html` dieses Spiels in einem Texteditor.
3. Suche die Konstante `CLIENT_ID` (ca. in Zeile 110) und ersetze sie mit deiner ID:
   ```javascript
   const CLIENT_ID = 'DEINE_CLIENT_ID_HIER';
