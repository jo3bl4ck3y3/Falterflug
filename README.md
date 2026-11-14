# Falterflug

Android-Spiel: Ein Schmetterling kreist um Blüten. Tippen lässt ihn geradeaus losfliegen,
trifft er die nächste Blüte, kreist er dort weiter.

## APK bauen

Bei jedem Push auf `main` baut GitHub Actions die APK automatisch.

1. Im Repository auf **Actions** gehen und den neuesten Lauf **APK bauen** öffnen.
2. Unten unter **Artifacts** die Datei **Falterflug-APK** herunterladen (ZIP mit `app-debug.apk`).
3. Die APK aufs Handy kopieren und öffnen. Android fragt einmal nach der Erlaubnis,
   Apps aus dieser Quelle zu installieren.

Von Hand starten: **Actions → APK bauen → Run workflow**.

## Spiel ändern

Das ganze Spiel steckt in `app/src/main/assets/index.html`.
Für eine neue Version in `app/build.gradle` die `versionCode` um 1 erhöhen.

## Hinweis zum Schlüssel

`app/falterflug.keystore` signiert die APK, damit Updates die alte Version ersetzen.
Das Passwort steht offen in `app/build.gradle`. Für ein privates Spiel reicht das,
für den Play Store bräuchte es einen geheimen Schlüssel.
