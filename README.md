# Degree Project – Environment & Setup
---

## Repository Structure

```
degree_project/
│
├── notebooks/
├── src/
├── requirements.txt          # core environment
├── requirements_ml.txt      # ML dependencies
├── .gitignore
└── data/ (ignored)
```

---

## Local Setup

### 1) Create environment

```bash
python -m venv .venv
```

Activate:

**Windows (PowerShell)**
```powershell
.\.venv\Scripts\Activate
```

**Linux / macOS**
```bash
source .venv/bin/activate
```

---

### 2) Install dependencies

Core pipeline:
```bash
python -m pip install -r requirements.txt
```

Optional NLP model dependencies:
```bash
python -m pip install -r requirements_ml.txt
```

---

### 3) Register notebook kernel

```bash
python -m ipykernel install --user --name degree_project --display-name "Python (degree_project)"
```

Open notebook → Select Kernel → `Python (degree_project)`

---

## Google Colab Setup

No manual installation required — notebook auto-detects Colab.

Typical workflow:

1. Open notebook in Colab
2. Mount Drive when prompted
3. Run all cells
4. Download results or copy to Drive

Working directory in Colab:
```
/content/data
```
This is temporary and resets when runtime stops.

---

### Recommended pre-processing flow

1. Run cleaning of file dumps locally
2. Upload the files from "cleaned_data" in "processed" folder to Google Colab
3. Run the rest of the pre-processing pipeline in Google Colab
4. Download "aligned_parquet" or copy to Drive

Working directory in Colab:
```
/content/data
```
This is temporary and resets when runtime stops.

```

