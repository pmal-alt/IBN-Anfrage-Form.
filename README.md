# IBN-Anfrage-Form

Ein einzelnes HTML-Dokument (`IBN anfrage nice looking one  (2).htm`) enthält das komplette Formular inklusive Styling und JavaScript, um die Daten über [Formspree](https://formspree.io/) zu versenden.

## Formular anzeigen

1. Lade dieses Repository als ZIP herunter **oder** klone es (`git clone …`).
2. Öffne die Datei `IBN anfrage nice looking one  (2).htm` per Doppelklick im Browser. Alle Assets sind eingebettet.
3. Alternativ kannst du im Projektordner einen Mini-Webserver starten, z. B.:
   ```bash
   python3 -m http.server 8000
   ```
   und dann `http://localhost:8000/IBN%20anfrage%20nice%20looking%20one%20%20(2).htm` aufrufen.

## Häufige Stolperfallen

| Problem | Lösung |
| --- | --- |
| Online-Editor (z. B. W3Schools, CodePen, StackBlitz) zeigt keine Reaktion beim Absenden. | Viele Editoren blockieren externe `fetch`-Anfragen. Öffne die Datei stattdessen direkt im Browser oder starte sie lokal über `python -m http.server`. |
| Es kommt eine Fehlermeldung von Formspree. | Prüfe, ob das Formular-Feld „E-Mail“ ausgefüllt ist und ob die verwendete Formspree-Form (`https://formspree.io/f/xvgvjdlj`) für deine E-Mail-Adresse freigeschaltet ist. |
| Formular lädt nach Fehlern neu. | In sehr restriktiven Umgebungen wechselt das Script automatisch auf den klassischen Formspree-Submit und zeigt anschließend deren Bestätigungsseite. |

## Formspree anpassen

- Ersetze bei Bedarf die `action`-URL im `<form>`-Tag durch deine eigene Formspree-Endpunkt-ID.
- Passe die Betreffzeile über das versteckte Feld `_subject` an.
- Wenn du andere Pflichtfelder benötigst, ergänze sie im Formular und in der `validateStrict()`-Routine.
