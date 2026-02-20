# Conceptional model: library provenance research domain ontology (*WIP*)
This domain ontology seeks to minutely describe the kind of data one collects when recording provenance markers in library collections, that is, in books and periodicals. I've tried to follow the WEMI class logic by using the IFLA LRMoo extension of CRM (F5 Item as a sub class of E24 Physical Human-Made Thing). 

---
### Begründungen der Modellierungsentscheidungen:
| Pfad | Bedeutung | Warum so modelliert? |
|------|-----------|---------------------|
| **F5 → R7 exemplifies → F3 Manifestation** | WEMI-Relation | Exemplar hängt im Bibliothekskatalog an einem Titeldatensatz (Manifestation), in dem das Expl. näher beschrieben wird (z.B. mit Titel)  |
| **F3 → P102 has title → E35 Title** | Die Manifestation hat einen Titel | Mit E35 als eigenes Konzept nicht bloßer Text |
| **F3 → P1 is identified by → E42 Identifier** | Identifikator des Titeldatensatzes im K10Plus | Eindeutiger Code, der einem K10Plus-Datensatz zugewiesen wird, keine Freitext |
| **F5 Exemplar → P51 has current owner → E74 Group → E42 ISIL** | Exemplar ist im Besitz einer Bibliothek | Bibliothke wird durch **eindeutigen, persistenten Identifikator** bezeichnet  |
| **F5 Exemplar → P1 is identified by → E42 Identifier** | Identifikator des Exemplar | Eindeutiger Code (EPN K10Plus-Exemplardatensatensatz), Inventar-Nr., keine Freitext |
| **F5 Exemplar → P65 shows visual item → E36 Visual Item → P138 represents → E1 CRM Entity** | Provenienzmerkmale | E36 Visual Item, P138 represents (has representation) to E1 CRM Entity, which in addition captures the optical features of the depiction [noch unsicher, ggf. persistente Ident. + E55 Type of Provenance marker etc.] |
| <span style="color:grey"> **F5 Exemplar → P128 carries → E34 Inscription → P3 has note → E62 String** | ALT. für Provenienzmerkal & Freitext | unsicher, ob dies nicht die bessere Variante ist </span>| 
| **F5 Exemplar → P2 has type → E55 Type → P127 has narrower term → E55 Type** | Exemplartyp | Exemplartyp nach T-Pro Thesaurus, z.B. "Exemplar: Widmungsempfänger"  |
| **F5 Exemplar → P54 has current permanent location → E53 Place** | Aktueller Standort | Sgn. und evtl. GND-Geografika?  |
