# DE-corona-VAT-reduction-2020

## Question

Welche Änderungen ergeben sich aufgrund der befristeten Absenkung der Umsatzsteuersätze ab dem 01.07.2020?

## Question

Wird das fiskaltrust.iPOS aufgrund der Umsatzsteuersatzsenkung geändert?

## Metadata tags

lang-de, market-de, middleware, PosCreator, PosDealer, Consultant

## Answer

### Steuerliche Beurteilung

#### 1. Befristeten Absenkung der Umsatzsteuersätze von 19% auf 16% und von 7% auf 5%

Durch das zweite Corona-Steuerhilfegesetz werden vom 01.07.2020 bis 31.12.2020 der allgemeine Umsatzsteuersatz von 19% auf 16% \(§ 12 Abs. 1 UStG\) sowie der ermäßigte Umsatzsteuersatz von 7% auf 5% \(§ 12 Abs. 2 UStG\) gesenkt.

#### 2. Befristete Absenkung des Umsatzsteuersatzes für Speisen in Restaurants und Gaststätten von 19% auf 7%

Die Regelung gilt ab dem 01.07.2020 und ist bis zum 30.06.2021 befristet. Da die obige Regelung der Reduktion von 7% auf 5% \(siehe 1.\) auch für diesen Fall gilt, beträgt der Umsatzsteuersatz auf Speisen in Restaurants und Gaststätten

* vom 1.7.2020 bis 31.12.2020: 5%
* vom 1.1.2020 bis 30.06.2020: 7%

Dies führt dazu, dass in allen Kassen zweimal, in Restaurants und Gaststätten dreimal Anpassungen vorgenommen werden müssen.

### Keine Änderung des fiskaltrust.iPOS

Das fiskaltrust.iPOS ist seit Beginn an derart flexibel aufgebaut und auf eine Änderung eines Steuersatzes vorbereitet, dass keine grundsätzliche Änderung erforderlich ist.

### Abbildung im json-request an die ft.Middleware

#### Änderung am 01.07.2020, am 01.01.2021 sowie am 01.07.2021

Die geänderte steuerliche Vorgabe ist durch korrekte json-requests an die ft.Middleware zu senden. Es ändert sich nur der Steuersatz, nicht jedoch die Leistungsart. Dies bedeutet, dass die bisherigen ftChargeItemCases für den allgemeinen Umsatzsteuersatz \(z.B. für Lieferungen 0x4445000000000011\) sowie für den ermäßigten Umsatzsteuersatz \(z.B. für Lieferungen 0x4445000000000012\) ab 01.07.2020 weiter verwendet werden müssen. [https://docs.fiskaltrust.cloud/doc/interface-doc/doc/appendix-de-kassensichv/reference-tables/type-of-service-ftchargeitemcase.html](https://docs.fiskaltrust.cloud/doc/interface-doc/doc/appendix-de-kassensichv/reference-tables/type-of-service-ftchargeitemcase.html)

Die Kassa hat jedoch immer den korrekten Mehrwertsteuersatz im Feld VATRate zu senden.

[https://docs.fiskaltrust.cloud/doc/interface-doc/doc/general/data-structures/data-structures.html](https://docs.fiskaltrust.cloud/doc/interface-doc/doc/general/data-structures/data-structures.html)

Daher ist

* der"alte" Steuersatz von 19% bis zum 30.06.2020 und 
* der temporär, "neue" Steuersatz von 16% ab 01.07.2020 

  im request zu senden.

Die Umstellung vom "alten" auf den "neuen" Steuersatz ist durch einen Tagesabschlusses \(daily-closing request\) zu trennen bzw. dadurch zu markieren.

### Zeitliche Zuordnung

Der Zeitpunkt der Ausführung einer Lieferungen bzw. einer sonstige Leistung ist für die Anwendung des korrekten Steuersatzes relevant. Hiefür ist die steuerliche Beurteilung des Unternehmens z.B. durch eine/n SteuerberaterIn maßgeblich.

### Behandlung von Sonderfällen

Beispielsweise sind Anzahlungen, Vorauszahlungen, Jahreskarten, Abonnements, Dauerleistungen, Bauleistungen, Pfand, Einzweck- und Mehrzweckgutscheine in Hinblick auf diese zeitliche Zuordnung besonders zu behandeln. In diesen Sonderfällen, welche zur Verwendung eines anderen \(alten\) Umsatzsteuersatzes führen, sind die jeweils korrekten Umsatzsteuersätze \(19%, 16%, 7% oder 5%\) im VATRate eines json-request zu verwenden. Die ft.Middleware trennt die Umsatzsteuersätze aufgrund der gesendeten Information für den korrekten Export im DSFinV-K.

### TSE-ProcessData-Container sowie DSFinV-K Steuerpositionen

Die ft.Middleware verwendet die TSE entsprechend der BSI-Richtlinien sowie des DSFinV-K.

#### TSE-ProcessData-Container

Dies bedeutet, die fünf bestehenden TSE-ProcessData-Container bleiben erhalten und werden nicht erweitert. 1. Regelsteuersatz, 2. ermäßigter Steuersatz, usw.

#### DSFinV-K Steuerpositionen

* 1 ist allgemeiner Umsatzsteuersatz
* 2 ermäßigter Umsatzsteuersatz, usw
* Die historische Steuersätze \(19% und 7%\) werden voraussichtlich in den IDs &gt; 10 und &lt; 1000 definiert.

Bundesregierung: [Steuerentlastungen-Coronavirus](https://www.bundesregierung.de/breg-de/themen/coronavirus/steuerentlastungen-coronavirus-1750826)

BMWI, 12.06.2020 -PRESSEMITTEILUNG: [Wirtschaftliche Entwicklung - Unbürokratische Umsetzung der Mehrwertsteuersenkung bei Preisangaben durch pauschale Rabatte möglich](https://www.bmwi.de/Redaktion/DE/Pressemitteilungen/2020/20200612-unbuerokratische-umsetzung-der-mehrwertsteuersenkung-bei-preisangaben-durch-pauschale-rabatte-moeglich.html)

