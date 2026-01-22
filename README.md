# 🛍️ Bon Prix: Personalization Lab  
### Wirtschaftsinformatik Case Study: Hyper-Personalization via NLP

Willkommen im **Personalization Lab**. In dieser Session bauen wir einen KI-gestützten Shopping-Assistenten für **bon prix**, der Kundenrezensionen basierend auf individuellen Präferenzen zusammenfasst.

---

## 🛠️ 1. System-Voraussetzungen & Vorbereitung

### Schritt A: Python & JupyterLab

1. Installieren Sie **Python 3.10+** von https://www.python.org  
2. Installieren Sie die benötigten Pakete:

```bash
pip install pandas gradio plotly python-dotenv jupyterlab ibm-watsonx-ai ollama langfuse
```

### Schritt B: Repository vorbereiten

- Repository klonen oder herunterladen
- Dateien im Root-Verzeichnis:
  - personalization_users_visible.csv
  - reviews_all_users_in_shop.csv

---

## 🔑 2. Konfiguration (.env)

| Variable | Beschreibung |
|--------|--------------|
| WATSONX_API_KEY | IBM Cloud API-Key |
| WATSONX_URL | https://eu-de.ml.cloud.ibm.com |
| WATSONX_PROJECT_ID | watsonx Projekt-ID |
| LANGFUSE_PUBLIC_KEY | Langfuse Public Key |
| LANGFUSE_SECRET_KEY | Langfuse Secret Key |
| LANGFUSE_BASE_URL | https://cloud.langfuse.com |

---

## 🚀 3. Start

```bash
jupyter lab
```

---

## ❓ Troubleshooting

- pip nicht gefunden → Python zum PATH hinzufügen
- UI hängt → capture_output=False im @observe-Decorator
