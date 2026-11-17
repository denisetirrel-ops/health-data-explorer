# Health Data Explorer

**Python-Abschlussprojekt (Masterschool, Data Analytics) · pandas · seaborn · SciPy · scikit-learn**

*English summary below.*

**Präsentation / Slides (EN):** [presentation/Health_Data_Explorer.pdf](presentation/Health_Data_Explorer.pdf)

## Frage

Was beeinflusst den Körperfettanteil von rund 50.000 Menschen wirklich, und was scheint nur so? Sieben vorgegebene und drei eigene Fragen zu Alter, Geschlecht, Aktivität, Rauchen, BMI und Körperfett.

## Vorgehen

1. **Daten-Audit zuerst:** 96 identische Zeilen und eine ungültige Aktivitätskategorie gefunden und bereinigt (50.001 Zeilen danach). Nachgewiesen, dass `BF%` nicht gemessen, sondern mit der Deurenberg-Formel aus BMI, Alter und Geschlecht berechnet ist.
2. **Geführte Fragen:** Verteilungen und Vergleiche nach Geschlecht, Aktivität, Rauchstatus und Altersgruppe.
3. **Eigene Fragen:** Kreuzauswertung nach Alter und Aktivität, Textanalyse der `message`-Spalte, Vorhersagekraft einzelner Merkmale (Chi-Quadrat-Tests, logistische Regression).

## Ergebnisse

- **Das Alter bestimmt die Werte.** Der Körperfettanteil steigt von 21,5 % (18–29 Jahre) auf 34,7 % (60+), der Anteil gesunder Werte fällt von 82 % auf 6 %.
- **Aktivität und Rauchen zeigen keinen eigenen Effekt.** Raucher wirken nur gesünder, weil 61 % von ihnen Männer sind. Sehr Aktive sind im Schnitt jünger. Innerhalb von Altersgruppen und Geschlechtern verschwinden die Unterschiede.
- **Verdecktes Risiko:** Rund jede zweite Person mit „Great work – your BMI is in the healthy range“ hat einen ungesunden Körperfettanteil.

## Learning

Vergleiche immer nach Störgrößen wie Alter und Geschlecht trennen, bevor man Ursachen behauptet. Das gilt im Handel genauso, etwa bei Filialvergleichen.

## Ausführen

Das Notebook ist für Google Colab geschrieben. Der Datensatz `health_data_processed.csv` stammt aus dem Kursmaterial und ist nicht im Repository enthalten. Alle Ausgaben sind im Notebook gespeichert und auf GitHub direkt lesbar.

---

## English summary

Final Python project of my data analytics programme. I audited about 50,000 health records (96 duplicates, one invalid category, and proof that body fat was *calculated* with the Deurenberg formula, not measured), answered seven guided and three own questions, and tested effects with chi-square tests and logistic regression.

**Key findings:** age drives the values (healthy body fat drops from 82% at 18–29 to 6% at 60+); activity and smoking have no effect of their own once age and gender are controlled (smokers only look healthier because 61% of them are men); about half of the people told their BMI is healthy have unhealthy body fat.

**Lesson:** separate comparisons by confounders before claiming causes, in retail as much as in health data.

Author: [Denise Tirrel](https://www.linkedin.com/in/denise-tirrel)
