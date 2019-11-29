# SUV



![SUV](SUV_lux_CH.svg)

## Analyse der SUVs in der Schweiz

asdf.

**Datenquelle(n)**: Bundesamt für Strassen (ASTRA) ([astra.admin.ch](https://www.astra.admin.ch/astra/de/home.html))

**Artikel**: [Wird publiziert am 1. Dezember 2019](https://www.tagesanzeiger.ch/)

**Code**: [Juypter Notebook](https://github.com/tamedia-ddj/SUVs/blob/master/SUV Analyse Schweiz.ipynb)



## Beschreibung

Erstmals soll die Verteilung der SUVs und Geländewagen in der Schweiz auf Gemeindeebene dargestellt und untersucht werden. In der Schweiz gibt es keine offizielle Definition was als "SUV" oder als "Geländewagen" gilt. Deshalb greifen wir auf eine Liste der deutschen Behörden zurück, welche eine solche Kategorisierung vornimmt. Im weiteren Text wird der Begriff "SUV" verwendet und soll sich auf beide Typen beziehen. 

## Datengrundlage

### Fahrzeuge

Das Astra unterhält eine Datenbank mit allen registrierten Fahrzeugen in der Schweiz. Ein Auszug aus dieser Datenbank dient als Grundlage für diese Analyse. Der Auszug erfolgte im Februar 2019.

Der Datensatz enthält eine Zeile für jedes registrierte Fahrzeug. Insgesamt enthält der Datensatz 64 Variablen für jedes Fahrzeug. Die in der Analyse verwendeten Variablen sind hier erklärt:

| Variable          | Beschreibung                                                 |
| ----------------- | ------------------------------------------------------------ |
| `Fahrzeugart`     | Art des Fahrzeuges. In dieser Analyse werden nur "Personenwagen" berücksichtigt |
| `Marke`           | Marke des registrierten Fahrzeuges                           |
| `Marke_und_Typ`   | Marke und Typ des registrierten Fahrzeuges                   |
| `BFS-Gemeinde-Nr` | BFS-Gemeindenummer der Gemeinde in welcher das Fahrzeug registriert wurde |
| `Staat_Code`      | Code des Landes in welcher das Fahrzeug registriert wurde    |

Der verwendete Datensatz ist nicht öffentlich zugänglich und kann deshalb nicht in diesem Github Repo zur Verfügung gestellt werden. Stattdessen wir ein kleiner Auszug aus dem Datensatz zur Verfügung gestellte (10'000 Zeilen). Diese Datensatz ist zusätzlich auf die folgende Art unkenntlich gemacht:

- Spalte `Erstinvekehrsetzung_Kanton` wurde mit einem Platzhalter versehen
- Spalte `Spalte Inverkehrsetzung_Kanton` wurde mit einem Platzhalter versehen
- Spalte `PLZ` wurde mit einem Platzhalter versehen
- Spalte `Ort` wurde mit einem Platzhalter versehen

- Spalte `BFS-Gemeinde-Nr` ist mit einer zufällige (valide) BFS Nummer versehen.



### SUV Typen

In der Schweiz werden SUVs und Geländewagen nicht gesondert erfasst. Es gibt also keinen Eintrag in der Datenbank welcher den Rückschluss erlauben würde, ob es sich bei einem Fahrzeug um ein SUV oder Geländewagen handelt. Um Personenwagen als SUVs oder Geländewagen zu identifizieren haben wir auf eine Liste der deutschen Behörden zurückgegriffen, welche eine solche Einteilung vornimmt. Auf diese Liste sind die 117 häufigsten SUVs und Geländewagen aufgeführt. Zusätzlich habe wir die Liste mit Luxus-Geländewagen von Maserati, Lamborghini, Cadillac und Rolls Royce ergänzt.

Für diese Fahrzeuge haben wir eine zusätzlich Kategorisierung in Luxuriöse SUVs durchgeführt

## Analyse

Das Astra unterhält eine Datenbank mit allen registrierten Fahrzeugen in der Schweiz. Ein Auszug aus dieser Datenbank dient als Grundlage für diese Analyse. Diese Daten sind nicht öffentlich zugänglich und können deshalb nicht in diesem Github Repo zur Verfügung gestellt werden. Sat

| Variable                       | Beschreibunng                                                |
| ------------------------------ | ------------------------------------------------------------ |
| `...`                          | ...                                                          |
| `kanton_nummer `               | Eindeutige Kennziffer für die Kantone                        |
| `liste_bezeichnung `           | Bezeichnung der jeweiligen Liste (Listentitel)               |
| `...`                          | ...                                                          |
| `liste_unterlistenverbindung ` | Eine pro Kanton eindeutige Kennzeichung einer Unterlistenverbindung. Bestehend aus Buchstabe der Listenverbindung und aufsteigender Nummer für Unterlistenverbindung. (z.B.: `C2`) |
| `liste_verbindung `            | Eine pro Kanton eindeutige Kennzeichung einer Listenverbindung. Bestenhend aus aufsteigenden Buchstaben. (z.B.: `C`) |
| `...`                          | ...                                                          |
| `partei_id `                   | Eindeutige Kennziffer für die (Mutter-)Partei der jeweiligen Liste |
| `stimmen_liste `               | Absolute Anzahl Stimmen, die die Liste im Kanton erhalten hat. |



## Output-Files

### file1.csv

| Variable                      | Beschreibunng                                                |
| ----------------------------- | ------------------------------------------------------------ |
| `partei_bezeichnung_kurz_de ` | Parteibezeichnung Kurzform                                   |
| `sitze_diff `                 | Differenz zur realen Sitzverteilung im Nationalrat - negative Werte bedeuten, dass in einer Wahl ohne Listenverbindung die jeweilige Partei mehr Sitze erhalten hätte |



## Lizenz

*Listenverbindungen Public* is free and open source software released under the permissive MIT License.

```

```
