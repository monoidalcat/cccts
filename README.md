# cccts
🌵 Felicità dei Cactus – IoT + Data Science Project

Questo progetto nasce dalla constatazione che perfino un organismo minimale – un cactus innaffiato due volte al mese – produce una trama fitta di segnali: variazioni di umidità, lumen che crollano al tramonto, oscillazioni termiche, persino i decibel di canzoni che filtrano nella serra. L’obiettivo rimane pragmatico: verificare se la coabitazione di tali grandezze è sufficiente a generare un indicatore sintetico di benessere, un Happiness Score quotidiano, utile a governare un micro‑ecosistema e, insieme, a dimostrare come una pipeline analitica completa (ingest → feature engineering → modello → dashboard) possa essere riflessa in qualsiasi dominio.

Qui i dati sono materia duttile: li si modella, li si lascia sporgere, si rifila l’eccesso. PySpark per l’ingest, Delta Lake per la persistenza, Random Forest per la predizione. Non per dogma, ma per ergonomia: convivono, scalano, non chiedono permesso. Streamlit fa da superficie minima: uno spazio dove la linea dell’indice supera 0.75 e scatta l’emoji, un LED semantico che segnala al coltivatore quando rallentare o dare più luce.

In sintesi, un laboratorio tascabile per chi vuole mettere le mani su IoT, machine learning e storytelling senza annegare nella retorica agritech.

~~~~~~~~~~~~~~~~~~~~~~~~
.
├── data/                 # ↳ Dati grezzi e derivati (NON versionare raw >100 MB)
│   ├── raw/
│   └── processed/
├── notebooks/            # ↳ Esplorazioni e prototipi Jupyter
├── src/                  # ↳ Codice sorgente modulare
│   ├── etl/
│   │   └── spark_ingest.py
│   ├── features/
│   │   └── build_features.py
│   ├── models/
│   │   └── train_model.py
│   └── app/
│       └── app.py        # ↳ Dashboard Streamlit
├── dags/
│   └── cactus_pipeline.py # ↳ DAG Airflow (opzionale)
├── requirements.txt      # ↳ Librerie Python
├── Dockerfile            # ↳ Ambiente containerizzato
└── README.md             # ↳ Questo file
