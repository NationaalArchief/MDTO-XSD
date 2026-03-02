# 📘 MDTO XML-Schema

## Inleiding

**MDTO (Metagegevens voor Duurzaam Toegankelijke Overheidsinformatie)** is een norm voor het eenduidig vastleggen en uitwisselen van metagegevens, met het doel de **duurzame toegankelijkheid van overheidsinformatie** mogelijk te maken.  

Het schema richt zich op generieke metagegevens die gelden voor (bijna) alle overheidsorganisaties, werkprocessen en informatiesoorten.  
MDTO sluit aan op de verplichtingen zoals opgenomen in de *Archiefregeling 2009*.  

➡️ Meer informatie: [Nationaal Archief – MDTO](https://www.nationaalarchief.nl/archiveren/mdto)

----

## Doel van het XML-schema

Het XML-schema beschrijft de XML-syntax waarmee MDTO-metagegevens conform het metagegevensmodel kunnen worden vastgelegd en uitgewisseld.  
Het schema maakt het mogelijk om systemen en koppelingen te ontwerpen waarin consistente metagegevens worden gebruikt — wat bijdraagt aan betere gegevensuitwisseling, lagere vertaalkosten en hogere kwaliteit van metagegevens.

📄 **Schema-locatie:**  
[https://www.nationaalarchief.nl/archiveren/mdto/xml-schema](https://www.nationaalarchief.nl/archiveren/mdto/xml-schema)

---

## Namespace en opbouw

- **Namespace:** `https://www.nationaalarchief.nl/mdto`  
- **Hoofdelement:** `<MDTO>` van het type `mdtoType`  
- Binnen het schema worden o.a. de objecttypen **Informatieobject** en **Bestand** onderscheiden, elk met hun eigen set metagegevens.  
- Het schema is uitbreidbaar en kan worden toegepast in verschillende contexten binnen het archief- en informatiemanagementdomein.

---

## Versiebeheer en publicatie

Het schema wordt onderhouden en gepubliceerd door het **Nationaal Archief**.  
Voor elke officiële wijziging wordt een nieuwe versie uitgegeven, bijvoorbeeld `MDTO-XML1.0.1.xsd`.  

Versies worden beheerd via **GitHub** en zijn publiek beschikbaar.  
Gebruikers wordt aangeraden in hun implementaties en documentatie altijd de gebruikte schema-versie te vermelden.

> **Tip:** Voor publicatie kan een stabiele URL worden gebruikt, zoals  
> `https://www.nationaalarchief.nl/mdto/MDTO-XML.xsd`  
> Deze kan verwijzen (redirecten) naar de meest recente versie, terwijl oudere versies onder hun specifieke naam blijven bestaan.

---

## 📂 Voor wie is dit schema bedoeld?

Het MDTO-schema is bedoeld voor:

- Overheidsorganisaties die metadata van blijvend te bewaren informatieobjecten vastleggen en uitwisselen.  
- Leveranciers van informatiesystemen en archiveringsoplossingen die interoperabiliteit en duurzame toegankelijkheid ondersteunen.  
- Beheerders van informatiesystemen die gebruikmaken van koppelingen of uitwisselformaten tussen organisaties.

---

## 📌 Meer informatie

- Website: [Nationaal Archief – MDTO](https://www.nationaalarchief.nl/archiveren/mdto)  
- Schema’s: [XML-Schema – MDTO](https://www.nationaalarchief.nl/archiveren/mdto/xml-schema)  
- Contact: [info@nationaalarchief.nl](mailto:info@nationaalarchief.nl)

---

© Nationaal Archief – MDTO XML-Schema  
Laatste update: **v1.0.2**

