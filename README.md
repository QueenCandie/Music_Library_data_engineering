# Personal Music Library – Data Engineering Project

A beginner-friendly **end-to-end data engineering project** that turns a messy collection of MP3 files into a clean, structured, and queryable database.

**Pipeline:** Extract → Clean → Improve → Analyze → Store → Query

---

## Project Overview

| Item                    | Details                          |
|-------------------------|----------------------------------|
| Level                   | Beginner                         |
| Platform                | Android (Pydroid 3) + Python     |
| Final Dataset           | 713 clean MP3 songs              |
| Total Library Size      | 4.66 GB                          |
| Total Listening Time    | 43 hours                         |
| Database                | SQLite                           |

---

## What This Project Does

1. **Extracts** metadata (title, artist, album, genre, duration, bitrate, etc.) from MP3 files
2. **Cleans** missing and messy data
3. **Improves** data quality by recovering Artist & Title from filenames
4. **Removes** broken/short songs
5. **Analyzes** the music library (top artists, duration distribution, storage usage, etc.)
6. **Stores** the clean data in a SQLite database
7. **Queries** the database using SQL

---

## Project Structure

```
music-library-data-engineering/
│
├── README.md
├── requirements.txt
│
├── scripts/
│   ├── 01_extract_metadata.py
│   ├── 02_clean_data.py
│   ├── 03_improve_data.py
│   ├── 04_analyze_data.py
│   ├── 05_create_database.py
│   └── 06_query_database.py
│
└── data/                  # (Your generated files will go here)
    ├── my_music_catalog.csv
    ├── my_music_catalog_clean.csv
    ├── my_music_catalog_final_v2.csv
    └── my_music_library.db
```

---

## Tools & Libraries Used

- **Python 3**
- **tinytag** – Extract metadata from MP3 files
- **pandas** – Data cleaning and analysis
- **sqlite3** – Create and query the database (built-in)

---

## How to Run the Project

### 1. Install required libraries

```bash
pip install tinytag pandas
```

### 2. Update the folder path

In the scripts, change this line to the location of your MP3 files:

```python
music_folder = "/storage/emulated/0/Download/"
```

### 3. Run the scripts in order

```bash
python scripts/01_extract_metadata.py
python scripts/02_clean_data.py
python scripts/03_improve_data.py
python scripts/04_analyze_data.py
python scripts/05_create_database.py
python scripts/06_query_database.py
```

---

## Key Results

- **713** clean songs after processing
- **4.66 GB** total library size
- **43 hours** of total listening time
- Average song length: **3.6 minutes**
- Most songs are between **3–4 minutes**

### Top Artists
- Tyla
- Ariana Grande
- Michael Jackson
- Doja Cat
- Chris Brown
- Davido
- Burna Boy
- Ayra Starr
- Rema
- SZA

---

## Skills Demonstrated

- Data extraction from unstructured files
- Data cleaning & handling missing values
- Feature engineering from filenames
- Exploratory data analysis
- Creating and querying a SQLite database
- Building a complete data pipeline

---

## Future Improvements

- Better artist name standardization
- Genre enrichment using external APIs (MusicBrainz / Spotify)
- Audio feature extraction (tempo, key, etc.)
- Simple recommendation system
- Dashboard with Streamlit or Metabase

---

## Author

Beginner Data Engineering Project  
Built as a practical learning exercise on mobile (Pydroid 3)
