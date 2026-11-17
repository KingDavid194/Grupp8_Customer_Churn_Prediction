# Customer Churn Prediction – Grupp 8

**Kurs:** Statistisk programmering och maskininlärning  
**Utbildning:** BI-analytiker, Nackademin  
**Gruppmedlemmar:** David, Adam, Andy och Daro

## Projektbeskrivning

Detta projekt undersöker hur statistisk analys och maskininlärning kan användas för att identifiera kunder som riskerar att avsluta sina abonnemang (Customer Churn).

Vi analyserar historisk kunddata, undersöker samband mellan kundernas egenskaper och kundbortfall samt jämför två maskininlärningsmodeller.

## Dataset

Vi använder IBM Telco Customer Churn Dataset.

Datasetet innehåller 7 043 kundposter och 21 kolumner, inklusive:

- Kundtid (tenure)
- Avtalstyp (Contract)
- Månadskostnader (MonthlyCharges)
- Totala kostnader (TotalCharges)
- Kundbortfall (Churn)

**Källa:** [IBM Telco Customer Churn Dataset](https://github.com/IBM/telco-customer-churn-on-icp4d/blob/master/data/Telco-Customer-Churn.csv)

## Metoder och verktyg

Projektet är genomfört i Python med Google Colab.

Vi använder följande bibliotek:

- pandas – datahantering och analys
- Matplotlib – datavisualisering
- SciPy – statistiska tester
- scikit-learn – maskininlärning

Arbetet omfattar:

1. Dataimport och datarensning
2. Exploratory Data Analysis (EDA)
3. Statistiska tester
4. Data Preprocessing
5. Logistic Regression
6. Random Forest
7. Modellutvärdering och jämförelse

## Resultat

Analysen visade att 26,54 % av kunderna hade lämnat företaget.

Vi identifierade samband mellan kundbortfall och bland annat kundtid, avtalstyp och månadskostnader.

### Model Comparison

| Metric | Logistic Regression | Random Forest |
|---|---:|---:|
| Accuracy | 80.55 % | 79.99 % |
| Precision | 65.72 % | 65.75 % |
| Recall | 55.88 % | 51.34 % |
| F1-score | 60.40 % | 57.66 % |

Logistic Regression gav högre Accuracy, Recall och F1-score än Random Forest.

Vi valde därför Logistic Regression som vår preliminära huvudmodell, eftersom vi prioriterar att identifiera kunder som riskerar att lämna företaget.

Modellen identifierade 209 av 374 kunder som faktiskt lämnat i testdatan.

## Så kör du projektet

1. Öppna Google Colab: https://colab.research.google.com/
2. Ladda ner filen `Grupp8_Customer_Churn_Prediction.ipynb` från detta repository.
3. Öppna filen i Google Colab via **File → Upload notebook**.
4. Kör samtliga kodceller genom **Runtime → Run all**.

Projektet använder offentligt tillgänglig data som hämtas via en GitHub-länk i Notebooken.

## Begränsningar

Modellerna är utvärderade på historisk kunddata och resultaten visar statistiska samband, inte bevisade orsakssamband.

Logistic Regression missade 165 av 374 kunder som faktiskt lämnat företaget i testdatan.

Ytterligare validering och modellförbättring behövs innan lösningen används i en verklig verksamhet.

## Slutsats

Projektet visar hur Python, statistisk analys och maskininlärning kan komplettera Business Intelligence genom att identifiera mönster och förutsäga kundbortfall.

Logistic Regression gav bäst resultat av de två undersökta modellerna utifrån projektets målsättning.
