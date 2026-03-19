# XML-schema

## mdtoType

**Beschrijving:** Dit type vertegenwoordigt een metadata-object dat óf een `informatieobject` óf een `bestand` kan bevatten.

| Naam element                                                                                                                                                                                 | Verplicht | Herhaalbaar | Datatype             |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ----------- | -------------------- |
| informatieobject   <br> <small>Een op zichzelf staand geheel van gegevens met een eigen identiteit. (bron: DUTO-eisen)</small>                                                               | Ja        | Nee         | informatieobjectType |
| bestand            <br> <small>Een geordende verzameling van gegevens in elektronische vorm, die door een elektronisch apparaat onder één naam kan worden behandeld en aangesproken.</small> | Ja        | Nee         | bestandType          |

---

## objectType

**Beschrijving:** Basisobjecttype waar `informatieobjectType` later op voortbouwt.  

| Naam element                                                                                         | Verplicht | Herhaalbaar | Datatype              |
| ---------------------------------------------------------------------------------------------------- | --------- | ----------- | --------------------- |
| identificatie      <br> <small>Gegevens waarmee het object geïdentificeerd kan worden.</small>       | Ja        | Ja          | identificatieGegevens |
| naam               <br> <small>Een betekenisvolle aanduiding waaronder het object bekend is.</small> | Ja        | Nee         | xsd:string            |

---

## informatieobjectType

**Beschrijving:** Extensie van `objectType` met extra metadata specifiek voor informatieobjecten.

| Naam element                                                                                                                                            | Verplicht | Herhaalbaar | Datatype                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- | ----------- | ----------------------------------- |
| aggregatieniveau             <br> <small>Het aggregatieniveau van het informatieobject.</small>                                                         | Nee       | Nee         | begripGegevens                      |
| classificatie                 <br> <small>Ordening van informatieobjecten in een logisch verband, zoals vastgelegd in een classificatieschema.</small>  | Nee       | Ja          | begripGegevens                      |
| trefwoord                     <br> <small>Trefwoord dat aan het informatieobject is toegekend.</small>                                                  | Nee       | Ja          | xsd:string                          |
| omschrijving                  <br> <small>Omschrijving van de inhoud van het informatieobject.</small>                                                  | Nee       | Ja          | xsd:string                          |
| raadpleeglocatie              <br> <small>Actuele verwijzing naar de locatie waar het informatieobject ter inzage ligt.</small>                         | Nee       | Ja          | raadpleeglocatieGegevens            |
| dekkingInTijd                 <br> <small>Tijdstip of periode waarop de inhoud van het informatieobject betrekking heeft.</small>                       | Nee       | Ja          | dekkingInTijdGegevens               |
| dekkingInRuimte               <br> <small>Plaats of locatie waar de inhoud van het informatieobject betrekking op heeft.</small>                        | Nee       | Ja          | verwijzingGegevens                  |
| taal                          <br> <small>De taal waarin het informatieobject gesteld is.</small>                                                       | Nee       | Ja          | xsd:language                        |
| event                         <br> <small>Gebeurtenis die heeft plaatsgevonden m.b.t. ontstaan, wijzigen, vernietigen of beheer van dit object.</small> | Nee       | Ja          | eventGegevens                       |
| waardering                     <br> <small>Waardering van het informatieobject volgens de vastgestelde selectielijst.</small>                           | Ja        | Nee         | begripGegevens                      |
| bewaartermijn                  <br> <small>Termijn waarin het informatieobject bewaard dient te worden.</small>                                         | Nee       | Nee         | termijnGegevens                     |
| informatiecategorie            <br> <small>Informatiecategorie waarop de bewaartermijn is gebaseerd.</small>                                            | Nee       | Nee         | begripGegevens                      |
| isOnderdeelVan                 <br> <small>De direct bovenliggende aggregatie waar dit object onderdeel van is.</small>                                 | Nee       | Ja          | verwijzingGegevens                  |
| bevatOnderdeel                 <br> <small>Een informatieobject dat direct onderliggend onderdeel is van deze aggregatie.</small>                       | Nee       | Ja          | verwijzingGegevens                  |
| heeftRepresentatie             <br> <small>Verwijzing naar het bestand dat een representatie van het object is.</small>                                 | Nee       | Ja          | verwijzingGegevens                  |
| aanvullendeMetagegevens        <br> <small>Verwijzing naar een bestand met aanvullende metagegevens.</small>                                            | Nee       | Ja          | verwijzingGegevens                  |
| gerelateerdInformatieobject    <br> <small>Relatie met een ander informatieobject dat relevant is.</small>                                              | Nee       | Ja          | gerelateerdInformatieobjectGegevens |
| archiefvormer                  <br> <small>Organisatie verantwoordelijk voor het opmaken en/of ontvangen van het object.</small>                        | Ja        | Ja          | verwijzingGegevens                  |
| betrokkene                     <br> <small>Persoon of organisatie relevant voor ontstaan en gebruik van dit object.</small>                             | Nee       | Ja          | betrokkeneGegevens                  |
| activiteit                     <br> <small>Bedrijfsactiviteit waarbij het object is ontvangen of gemaakt.</small>                                       | Nee       | Nee         | verwijzingGegevens                  |
| beperkingGebruik               <br> <small>Een beperking die gesteld is aan het gebruik van het object.</small>                                         | Ja        | Ja          | beperkingGebruikGegevens            |

## bestandType

**Beschrijving:** Extensie van `objectType` dat een digitaal bestand representeert met specifieke metadata zoals omvang, bestandsformaat en checksums.

| Naam element                                                                                                                            | Verplicht | Herhaalbaar | Datatype           |
| --------------------------------------------------------------------------------------------------------------------------------------- | --------- | ----------- | ------------------ |
| omvang                <br> <small>Aantal bytes in het bestand.</small>                                                                  | Ja        | Nee         | xsd:integer        |
| bestandsformaat       <br> <small>De manier waarop de informatie in een computerbestand binair gecodeerd is.</small>                    | Ja        | Nee         | begripGegevens     |
| checksum              <br> <small>Gegevens om te bepalen of het bestand beschadigd of gewijzigd is.</small>                             | Ja        | Ja          | checksumGegevens   |
| URLBestand            <br> <small>Actuele verwijzing naar het bestand.</small>                                                          | Nee       | Nee         | xsd:anyURI         |
| isRepresentatieVan    <br> <small>Verwijzing naar het informatieobject waarvan het bestand een (deel van een) representatie is.</small> | Ja        | Nee         | verwijzingGegevens |