🛍️ Bon Prix: Personalization Lab
Wirtschaftsinformatik Case Study: Hyper-Personalization via NLP
Willkommen im Personalization Lab. In dieser Session bauen wir einen KI-gestützten Shopping-Assistenten für bon prix, der Kundenrezensionen basierend auf individuellen Präferenzen zusammenfasst.
🛠️ 1. System-Voraussetzungen & Vorbereitung
Bevor wir in den Code eintauchen, müssen wir sicherstellen, dass Ihre Arbeitsumgebung bereit ist.
Schritt A: Python & JupyterLab
Wir nutzen JupyterLab als interaktive Entwicklungsumgebung.
Installieren Sie Python 3.10+ von python.org.
Öffnen Sie Ihr Terminal (Mac/Linux) oder die PowerShell (Windows) und installieren Sie die benötigten Pakete:
# Installation der Kern-Bibliotheken & Jupyter
pip install pandas gradio plotly python-dotenv jupyterlab ibm-watsonx-ai ollama langfuse
Schritt B: Das Repository vorbereiten
Laden Sie dieses Repository herunter oder klonen Sie es via Git.
Stellen Sie sicher, dass die Dateien
personalization_users_visible.csv und
reviews_all_users_in_shop.csv
im Hauptverzeichnis liegen.
🔑 2. Konfiguration (Die .env Datei)
Aus Sicherheitsgründen speichern wir API-Keys niemals direkt im Code. Wir nutzen dafür eine Umgebungsvariable-Datei.
Suchen Sie die Datei .env.template.
Benennen Sie diese Datei um in .env.
Tragen Sie Ihre Zugangsdaten ein:
Variable	Beschreibung
WATSONX_API_KEY	IBM Cloud API-Key
WATSONX_URL	z. B. https://eu-de.ml.cloud.ibm.com
WATSONX_PROJECT_ID	watsonx Projekt-ID
LANGFUSE_PUBLIC_KEY	Langfuse Public Key
LANGFUSE_SECRET_KEY	Langfuse Secret Key
LANGFUSE_BASE_URL	https://cloud.langfuse.com
📓 3. Auswahl des richtigen Notebooks
Datei	Engine	Fokus
bonprix_lab-wx.ipynb	watsonx.ai	Enterprise Cloud
bonprix_lab-wx_tracing.ipynb	watsonx + Langfuse	Tracing
bonprix_lab-ollama.ipynb	Ollama	Lokal
bonprix_lab-ollama_tracing.ipynb	Ollama + Langfuse	Lokal + Observability
🚀 4. Starten des Labs
jupyter lab
❓ Troubleshooting
pip nicht gefunden → Python zum PATH hinzufügen
UI hängt → capture_output=False im @observe-Decorator setzen