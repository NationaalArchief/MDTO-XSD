# Introductie

Dit gedeelte beschrijft welke documenten de documentatieset bevat en hoe het XML-schema is afgeleid van het MDTO metagegevensschema.

## Inhoud documentatieset
De documentatieset bestaat uit de volgende links en mappen in een .zip bestand.

MDTO-XML 1.0.1.xsd: Het XML-schema. (Eerdere versie MDTO-XML 1.0.xsd)
MDTO-XML 1.0.1.html: Weergave van het schema als HTML-pagina. Bedoeld voor lezers die geen speciale viewer voor XML-schema’s hebben.  (Eerdere versie MDTO-XML 1.0.html) 
MDTO-XML 1.0.1 Voorbeelden: Map met voorbeelden van XML-bestanden conform het XML-schema. 

Aanwijzing voor gebruik:

Sla het .zip bestand op op uw computer
Pak het .zip bestand uit en sla daarbij het bestand op op uw computer
Open het bestand met de juiste applicatie vanuit de bestandenmap op uw computer


### Toelichting op de voorbeelden
De voorbeeldbestanden zijn ter informatie en maken geen onderdeel uit van de definitie van het XML-schema en zijn dus ook geen onderdeel van de norm. Het doel van de voorbeelden is dat de lezer zich een voorstelling kan maken hoe een XML-bestand conform het XML-schema er uit hoort te zien. De voorbeelden zijn zo realistisch mogelijk. Voor een zo volledig mogelijke representatie zijn er ook fictieve waarden gebruikt, of combinaties van waarden gebruikt die in de praktijk niet of nauwelijks zullen voorkomen. 

De volgende voorbeelden zijn opgenomen

- **MDTO-XML 1.0.1 Voorbeeld Serie Informatieobject.xml:**
Metagegevens voor de serie “Deelprogramma Kust. Voorbereiding 2010-2014 adviezen en voorstellen voorkeursstrategie Kust en strategische beslissing Zand”.
- **MDTO-XML 1.0.1 Voorbeeld Dossier Informatieobject.xml:**
Metagegevens voor het dossier “Brondocumenten en literatuur bij synthesedocument voorkeursstrategie Kust en strategische beslissing Zand”.
- **MDTO-XML 1.0.1 Voorbeeld Archiefstuk Informatieobject.xml:**
Metagegevens voor het informatieobject “Atelier Kustkwaliteit, 2011. Ontwerpstudie Dwarsdoorsneden kust, vier Kustdoorsneden in beeld, Werkboek 2, Delft”. 
- **MDTO-XML 1.0.1 Voorbeeld Bestand.xml:**
Metagegevens voor het bestand “DC-2015_1753-1.PDF” dat de representatie is van “Atelier Kustkwaliteit, 2011. Ontwerpstudie Dwarsdoorsneden kust, vier Kustdoorsneden in beeld, Werkboek 2, Delft”.

De hiërarchische relaties tussen de voorbeelden staan weergegeven in het volgende schema: 

![image](images/images/XML-voorbeelden-structuur.png)

### Relatie tussen het MDTO metagegevensschema en het MDTO-XML schema
Het XML-schema is op de volgende manier afgeleid van het metagegevensschema:

- Op het hoogste niveau bevat het schema één element “MDTO” van het type “mdtoType”. Dit element is bedoeld om te markeren dat het XML-bestand MDTO-metagegevens bevat.
- Een waarde van het type “mdtoType” is ofwel een element “informatieobject” of een element “bestand”. Dit zijn de twee mogelijkheden die voor mogen komen in een XML-bestand met MDTO-metagegevens.
- Voor elk object of gegevensgroep uit het metagegevensschema bevat het XML-schema een corresponderend <complexType>  waarvan de naam eindigt op “Type”. 
- Elk object in MDTO bevat in ieder geval een identificatie en een naam. Deze attributen zijn bij objectType opgenomen en wordt als basis gebruikt van informatieobjectType en bestandType d.m.v. <xsd:extension base=”objectType”>.
- Elke complextype bevat een <sequence> met daarin voor elk bijbehorend attribuut uit het metagegevensschema een <element>-definitie. Dat wil zeggen voor elk attribuut met het betreffende object of gegevensgroep als domein.

Voor elk attribuut bevat de <element>-definitie:

- name = naam van het attribuut.
- type = het bereik van het attribuut.
- minOccurs = ondergrens van de kardinaliteit van het attribuut . 
- maxOccurs = bovengrens van de kardinaliteit van het attribuut. 
- <annotation><documentation> =  definitie van het attribuut.