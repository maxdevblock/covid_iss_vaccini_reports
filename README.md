# covid_iss_vaccini_reports
Dati dei reports ISS su campagna vaccinale COVID-19
https://www.epicentro.iss.it/coronavirus/aggiornamenti

Il database inizia dal Report del 14 Luglio 2021 e viene aggiornato ad ogni nuovo Report ISS compatibile.

Struttura del database (formato Comma Separated Values, `.csv`)

| Colonna      | DataType | Descrizione     |
| :---        |    :----:   |          ---: |
| data      | Formatted String       | Data di riferimento del Report `YYYY-MM-DD`   |
| pubblicazione   | Formatted String        | Data di pubblicazione del Report `YYYY-MM-DD`    |
| url | String | Link al Report in formato pdf |
| fascia | String | Fascia d'età: 12-39, 40-59, 60-79, 80+ |
| vaccino | String | Stato vaccinale: non vaccinati, vaccinati incompleti, vaccinati completi |
| popolazione | Integer | Popolazione di riferimento per data, stato vaccinale e fascia d'età (vedi popolazione_giorno) |
| diagnosi | Integer | Numero di diagnosi di COVID-19 per intervallo temporale, stato vaccinale e fascia d'età (vedi diagnosi_start e diagnosi_end) |
| ricoveri | Integer | Numero di ricoveri di COVID-19 per intervallo temporale, stato vaccinale e fascia d'età (vedi ricoveri_start e ricoveri_end) |
| intensive | Integer | Numero di intensive di COVID-19 per intervallo temporale, stato vaccinale e fascia d'età (vedi intensive_start e intensive_end) |
| decessi | Integer | Numero di decessi di COVID-19 per intervallo temporale, stato vaccinale e fascia d'età (vedi decessi_start e decessi_end) |
| popolazione_giorno | Formatted String | Giorno di riferimento per il valore di popolazione |
| diagnosi_start | Formatted String | Estremo inferiore del periodo di riferimento per il valore diagnosi `YYYY-MM-DD` |
| diagnosi_end | Formatted String | Estremo superiore del periodo di riferimento per il valore diagnosi `YYYY-MM-DD` |
| ricoveri_start | Formatted String | Estremo inferiore del periodo di riferimento per il valore ricoveri `YYYY-MM-DD` |
| ricoveri_end | Formatted String | Estremo superiore del periodo di riferimento per il valore ricoveri `YYYY-MM-DD` |
| intensive_start | Formatted String | Estremo inferiore del periodo di riferimento per il valore intensive `YYYY-MM-DD` |
| intensive_end | Formatted String | Estremo superiore del periodo di riferimento per il valore intensive `YYYY-MM-DD` |
| decessi_start | Formatted String | Estremo inferiore del periodo di riferimento per il valore decessi `YYYY-MM-DD` |
| decessi_end | Formatted String | Estremo superiore del periodo di riferimento per il valore decessi `YYYY-MM-DD` |
| totale | Integer | Totale della popolazione nella fascia d'età e nel giorno di riferimento: non vaccinati + vaccinati incompleto + vaccinati completo |
| percentuale_popolazione | Float | Percentuale di popolazione vaccinata per fascia d'età, ovvero rapporto popolazione / totale |
| percentuale_diagnosi | Float | Rapporto tra diagnosi e popolazione per fascia d'età e stato vaccinale |
| percentuale_ricoveri | Float | Rapporto tra ricoveri e popolazione per fascia d'età e stato vaccinale |
| percentuale_intensive | Float | Rapporto tra intensive e popolazione per fascia d'età e stato vaccinale |
| percentuale_decessi | Float | Rapporto tra decessi e popolazione per fascia d'età e stato vaccinale |
