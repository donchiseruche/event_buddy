# EventBuddy

EventBuddy ist eine Webanwendung für Studierende, um Events und Angebote (z. B. Unterkünfte oder Fahrten) einfach zu entdecken, zu reservieren und miteinander in Kontakt zu treten.  
Das Projekt ist vollständig in **HTML, CSS und JavaScript** umgesetzt und speichert Zustände (Authentifizierung, Reservierungen, Profilinformationen) **clientseitig im LocalStorage**.

---

## Architekturüberblick

- **Frontend**  
  - Reines HTML/CSS/JS, responsive mit [Bootstrap 5](https://getbootstrap.com) und [Font Awesome](https://fontawesome.com).  

- **Persistenz (Simulation)**  
  - `localStorage` wird genutzt für Authentifizierungsstatus, Userprofil, Reservierungen und Nachrichten.  
  - Beispiel-Daten liegen als statische JSON-Dateien (`events.json`, `angebote.json`) vor.  

- **Struktur (wichtige Dateien)**  
  - `index.html` – Startseite, Eventliste mit Suche & Filter  
  - `event.html` – Detailseite für ein Event  
  - `angebote.html` – Liste aller Angebote (Unterkunft/Fahrt)  
  - `angebot-erstellen.html` – Formular zum Erstellen neuer Angebote  
  - `chat.html` – 1:1 Chat-Simulation zwischen Benutzern  
  - `profile.html` – Benutzerprofil, Bearbeitung persönlicher Daten  
  - `reservations.html` – Übersicht aller eigenen Reservierungen  
  - `login.html` / `register.html` / `forgot-password.html` – Authentifizierungsseiten  
  - `events.json`, `angebote.json` – Beispieldaten  

---

## Lokale Entwicklung

Voraussetzungen:  
- [Node.js](https://nodejs.org) oder [Python](https://www.python.org) für einfachen Dev-Server  
- Alternativ: Docker & Docker Compose  

### Variante 1: Lokaler HTTP-Server

```bash
# Mit Node.js (http-server)
npm install -g http-server
http-server . -p 8080
````

Danach ist die Anwendung erreichbar unter:
[http://localhost:8080](http://localhost:8080)

---

## Deployment

Das Projekt ist für **statisches Hosting** konzipiert und benötigt keinen Anwendungsserver.
---

## Erweiterbarkeit

EventBuddy ist modular aufgebaut. Typische Erweiterungspunkte:

* **Backend-Anbindung**: Ersetzen der LocalStorage-Simulation durch eine REST-API.
* **Authentifizierung**: Integration von OAuth 2.0 oder OpenID Connect.
* **Echte Datenbank**: Speicherung von Events, Angeboten und Reservierungen in einer relationalen DB oder NoSQL.
* **Realtime**: Nutzung von WebSockets für den Chat.
* **CI/CD**: Automatisierte Builds und Tests über Jenkins (siehe `Jenkinsfile`).

---

## Zielgruppe

Die Anwendung richtet sich primär an Studierende, die Events, Mitfahrgelegenheiten oder Unterkünfte finden, organisieren und verwalten möchten.
Das Projekt dient gleichzeitig als **Prototyp/Demonstrator** für moderne Frontend-Architekturen ohne komplexes Backend.



---
