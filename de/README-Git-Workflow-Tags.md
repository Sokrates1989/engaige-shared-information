
### Verbesserung der Übersichtlichkeit durch Fallnummer und Tags in Git

---

**Hallo Stefan,**

um die Übersichtlichkeit in Git zu verbessern, schlage ich folgende Optimierung vor: Du hattest Dir ja eine bessere Nachverfolgung anhand der Kanban-Nummer gewünscht.

---

### Aktuelle Praxis:
- Wir nutzen die Fallnummer aus dem Kanban-Board (z. B. `FA-YY-X`) in den Git-Commit-Nachrichten.
- Beispiel:  
  ```bash
  git commit -m "FA-YY-X: Beschreibung der Änderung."
  ```

---

### Optimierungsvorschlag:
Zusätzlich zu den Commit-Nachrichten könnte ein **Git-Tag** mit derselben Fallnummer verwendet werden. Tags bieten die Möglichkeit, spezifische Änderungen direkt und übersichtlich in GitLab/GitHub zu referenzieren.

#### Vorteile:
1. **Bessere Nachverfolgbarkeit**: Tags ermöglichen es, Commits schneller zu finden, da sie direkt sichtbar in der Git-Oberfläche angezeigt werden.
2. **Übersichtlichkeit für Nicht-Entwickler**: Manager können anhand der Tags nachvollziehen, welche Änderungen zu einem spezifischen Fall gehören, ohne tief in die Commit-Historie eintauchen zu müssen.
3. **Einfache Integration in bestehende Workflows**: Das Hinzufügen von Tags ist unkompliziert und stört bestehende Abläufe nicht.

---

### Aktualisierte Workflow-Umsetzung:

#### Schritte:
1. **Commit mit Fallnummer erstellen**:
   ```bash
   git commit -m "FA-YY-X: Beschreibung der Änderung."
   ```

2. **Tag hinzufügen**:
   ```bash
   git tag FA-YY-X
   ```

3. **Commit pushen**:
   ```bash
   git push
   ```

4. **Tag separat pushen**:
   ```bash
   git push --tags
   ```

---

#### Alternative: Commit und Tag zusammen pushen:
Falls nur ein einzelnes Tag gepusht werden soll, kann das spezifische Tag explizit angegeben werden:
   ```bash
   git push origin FA-YY-X
   ```

---

### Beispiel:
1. **Commit erstellen**:
   ```bash
   git commit -m "FA-123-45: Fix für Berechnungsfehler."
   ```

2. **Tag hinzufügen**:
   ```bash
   git tag FA-123-45
   ```

3. **Push Workflow:**
   - Commit pushen:
     ```bash
     git push
     ```
   - Tag pushen:
     ```bash
     git push --tags
     ```

---

### Ergebnis:
Das Ergebnis ist eine klar strukturierte Historie in GitLab/GitHub, in der sowohl Commits als auch Tags die Fallnummer enthalten. Manager und Entwickler profitieren gleichermaßen von der verbesserten Übersichtlichkeit.

---

**Ich freue mich auf Dein Feedback oder weitere Vorschläge!**

**Viele Grüße**  
Patrick
