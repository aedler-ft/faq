# DE-Rechnung-Beleg-Inhalte

## Question

Welche Inhalte müssen auf eine Rechnung gedruckt werden?

## Question

Welche Inhalte müssen auf einen Beleg \(Quittung, Bon\) gedruckt werden?

## Question

Ist es wirklich notwendig dass der Beleg so lang wird?

## Metadata tags

lang-de, market-de, middleware, PosCreator, PosDealer, Consultant

## Answer

Der optionale QR Code ist in der DSFinV-K empfohlen um eine etwaige Prüfung durch das Finanzamt zu erleichtern.

Alle anderen Inhalte \(SignatureItems\) MÜSSEN auf den Beleg gedruckt werden.

Informationen zu den verschiedenen gesetzlichen Anforderungen an die Inhalte von Rechnung, Beleg und Quittung hat [Axel Kutschera](https://github.com/AxelKutschera) zusammengestellt:

| Nr | Nr | Rechnung |  | Nr | Kleinbetragsrechnungen  &lt; EUR 250,- |  | Nr | Grundaufzeichnungen  \(Einzelaufzeichnung\) |  | Nr | Beleg |  | Nr | Beleg |  | Nr | Beleg |  | Nr | Quittung |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
|  |  | §  14 Abs. 4 iVm § 14a Abs. 5 UStG |  |  | §  33 Umsatzsteuerdurchführungsverordnung - UStDV und siehe BMF-Schreiben vom  18.10.2006 |  |  | AEAO  zu § 146 Kap. 2.1.2. und 2.1.3 |  |  | §  6 KassenSichV |  |  | AEAO  zu 146a AO |  |  | DSFinV-K  v2.0 Anhang I Kap. 2. \(freiwillig\) |  |  | AO  \(bzw. BGB\) |
| x^x |  | Pflicht  zur Ausstellung wie bisher |  |  | Pflicht  zur Ausstellung wie bisher |  |  | Pflicht  ab 1.1.2020 |  |  | Pflicht  ab Verwendung einer TSE |  |  | Pflicht  ab Verwendung einer TSE |  |  | Pflicht  ab Verwendung einer TSE |  |  | Pflicht  ab Verwendung einer TSE |
| 1 | RU1 | vollständiger  Name und vollständige Anschrift des leistenden Unternehmers | = | RK1 | vollständiger  Name und Anschrift des leistenden Unternehmers |  |  |  | = | BK1 | vollständiger  Namen und die vollständige Anschrift des leistenden Unternehmers | = | BA1 | Den  vollständigen Namen und die vollständige Anschrift des leistenden  Unternehmers \(vgl. § 6 Nr. 1 KassenSichV\). Aus Vereinfachungsgründen genügen  die Angaben aus § 31 Abs. 2 UStDV \(UStAE Abschnitt 14.5 Abs. 2\) | = |  |  |  |  |  |
| 2 | RU2 | Menge  und handelsübliche Bezeichnung der gelieferten Gegenstände oder die Art und  den Umfang der sonstigen Leistung; | = | RK2 | Menge  und Art der gelieferten Gegenstände oder Art und den Umfang der sonstigen  Leistung | &lt; | G2 | verkaufte,  eindeutig bezeichnete Artikel; sowie die verkaufte Menge bzw. Anzahl | = | BK2 | Menge  und die Art der gelieferten Gegenstände oder den Umfang und die Art der  sonstigen Leistung | = | BA2 | Menge  und Art der gelieferten Gegenstände oder den Umfang und die Art der sonstigen  Leistung \(vgl. auch AEAO zu § 146, Nr. 2.1.3\) | = |  |  | &gt; | QU2 | Zweck  der Zahlung |
| 3 | RU3 | Zeitpunkt  der Lieferung bzw. sonstigen Leistung | = |  |  | &gt; | G3 | Datum  und Zeitpunkt des Umsatzes |  |  |  |  |  |  |  |  |  |  |  |  |
| 4 | RU4 | Ausstellungsdatum  der Rechnung     \(im Falle der Berichtigung gilt das Datum, an dem die Rechnung berichtigt  wird.\) | = | RK4 | Ausstellungsdatum  der Rechnung |  |  |  |  | BK4 | Datum  der Belegausstellung und den Zeitpunkt des Vorgangbeginns im Sinne des § 2  Satz 2 Nummer     Zeitpunkt der Vorgangsbeendigung im Sinne des § 2 Satz 2 Nummer 6 |  | BA4 | Datum  der Belegausstellung und den Zeitpunkt des Vorgangbeginns sowie den Zeitpunkt  der Vorgangsbeendigung \(vgl. AEAO zu § 146a, Nr. 3.6.3 „Zeitpunkt des  Vorgangsbeginns bzw. der Vorgangsbeendigung“\) |  |  |  |  | QU4 | Ort  und das Datum des Erhalts der Leistung oder Zahlung |
| 5 | RU5 | nach  Steuersätzen und -befreiungen aufgeschlüsseltes Entgelt für die Lieferung  oder sonstige Leistung | != | RK5 | Entgelt  und den darauf entfallenden Steuerbetrag für die Lieferung oder sonstige  Leistung in einer Summe \(Angabe des Bruttoentgelts inkl. Umsatzsteuer\) | &lt; | G5 | endgültiger  Einzelverkaufspreis | + | BK5 | Entgelt  und den darauf entfallenden Steuerbetrag für die Lieferung oder sonstige  Leistung in einer Summe | + | BA5 | Entgelt  und den darauf entfallenden Steuerbetrag für die Lieferung oder sonstige  Leistung in einer Summe | + |  |  |  | QU5 | Die  Höhe des Betrages in Zahlen und in Worten; Der Nettowert des Betrages sowie  der Mehrwertsteuersatz |
| 6 | RU6 | anzuwendender  Steuersatz oder      Im Falle einer Steuerbefreiung ist ein Hinweis auf die Steuerbefreiung  erforderlich \(z.B. ”Innergemeinschaftliche Lieferung”\);     Einen Hinweis auf die 2-jährige Aufbewahrungspflicht bei steuerpflichtigen  Werklieferungen oder sonstigen Leistungen im Zusammenhang mit einem  Grundstück, soweit der Leistungsempfänger kein Unternehmer ist oder zwar  Unternehmer ist, die Leistung aber für seinen nicht-unternehmerischen Bereich  bezieht;     Ggf. Hinweis auf die Steuerschuld des Leistungsempfängers  \(Reverse-Charge-Verfahren\), beispielsweise bei Bauleistungen sowie bei  Werklieferungen eines im Ausland ansässigen Unternehmers \(Einzelheiten siehe  § 13 b UStG | - | RK6 | anzuwendender  Steuersatz oder Hinweis auf eine Steuerbefreiung | &gt; | G6 | dazugehörige  Umsatzsteuersatz | = |  | anzuwendender  Steuersatz oder im Fall einer Steuerbefreiung einen Hinweis darauf, dass für  die Lieferung oder sonstige Leistung eine Steuerbefreiung gilt | = | BA6 | anzuwendenden  Steuersatz oder im Fall einer Steuerbefreiung einen Hinweis darauf, dass für  die Lieferung oder sonstige Leistung eine Steuerbefreiung gilt. | = |  |  |  |  |  |
| 7 | RU7 | auf  das Entgelt entfallender Steuerbetrag | - |  |  |  | G7 | dazugehörige  Umsatzsteuerbetrag |  |  |  |  |  |  |  |  |  |  |  |  |
| 8 | RU8 | im  Voraus vereinbarte Minderungen des Entgelts | - |  |  | = | G8 | vereinbarte  Preisminderungen | = |  |  | = |  |  | = |  |  |  |  |  |
| 9 | RU9 | vollständiger  Name des Leistungsempfängers | - |  |  | &gt; | G9 | Name  des Vertragspartners |  |  |  |  |  |  |  |  |  |  | QU9 | vollständiger  Name des Leistungsempfängers = Name des Zahlenden |
| 10 | RU10 | vollständige  Anschrift des Leistungsempfängers |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | QU10 | vollständige  Anschrift des      Leistungsempfängers |
| 11 | RU11 | Finanzamtsbezogene  Steuernummer \(Nach dem BMF-Schreiben vom 29. Januar 2004 müssen Name oder  Anschrift des Finanzamtes nicht genannt werden\) oder  Umsatzsteueridentifikationsnummer \(USt-IdNr.\) | - |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 12 | RU12 | Fortlaufende  Rechnungsnummer |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| 13 |  |  |  |  |  |  | G13 | Zahlungsart |  |  |  |  |  |  |  |  |  |  |  |  |
| 14 |  |  |  |  |  |  |  |  |  |  |  | &lt; | BA14 | Betrag je  Zahlungsart |  |  |  |  |  |  |
| 15 |  |  |  |  |  |  |  |  |  | BK15 | Transaktionsnummer  im Sinne des § 2 Satz 2 Nummer 2 |  | BA15 | Transaktionsnummer  i. S. d. § 2 Satz 2 Nummer 2 KassenSichV \(vgl. AEAO zu § 146a, Nr. 3.5\) |  |  |  |  |  |  |
| 16 |  |  |  |  |  |  |  |  |  | BK16 | Seriennummer  des elektronischen Aufzeichnungssystems oder die Seriennummer des  Sicherheitsmoduls. |  | BA16 | Seriennummer  des elektronischen Aufzeichnungssystems oder die Seriennummer des  Sicherheitsmoduls.     Auf dem Beleg ist die nach § 2 Satz 2 Nr. 8 KassenSichV protokollierte  Seriennummer anzugeben \(vgl. AEAO zu § 146a, Nrn. 3.6.1, 3.6.2\). |  |  |  |  |  |  |
| 17 |  |  |  |  |  |  |  |  |  |  |  |  | BA17 | Signaturzähler |  |  |  |  |  |  |
| 18 |  |  |  |  |  |  |  |  |  |  |  |  | BA18 | Prüfwert |  |  |  |  |  |  |
| 19 |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | BD19 | QR-Code |  |  |  |
| 20 |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | BD20 | Datum  der ersten Bestellung bei getrennter Bestell-Rechnungsverarbeitung      \(DSFinV-K 2.7.2\) |  |  |  |
| 21 |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  | QU21 | Die  Unterschrift und der Firmenstempel des Empfängers der Zahlung |
|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  | Anmerkungen |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  | GAa | Die  Möglichkeit zum Ausweis des Steuerbetrags in einer Summe nach § 32 UStDV in  der Rechnung und die Zusammenfassung des Entgelts und des darauf entfallenden  Steuerbetrags in einer Summe nach § 33 Satz 1 Nr. 4 UStDV in der Rechnung  bleiben unbenommen. |  | BKa | Die  Angaben auf einem Beleg müssen für jedermann ohne maschinelle Unterstützung  lesbar sein. Ein Beleg kann in Papierform oder mit Zustimmung des  Belegempfängers elektronisch in einem standardisierten Datenformat ausgegeben  werden. |  | BAa | Erfordert  ein Geschäftsvorfall \(vgl. AEAO zu § 146a, Nr. 1.7\) nicht die Erstellung  einer Rechnung i. S. d. § 14 UStG, sondern einen sonstigen Beleg \(z.B.  Lieferschein\), wird nicht beanstandet, wenn dieser Beleg nicht den unter § 6  Satz 1 Nr. 5 KassenSichV geforderten Steuerbetrag enthält. |  | BDa | DSFinV-K  2.7.2: Der Start-Zeitpunkt der ersten Transaktion „Bestellung“ muss  zusätzlich auf dem Bon abgedruckt werden |  | QUa | AEAO  § 146a 6.10 Die Befreiung von der Belegausgabepflicht nach § 146a Abs. 2 AO  entbindet den Unternehmer nicht von dem Anspruch des Kunden auf die  Ausstellung einer Quittung \(§ 368 BGB\). |
|  |  |  |  |  |  |  | GAb | Eine  Verpflichtung zur einzelnen Verbuchung \(im Gegensatz zur Aufzeichnung\) eines  jeden Geschäftsvorfalls besteht nicht. |  |  |  |  |  |  |  |  |  |  | QUb | Quercheck:     Zusätzlich zu Quittungen müssen Rechnungen beinhalten     Steuernummer     Lieferdatum / Leistungsdatum     Rechnungsnummer |
|  |  |  |  |  |  |  | GAc | Werden  der Art nach gleiche Waren mit demselben Einzelverkaufspreis in einer  Warengruppe zusammengefasst, wird dies nicht beanstandet, sofern die  verkaufte Menge bzw. Anzahl ersichtlich bleibt. |  |  |  |  |  |  |  |  |  |  | QUc | Rechnung  als Quittung mit Vermerk „Betrag erhalten“ |
|  |  |  |  |  |  |  | GAd | Dies  gilt entsprechend für Dienstleistungen. |  |  |  |  |  |  |  |  |  |  |  |  |
|  |  |  |  |  |  |  | GAe | Ausnahmen  aus Zumutbarkeitsgesichtspunkten siehe 2.2. |  |  |  |  |  |  |  |  |  |  |  |  |

