# Aktienanalyse Microsoft (MSFT) vs. S&P 500 Total Return

Rendite- und Risikoanalyse der Microsoft-Aktie für den Zeitraum 2021–2025 mit Python – inklusive Benchmark-Vergleich mit dem S&P 500 Total Return Index.

Projekt im Rahmen der Weiterbildung **„Python und Data Science im Finanzwesen“** an der IU Internationale Hochschule (Kurs: Projekt Programmierung mit Python, 09/2026).

## Leitfrage

Welche Rendite erzielte Microsoft, welches Risiko war damit verbunden und wie ist das Ergebnis gegenüber dem Markt einzuordnen?

## Ergebnisse

| Kennzahl | Microsoft | S&P 500 TR |
|---|---:|---:|
| Annualisierte durchschnittliche Rendite | 20,17 % | 15,28 % |
| Annualisierte Volatilität | 25,71 % | 16,96 % |
| Maximum Drawdown | −37,15 % | −24,49 % |
| Sharpe Ratio (rf = 0 %) | 0,78 | 0,90 |

- Datenbasis: **1.255 gemeinsame Handelstage** (04.01.2021–31.12.2025), keine fehlenden Werte
- Wertzuwachs des bereinigten Kurses: **+131,53 %**
- Korrelation der Tagesrenditen mit dem Markt: **0,76** · Beta: **1,15**

**Fazit:** Microsoft erzielte die höhere Rendite, der S&P 500 TR das bessere Verhältnis von Rendite zu Schwankungsrisiko.

## Vorgehen

1. **Daten beschaffen** – Yahoo Finance über `yfinance` (dividenden- und splitbereinigte Kurse, `^SP500TR` als Benchmark)
2. **Qualität prüfen** – Zeitraum, Datentypen, fehlende Werte, Abgleich der Handelstage
3. **Kennzahlen berechnen** – Tagesrenditen, kumulative Rendite, Volatilität (gesamt und rollierend 30 Tage), Maximum Drawdown, Sharpe Ratio, Korrelation, Beta
4. **Visualisieren und einordnen** – Kursverlauf, Drawdown, Volatilität, normierte Wertentwicklung, Risiko-Rendite-Diagramm

## Grenzen

Historische Kennzahlen sind keine Prognose. Die Analyse nutzt eine Datenquelle, einen risikofreien Zinssatz von 0 % und berücksichtigt keine Steuern, Kosten oder Wechselkurseffekte.

## Dateien

| Datei | Inhalt |
|---|---|
| `Microsoft_Aktienanalyse.ipynb` | Jupyter Notebook mit Code, Ausgaben und Grafiken |
| `Praesentation_Microsoft_Aktienanalyse.pdf` | Projektpräsentation (13 Folien) |
| `requirements.txt` | Benötigte Python-Pakete |

## Ausführen

```bash
pip install -r requirements.txt
jupyter notebook Microsoft_Aktienanalyse.ipynb
```

## Werkzeuge

Python · pandas · NumPy · Matplotlib · yfinance · Jupyter

---

**Ashraf Al Keilani** · Hannover · [LinkedIn](https://www.linkedin.com/in/ashraf-al-keilani)
