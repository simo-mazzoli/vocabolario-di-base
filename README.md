# Nuovo Vocabolario di Base della lingua italiana — De Mauro (CSV)

Dataset strutturato ricavato dal **Nuovo vocabolario di base della lingua italiana** di Tullio De Mauro, pubblicato su *Internazionale* il 23 dicembre 2016.

## File

`De_Mauro_vocabolario_base.csv` — 7.237 voci, codifica UTF-8, separatore virgola.

## Colonne

| Colonna | Descrizione | Esempio |
|---|---|---|
| `parola` | La voce lessicale | `abbandono` |
| `categoria` | Livello di frequenza/disponibilità (vedi sotto) | `alto_uso` |
| `prefisso_numerico` | Numero disambiguante per gli omonimi (`1`, `2`, …); vuoto se assente | `1` |
| `info_grammaticale` | Categorie grammaticali nella notazione originale | `s.m.` |
| `pos` | Parte/i del discorso normalizzate (derivate da `info_grammaticale`) | `verbo; participio passato; aggettivo; sostantivo` |
| `gender` | Informazioni di genere/numero/invariabilità estratte (quando presenti) | `maschile e femminile; invariabile` |
| `info_verbali` | Marcatori verbali originali separati (es. transitività/participi) | `v.tr.` |

## Categorie

De Mauro distingue tre fasce lessicali, codificate nel PDF originale tramite stile tipografico e qui riportate nella colonna `categoria`:

| Valore | Stile nel PDF | Descrizione | N. voci |
|---|---|---|---|
| `fondamentale` | **grassetto** | Parole ad altissima frequenza, indispensabili per la comunicazione di base | 1.969 |
| `alto_uso` | tondo | Parole frequenti, note a tutti i parlanti | 3.097 |
| `alta_disponibilita` | *corsivo* | Parole meno frequenti nei testi scritti ma largamente note e usate nel parlato | 2.171 |

## Fonte

De Mauro, T. (2016). *Il Nuovo vocabolario di base della lingua italiana*. Internazionale.  
URL originale: [dizionario.internazionale.it/nuovovocabolariodibase](https://dizionario.internazionale.it/nuovovocabolariodibase)

## Note metodologiche

Le voci e le informazioni grammaticali sono state estratte automaticamente dal PDF tramite parsing testuale. La categoria di ciascuna voce è stata determinata leggendo direttamente i metadati tipografici del PDF (nome del font), senza dipendere da euristiche sul testo.

Gli omonimi (es. *piano¹*, *piano²*) sono trattati come righe separate, distinguibili tramite la colonna `prefisso_numerico`.
