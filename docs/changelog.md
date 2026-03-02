# Changelog

Alle noemenswaardige wijzigingen aan het MDTO XML-schema en de bijbehorende voorbeeldbestanden worden in dit document bijgehouden.

---

## [1.0.1]

### 2023-02-21 – XML-schema
**Wijzigingen:**
- `maxOccurs` bij attribuut **archiefvormer** aangepast naar `unbounded`.
- `minOccurs` bij attribuut **beperkingGebruik** aangepast naar `1`.

Beide attributen zijn hiermee in lijn gebracht met het MDTO-metagegevensschema.

**Overig:**
- Versienummer van het XML-schema bijgewerkt naar **1.0.1**.

---

### 2023-07-13 – Voorbeeldbestanden
**Toegevoegd:**
- MDTO-XML **1.0.1** voorbeeldbestanden toegevoegd.

**Aanpassingen:**
- Voorbeelden gekoppeld aan versie **1.0.1** van het XML-schema.
- In de XML-header is een verwijzing naar `schemaLocation` toegevoegd.
- Verwijzingen naar MDTO-begrippenlijsten zijn bijgewerkt.

---

### 2023-07-13 – Documentatie
**Verwijderd:**
- MDTO 1.0 diagrammen verwijderd uit de repository.  
  Deze zijn nog beschikbaar via het webarchief.

---

### 2025-08-13 – XML-voorbeeldbestanden (Nationaal Archief)
**Wijzigingen:**
- XML-voorbeeldbestanden aangepast op basis van daadwerkelijk bestaande informatieobjecten.
- Niet-werkende links vervangen.
- Extra attributen toegevoegd (o.a. **aanvullendeMetagegevens**) voor een completere representatie.
- Voor het objecttype **Bestand** is een correcte checksum toegevoegd.

**Documentatie:**
- Tekstuele toelichting aangepast: de voorbeelden zijn bedoeld om te laten zien hoe MDTO XML-bestanden er **uit horen te zien** (in plaats van *uit kunnen zien*).