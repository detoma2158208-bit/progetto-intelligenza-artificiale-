PROGETTO INTELLIGENZA ARTIFICIALE 
# Predire il genere dagli schemi di editing: un’analisi sul dataset *Gender Gap in Spanish Wikipedia*

## Descrizione del progetto

Il presente progetto mira allo sviluppo di un **modello di classificazione binaria** finalizzato alla predizione del **genere degli editor di Wikipedia in lingua spagnola** (*Male / Female*), utilizzando esclusivamente **pattern quantitativi di contribuzione**.

Il problema si colloca nell’ambito della **classificazione supervisionata** e affronta il tema del *Gender Gap* nelle piattaforme collaborative online, con particolare attenzione all’individuazione di possibili differenze sistematiche nei comportamenti di editing.

## Metodologia

L’approccio metodologico adottato si articola nelle seguenti fasi principali:

- **Analisi esplorativa dei dati (EDA)**, volta a esaminare le distribuzioni delle variabili e lo sbilanciamento delle classi;
- **Selezione delle feature**, basata sull’algoritmo Random Forest e su tecniche di riduzione della multicollinearità;
- **Addestramento e valutazione** di modelli di apprendimento supervisionato, mediante l’utilizzo dell’**F1-score**, metrica particolarmente indicata in presenza di dataset sbilanciati.

## Domanda di ricerca

> È possibile predire il genere di un utente Wikipedia utilizzando esclusivamente variabili di attività di editing?

Il modello si basa unicamente su **metriche quantitative di attività**, quali il numero di modifiche, il volume di pagine editate e la frequenza temporale degli interventi.  
## Dataset e strumenti utilizzati

Il dataset utilizzato nel presente lavoro è stato selezionato dalla lista di dataset fornita dalla docente e reso disponibile tramite apposito link:  
[*Gender Gap in Spanish Wikipedia*](link).

L’analisi e lo sviluppo dei modelli sono stati condotti utilizzando un **notebook Google Colab**, come richiesto, al fine di garantire la riproducibilità degli esperimenti e un ambiente di sviluppo condivisibile.

## Librerie utilizzate

Il codice è stato implementato in linguaggio **Python**, facendo uso delle seguenti librerie:

- **pandas**: gestione e manipolazione dei dati;
- **numpy**: operazioni numeriche e algebra lineare;
- **matplotlib** e **seaborn**: visualizzazione dei dati e analisi esplorativa;
- **scikit-learn**:
  - `train_test_split` per la suddivisione del dataset;
  - `StandardScaler` per la normalizzazione delle feature;
  - `DummyClassifier` come baseline;
  - `LogisticRegression`, `RandomForestClassifier`, `SVC`, `GaussianNB` per l’addestramento dei modelli;
  - metriche di valutazione quali `accuracy_score`, `precision_score`, `recall_score`, `f1_score`, `classification_report` e `confusion_matrix`.

L’impiego di tali librerie ha consentito di implementare in modo efficiente le fasi di preprocessing, modellazione e valutazione delle prestazioni.
