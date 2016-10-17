## LernMoment's TypeScript Startprojekt

> Hinweis: möchtest du nur ein paar Zeilen TypeScript schreiben, dann ist es einfacher den [TypeScript Playground](http://www.typescriptlang.org/play/) zu verwenden. Da brauchst du nichts lokal zu installieren.

Gerade um TypeScript zu lernen mache ich häufig einige Übungsaufgaben bei denen ich einfach nur eine Art Konsolenprogramm erstelle. Um die Entwicklung möglichst einfach zu halten spare ich somit den Webserver und sonstige Build-Werkzeuge ein. Dieses Projekt dient als Basis für genau solche Übungen.

Du kannst dieses Projekt entweder direkt von der Konsole, also lediglich mit einem Texteditor, verwenden, oder auch in einer Entwicklungsumgebung wie [VS Code](https://code.visualstudio.com/).

### Voraussetzungen

Möchtest du das Projekt direkt von der Konsole verwenden, dann brauchst du lediglich `node` inkl. `npm` auf deinem Rechner installiert haben.

Falls du eine Entwicklungsumgebung wie VS Code verwenden möchtest, brauchst du zusätzlich noch TypeScript. Das kannst du dir mit `npm install -g typescript` installieren. Dann würde ich dir auch empfehlen `tslint` global zu installieren (`npm install -g tslint`). Um `tslint` direkt in VS Code zu verwenden gibt es die [TSLint extension](https://marketplace.visualstudio.com/items?itemName=eg2.tslint) von Erich Gamma! 

### Ein Projekt starten

Um dieses Projekt als Ausgangsbasis für eine Übung oder ähnliches zu verwenden kannst du einfach folgende Befehle auf der Konsole verwenden:

```
git clone https://github.com/LernMoment/typescript-console-seed.git
cd typescript-console-seed
npm install
npm start
```

Mit diesen Befehlen lädst du dir den Quellcode in ein Verzeichnis mit dem Namen `typescript-console-seed`, wechselst in das Verzeichnis, lässt [npm](https://www.npmjs.com) alle Abhängigkeiten laden und startest dann das Kompilieren und Ausführen. Als Bestätigung, dass alles geklappt hat, wirst du die Ausgabe *Hello Seed Project!* auf der Konsole finden.

### Anpassen für dein Projekt / Übung

Sobald das Projekt bei dir läuft, kannst du anfangen es an deine Vorstellungen anzupassen. Ich würde dafür folgende Änderungen machen:

 1. Den Verzeichnisnamen ändern
 2. Die bisherige Git-Historie löschen (`rm -rf .git`) und das Verzeichnis neu für git initialisieren (`git init`)
 3. Die TypeScript-Datei `hello-seed.ts` umbenennen in etwas was zu deinem Projekt passt oder wenigstens in `app.ts`
 4. In der Datei `package.json` das Skript `mon` anpassen. Dort solltest du anstelle von `hello-seed.ts` den Namen der Datei verwenden in der deine Anwendung gestartet wird (beispielsweise den Namen aus dem vorherigen Schritt.
 5. Einige weitere Eigenschaften in der `package.json` wie zum Beispiel *author* und *name* anpassen
 6. Erneut `npm start` ausführen und überprüfen, dass die Anwendun noch immer läuft

### Quellcode entwickeln

Das Projekt ist so aufgesetzt, dass Änderungen an TypeScript-Dateien automatisch erkannt werden, wenn du speicherst. D.h. wenn du `npm start` ausgeführt hast, kannst du beispielsweise eine Änderung in `hello-seed.ts` (oder jeder beliebigen anderen Datei) vornehmen und speichern. Danach wird diese Datei erneut kompiliert und `node` führt die neu erstellten JavaScript-Dateien dann erneut aus. Du siehst also eine Ausgabe.

Damit kannst du sehr leicht und schnell deinen Quellcode schreiben und bekommst sofort Rückmeldung. 

Als weiteres Skript kannst du `npm run lint` ausführen. Damit wird `tslint` in der Standardkonfiguration ausgeführt und zeigt dir an, ob du alle Richtlinien (best practices) eingehalten hast. Diese Richtlinien kannst du mit der Datei `tslint.json` anpassen. 
