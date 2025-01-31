# Discord Board Push Listener

## Einleitung

Dieses Repository dient als Beispiel wie ein Bot für das Plugin "Discord-Push: Forum" aussehen könnte. Es sollte nur von erfahrenen Benutzern mit Programmierkenntnissen genutzt werden. Es gibt keinen offiziellen Support für dieses Projekt.

## Start with Docker

Voraussetzungen:
- Docker muss installiert sein

Anleitung:
1. Kone das Repository (z.B. via Konsole: `git@github.com:HanashiDev/discord-push-board-listener.git`)
2. Benenne die Datei `config/config.json.dist` in `config/config.json` um.
3. Fülle die Datei `config/config.json` aus. Siehe dazu weiter unten "Config ausfüllen".
4. Starte auf der Konsole `docker build . -t "discord-push"` um das Docker Image zu bauen.
5. Starte `docker run --name discord-push -d discord-push` um das Tool zu starten.

## Start with pm2

Voraussetzung:
- NodeJS muss installiert sind

Anleitung:
1. Kone das Repository (z.B. via Konsole: `git@github.com:HanashiDev/discord-push-board-listener.git`)
2. Benenne die Datei `config/config.json.dist` in `config/config.json` um.
3. Fülle die Datei `config/config.json` aus. Siehe dazu weiter unten "Config ausfüllen".
4. Installiere Abhängigkeiten via Konsole `npm install -g typescript pm2`
5. Führe auf der Konsole `npm install` aus.
6. Starte `pm2 start ecosystem.config.json` um das Tool zu starten

## Config ausfüllen

**botToken:** der Bot-Token vom Discord-Bot

**guildID:** die ID des Discord-Servers

**webhookURL:** die Webhook-Url für Discord-Push Forum, kann im ACP unter "Konfiguration > Discord > Forum > Geheimer Schlüssel für richtigen Bot" in der Beschreibung eingesehen werden.

**secret:** der geheime Schlüssel für den Webhook, kann im ACP unter "Konfiguration > Discord > Forum > Geheimer Schlüssel für richtigen Bot" eingesehen und verändert werden.
