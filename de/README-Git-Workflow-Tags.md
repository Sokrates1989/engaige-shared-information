
Verbesserung der Übersichtlichkeit durch Fallnummer und Tags in Git

---

**Hallo Stefan,**

um die Übersichtlichkeit in Git zu verbessern, schlage ich folgende Optimierung vor: Du hattest Dir ja eine bessere Nachverfolgung anhand der Kanban Nummer gewünscht.

### Aktuelle Praxis:
- Wir nutzen die Fallnummer aus dem Kanban-Board (z. B. `FA-YY-X`) in den Git-Commit-Nachrichten.
- Beispiel:  
  ```bash
  git commit -m "FA-YY-X: Beschreibung der Änderung"
  ```

### Optimierungsvorschlag:
Zusätzlich zu den Commit-Nachrichten könnte ein **Git-Tag** mit derselben Fallnummer verwendet werden. Tags bieten die Möglichkeit, spezifische Änderungen direkt und übersichtlich in GitHub/GitLab zu referenzieren. 

#### Vorteile:
1. **Bessere Nachverfolgbarkeit**: Tags ermöglichen es, Commits schneller zu finden, da sie direkt sichtbar in der Git-Oberfläche angezeigt werden.
2. **Übersichtlichkeit für Nicht-Entwickler**: Als Manager können Sie direkt anhand der Tags nachvollziehen, welche Änderungen zu einem spezifischen Fall gehören, ohne tief in die Commit-Historie einzutauchen.
3. **Einfache Integration in bestehende Workflows**: Das Hinzufügen von Tags ist unkompliziert und stört bestehende Abläufe nicht.

#### Umsetzung:
- Nach dem Erstellen eines Commits wird ein Tag mit der Fallnummer hinzugefügt:  
  ```bash
  git tag FA-YY-X
  ```
- Anschließend werden Commit und Tag gemeinsam gepusht:  
  ```bash
  git push --follow-tags
  ```
  (Dieser Befehl pusht sowohl den Commit als auch das zugehörige Tag.)

### Beispiel:
1. Commit mit Fallnummer:
   ```bash
   git commit -m "FA-123-45: Fix für Berechnungsfehler"
   ```
2. Tag hinzufügen:
   ```bash
   git tag FA-123-45
   ```
3. Commit und Tag pushen:
   ```bash
   git push --follow-tags
   ```

Das Ergebnis ist eine klar strukturierte Historie, in der sowohl Commits als auch Tags die Fallnummer enthalten. Dadurch wird die Übersichtlichkeit, insbesondere für Manager in GitLab/GitHub, erheblich verbessert.

---

**Ich freue mich auf Ihr Feedback oder weitere Vorschläge!**

**Viele Grüße**  
Patrick
