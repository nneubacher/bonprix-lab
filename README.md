# 🛍️ Bon Prix: Personalization Lab  
### KLU Projekt: Shopping Personalisierung via NLP

Willkommen im **Personalization Lab**. In dieser Session bauen wir einen KI-gestützten Shopping-Assistenten für **bonprix**, der Kundenrezensionen basierend auf individuellen Präferenzen zusammenfasst.

---

## 🛠️ 1. System-Voraussetzungen & Vorbereitung

### Schritt A: Python Installation

1. Installieren Sie **Python 3.11** von https://www.python.org/downloads/
2. Stellen Sie sicher, dass Python zum **PATH** hinzugefügt wurde.

---

### Schritt B: Virtuelle Umgebung (venv) einrichten **(WICHTIG)**

Um zu vermeiden, dass Python-Pakete **global** installiert werden, nutzen wir eine **virtuelle Umgebung (venv)**.

#### 📁 1. Virtuelle Umgebung (venv) erstellen
Führen Sie im Projektverzeichnis folgenden Befehl aus:

```bash
python -m venv .venv
```

Dadurch wird ein Ordner `.venv` erstellt, der eine isolierte Python-Umgebung enthält.

#### ▶️ 2. Virtuelle Umgebung aktivieren

**macOS / Linux**
```bash
source .venv/bin/activate
```

**Windows (PowerShell)**
```powershell
.venv\Scripts\Activate.ps1
```

Nach erfolgreicher Aktivierung sehen Sie `(.venv)` am Anfang Ihrer Kommandozeile.

---

### Schritt C: Abhängigkeiten installieren (innerhalb der venv)

⚠️ **Stellen Sie sicher, dass die venv aktiviert ist**, bevor Sie diesen Schritt ausführen.

```bash
pip install pandas gradio plotly python-dotenv jupyterlab ibm-watsonx-ai ollama langfuse iprogress
```

---

### Schritt D: Repository vorbereiten

- Repository klonen oder herunterladen
- Stellen Sie sicher, dass sich folgende Dateien im Root-Verzeichnis befinden:
  - `personalization_users_visible.csv`
  - `reviews_all_users_in_shop.csv`

---

## 🔑 2. Konfiguration (.env)

1. Benennen Sie `.env.template` um in `.env`
2. Tragen Sie Ihre Zugangsdaten ein:

| Variable | Beschreibung |
|--------|--------------|
| `WATSONX_API_KEY` | IBM Cloud API-Key |
| `WATSONX_URL` | https://eu-de.ml.cloud.ibm.com |
| `WATSONX_PROJECT_ID` | watsonx Projekt-ID |
| `LANGFUSE_PUBLIC_KEY` | Langfuse Public Key |
| `LANGFUSE_SECRET_KEY` | Langfuse Secret Key |
| `LANGFUSE_BASE_URL` | https://cloud.langfuse.com |

---

## 📓 3. Notebook-Varianten: Model Provider & Tracing

Für dieses Lab stehen mehrere Notebook-Varianten zur Verfügung. Sie unterscheiden sich im **Model Provider** (Cloud vs. lokal) und darin, ob **Tracing (Beobachtbarkeit)** aktiviert ist.

---

### 🔹 Model Provider
* **IBM watsonx.ai**: Cloud-basierte Enterprise-LLMs (API-Key erforderlich).
* **Ollama**: Lokale Ausführung von LLMs (kein Cloud-Key notwendig).

### 🔹 Tracing (optional)
* **Ohne Tracing**: Fokus auf Funktionalität & Ergebnis.
* **Mit Tracing (Langfuse)**: Zusätzlich: Nachvollziehbarkeit von Prompt, Antwort, Laufzeit & Kosten.

---

### 📂 Übersicht der verfügbaren Notebooks

| Notebook | Model Provider | Tracing | Einsatz |
| :--- | :--- | :---: | :--- |
| `bonprix_lab-wx.ipynb` | watsonx.ai | ❌ | Standard-Variante (Cloud) |
| `bonprix_lab-wx_tracing.ipynb` | watsonx.ai | ✅ | Cloud + Observability |
| `bonprix_lab-ollama.ipynb` | Ollama | ❌ | Lokal, kein API-Key |
| `bonprix_lab-ollama_tracing.ipynb` | Ollama | ✅ | Lokal + Observability |

---

## 🚀 4. JupyterLab starten

⚠️ **JupyterLab muss aus aktivierter venv gestartet werden.**

```bash
jupyter lab
```

---

## ❓ Troubleshooting

- **pip installiert global** → venv war nicht aktiviert  
- **venv lässt sich nicht aktivieren (Windows)** →  
  `Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy RemoteSigned`
- **UI hängt / keine Plots sichtbar** →  
  `capture_output=False` im `@observe`-Decorator setzen

---

## 🧠 Best Practice

- `.venv/` in `.gitignore` aufnehmen  
- venv bei jedem neuen Terminal neu aktivieren  
- Niemals `pip install` ohne aktive venv ausführen
