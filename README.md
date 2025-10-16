# 📚 Norske Bibliotek - Streamlit App

En moderne webapplikasjon for å utforske, søke og administrere data om norske bibliotek fra BaseBibliotek API.


## ✨ Funksjoner

- 🔍 **Avansert søk og filtrering** - Søk etter bibliotek basert på fylke, type, system eller fritekst
- 📊 **Statistikk og visualisering** - Oversikt over bibliotektyper og systemer
- 🗺️ **Kartvisning** - Geografisk visning av bibliotek med koordinater
- ✏️ **Redigering** - Oppdater biblioteksinformasjon direkte i appen
- 💾 **Database** - Lokal SQLite-database for rask tilgang og persistens
- 📥 **Import/Export** - Last inn JSON, hent fra API, eller eksporter til Excel
- 📖 **Detaljert visning** - Se all tilgjengelig informasjon om hvert bibliotek

## 🚀 Kom i gang

### Forutsetninger

- Python 3.8 eller nyere
- pip eller uv (for pakkehåndtering)

### Installasjon

1. **Klon repositoryet:**
```bash
git clone https://github.com/dittbrukernavn/norske-bibliotek.git
cd norske-bibliotek
```

2. **Opprett virtuelt miljø:**
```bash
# Med venv:
python3 -m venv .venv
source .venv/bin/activate  # På Windows: .venv\Scripts\activate

# Eller med uv (raskere):
uv venv
source .venv/bin/activate
```

3. **Installer avhengigheter:**
```bash
# Med pip:
pip install -r requirements.txt

# Eller med uv:
uv pip install -r requirements.txt
```

4. **Kjør applikasjonen:**
```bash
streamlit run app.py
```

Appen åpnes automatisk i nettleseren på `http://localhost:8501`

## 📁 Prosjektstruktur

```
norske-bibliotek/
├── app.py                  # Hovedapplikasjon
├── requirements.txt        # Python-avhengigheter
├── README.md              # Denne filen
├── bibliotek.db           # SQLite-database (opprettes automatisk)
└── bib_data.json          # Eksempel på dataformat (valgfri)
```

## 💻 Bruk

### Last inn data

**Alternativ 1: Last fra database**
- Hvis du allerede har data i databasen, velg "Last fra database" i sidemenyen

**Alternativ 2: Last opp JSON**
- Velg "Last opp JSON" og last opp en `bib_data.json`-fil
- Data lagres automatisk i lokal database

**Alternativ 3: Hent fra API**
- Gå til "API"-fanen
- Last opp en CSV-fil med biblioteknumre
- Klikk "Start datahenting"

### Søk og filtrer

- Bruk filtrene i sidemenyen for å begrense resultater
- Søk i alle felt med søkefeltet
- Bruk "Søk bibliotek"-fanen for dedikert søk

### Rediger bibliotek

1. Finn biblioteket i listen eller via søk
2. Klikk på "✏️ Rediger"
3. Endre ønskede felt
4. Klikk "💾 Lagre endringer"

### Eksporter data

- Bruk "📥 Last ned Excel"-knappen i sidemenyen
- Eksporterer kun filtrerte resultater

## 🗂️ Dataformat

Appen forventer JSON-data fra BaseBibliotek API med følgende struktur:

```json
[
  {
    "rid": 13,
    "bibnr": "1010101",
    "isil": "NO-1010101",
    "inst": "Biblioteksnavn",
    "katsyst": "Alma",
    "bibltype": "HØY",
    "kommnr": {
      "kommnr": "3101",
      "navn": "Halden"
    },
    ...
  }
]
```

## 🛠️ Teknologi

- **[Streamlit](https://streamlit.io/)** - Web-applikasjonsrammeverk
- **[Pandas](https://pandas.pydata.org/)** - Datahåndtering
- **[Folium](https://python-visualization.github.io/folium/)** - Kartvisning
- **[SQLite](https://www.sqlite.org/)** - Database
- **[OpenPyXL](https://openpyxl.readthedocs.io/)** - Excel-eksport

## 📝 Lisens

Dette prosjektet er lisensiert under MIT-lisensen.

## 🤝 Bidrag

Bidrag er velkomne! Åpne gjerne en issue eller pull request.

## 📧 Kontakt

For spørsmål eller tilbakemeldinger, åpne en issue på GitHub.

## 🙏 Anerkjennelser

Data fra [BaseBibliotek](https://www.nb.no/basebibliotek/) - Nasjonalbiblioteket