# MDTO XML Schema – Documentatie en Voorbeelden

## Inleiding
Dit gedeelte beschrijft welke documenten de documentatieset bevat en hoe het XML-schema is afgeleid van het MDTO-metagegevensschema.

---

## Toelichting op de voorbeelden

De voorbeeldbestanden zijn uitsluitend ter informatie en maken **geen onderdeel uit van de definitie van het XML-schema**. Ze zijn dus ook **geen onderdeel van de norm**.

Het doel van de voorbeelden is om de lezer een duidelijk beeld te geven van hoe een XML-bestand dat voldoet aan het XML-schema eruit kan zien. De voorbeelden zijn zo realistisch mogelijk opgesteld. Voor een zo volledig mogelijke representatie zijn daarnaast fictieve waarden gebruikt, of combinaties van waarden die in de praktijk niet of nauwelijks zullen voorkomen.

### Opgenomen voorbeelden

- **MDTO-XML 1.0.1 Voorbeeld Serie Informatieobject.xml**  
  Metagegevens voor de serie:  
  *“Deelprogramma Kust. Voorbereiding 2010-2014 adviezen en voorstellen voorkeursstrategie Kust en strategische beslissing Zand”*.

- **MDTO-XML 1.0.1 Voorbeeld Dossier Informatieobject.xml**  
  Metagegevens voor het dossier:  
  *“Brondocumenten en literatuur bij synthesedocument voorkeursstrategie Kust en strategische beslissing Zand”*.

- **MDTO-XML 1.0.1 Voorbeeld Archiefstuk Informatieobject.xml**  
  Metagegevens voor het informatieobject:  
  *“Atelier Kustkwaliteit, 2011. Ontwerpstudie Dwarsdoorsneden kust, vier Kustdoorsneden in beeld, Werkboek 2, Delft”*.

- **MDTO-XML 1.0.1 Voorbeeld Bestand.xml**  
  Metagegevens voor het bestand:  
  *“DC-2015_1753-1.PDF”*, dat de representatie is van:  
  *“Atelier Kustkwaliteit, 2011. Ontwerpstudie Dwarsdoorsneden kust, vier Kustdoorsneden in beeld, Werkboek 2, Delft”*.

---

## Relatie tussen het MDTO-metagegevensschema en het MDTO-XML schema

Het XML-schema is op de volgende manier afgeleid van het metagegevensschema:

- Op het hoogste niveau bevat het schema één element **`MDTO`** van het type **`mdtoType`**.  
  Dit element markeert dat het XML-bestand MDTO-metagegevens bevat.

- Een waarde van het type **`mdtoType`** is:
  - een element **`informatieobject`**, of  
  - een element **`bestand`**.  
  Dit zijn de twee mogelijke hoofdstructuren binnen een XML-bestand met MDTO-metagegevens.

- Voor elk object of gegevensgroep uit het metagegevensschema bevat het XML-schema een corresponderend **`<complexType>`** waarvan de naam eindigt op **`Type`**.

- Elk object in MDTO bevat minimaal:
  - een identificatie  
  - een naam  

  Deze attributen zijn opgenomen in **`objectType`** en worden als basis gebruikt voor:
  - **`informatieobjectType`**
  - **`bestandType`**

  via:

  ```xml
  <xsd:extension base="objectType">