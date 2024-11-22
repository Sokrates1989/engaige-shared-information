
# Nutzung von Git-Tags zur schnelleren Nachverfolgung von Änderungen

### Tags anzeigen:
1. **In GitLab/GitHub:**
   - Navigieren Sie zur Übersicht des Projekts.
   - Öffnen Sie den Reiter **"Tags"** (meist unter **"Repository"** oder direkt in der Sidebar sichtbar).
   - Hier sehen Sie alle Tags, die für dieses Projekt erstellt wurden, zusammen mit den zugehörigen Commit-Nachrichten.

2. **Direkt im Terminal (optional):**
   Falls Sie Zugriff auf das Git-Repository im Terminal haben, können Sie folgende Befehle verwenden:
   ```bash
   git fetch --tags
   git tag
   ```
   Dies zeigt eine Liste aller verfügbaren Tags.

### Vorteile für Ihren Workflow:
- **Schnelle Zuordnung zu Kanban-Fällen:** Da die Tags die Fallnummer (z. B. `FA-123-45`) enthalten, können Sie direkt nachvollziehen, welche Änderungen zu welchem Fall gehören.
- **Direkter Zugriff auf Änderungen:** Ein Klick auf das Tag in GitLab/GitHub führt Sie direkt zum zugehörigen Commit und den Details der Änderung.
- **Übersichtlichkeit in Versionsständen:** Tags können auch genutzt werden, um Meilensteine (z. B. Release-Stände) zu markieren, wodurch die Projektübersicht weiter optimiert wird.

### Beispiel-Workflow:
1. **Projektübersicht öffnen:** Gehen Sie in GitLab/GitHub zum Reiter **"Tags"**.
2. **Tag auswählen:** Klicken Sie auf ein spezifisches Tag, z. B. `FA-123-45`.
3. **Änderungen einsehen:** Sie sehen sofort, welche Änderungen (Code, Dateien etc.) mit diesem Fall verknüpft sind, inklusive der Commit-Nachricht.

Dieser Workflow ermöglicht es, Änderungen schneller nachzuvollziehen, ohne tief in die Commit-Historie einzusteigen oder Entwickler um zusätzliche Informationen bitten zu müssen.
