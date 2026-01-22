🛍️ Bon Prix: Personalization Lab
Wirtschaftsinformatik Case Study: Hyper-Personalization via NLP

Willkommen im Personalization Lab. In dieser Session bauen wir einen KI-gestützten Shopping-Assistenten für bon prix, der Kundenrezensionen basierend auf individuellen Präferenzen zusammenfasst.

🛠️ 1. System-Voraussetzungen & Vorbereitung
Bevor wir in den Code eintauchen, müssen wir sicherstellen, dass Ihre Arbeitsumgebung bereit ist.

Schritt A: Python & JupyterLab

Wir nutzen JupyterLab als interaktive Entwicklungsumgebung.

Installieren Sie Python 3.10+ von python.org.

Öffnen Sie Ihr Terminal (Mac/Linux) oder die PowerShell (Windows) und installieren Sie die benötigten Pakete:

Bash
# Installation der Kern-Bibliotheken & Jupyter
pip install pandas gradio plotly python-dotenv jupyterlab ibm-watsonx-ai ollama langfuse
Schritt B: Das Repository vorbereiten

Laden Sie dieses Repository herunter oder klonen Sie es.

Stellen Sie sicher, dass die Dateien personalization_users_visible.csv und reviews_all_users_in_shop.csv im Hauptverzeichnis liegen.

🔑 2. Konfiguration (Die .env Datei)
Aus Sicherheitsgründen speichern wir API-Keys niemals direkt im Code. Wir nutzen dafür eine Umgebungsvariable-Datei.

Suchen Sie die Datei .env.template in Ihrem Ordner.

Benennen Sie diese Datei um in .env (löschen Sie das .template am Ende).

Öffnen Sie die Datei mit einem Texteditor und tragen Sie Ihre Zugangsdaten ein:

Variable	Beschreibung
WATSONX_API_KEY	Ihr persönlicher API-Key aus der IBM Cloud.
WATSONX_PROJECT_ID	Die ID Ihres watsonx Sandkastens/Projekts.
LANGFUSE_PUBLIC_KEY	Public Key aus den Langfuse-Projekteinstellungen.
LANGFUSE_SECRET_KEY	Secret Key aus den Langfuse-Projekteinstellungen.
📓 3. Auswahl des richtigen Notebooks
Je nach technischem Setup und Fokus der Session stehen Ihnen vier Varianten zur Verfügung:

Datei	Engine	Fokus
bonprix_lab-wx.ipynb	IBM watsonx.ai	Enterprise Cloud Lösung (Standard).
bonprix_lab-wx_tracing.ipynb	watsonx + Langfuse	Inklusive Prozess-Überwachung (Tracing).
bonprix_lab-ollama.ipynb	Ollama (Lokal)	Lokale KI-Inferenz (kein API-Key nötig).
bonprix_lab-ollama_tracing.ipynb	Ollama + Langfuse	Lokale KI mit voller Observability.
🚀 4. Starten des Labs
Sind alle Vorbereitungen getroffen? Dann geht es jetzt los:

Öffnen Sie Ihr Terminal im Projektordner.

Starten Sie JupyterLab mit folgendem Befehl:

Bash
jupyter lab
Ihr Browser öffnet sich automatisch. Wählen Sie das gewünschte Notebook aus der Liste links aus.

Führen Sie die Zellen nacheinander mit Shift + Enter aus.

🎯 5. Lernziele für Product Owner
In diesem Lab lernen wir nicht nur programmieren, sondern verstehen die Wertschöpfungskette der KI:

Data Layer: Wie wir aus "toten" CSV-Daten ein lebendiges Kundenprofil (Memory) erstellen.

Prompt Engineering: Wie wir Geschäftsregeln (z.B. "sei ehrlich", "fass dich kurz") in natürliche Sprache für die KI übersetzen.

Observability (Tracing): Wie wir mit Langfuse Latenz, Kosten und Qualität kontrollieren.

MVP-Deployment: Wie wir mit Gradio innerhalb von Minuten einen Prototyp bauen, den der Fachbereich testen kann.

❓ Troubleshooting (Hilfe bei Problemen)
ModuleNotFoundError: Sie haben pip install wahrscheinlich in einem anderen Terminal ausgeführt als JupyterLab. Installieren Sie die Pakete erneut direkt im Notebook mit !pip install ....

.env wird nicht erkannt: Stellen Sie sicher, dass die Datei wirklich nur .env heißt (kein .txt am Ende!) und im selben Ordner wie das Notebook liegt.

Gradio UI lädt ewig: Überprüfen Sie Ihr Terminal. Meistens wartet die KI auf eine Antwort (Cloud-Latenz) oder es gibt einen Authentifizierungsfehler.