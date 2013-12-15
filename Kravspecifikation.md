# Kravspecifikation - Den glade piraten! #

## Aktörer ##

### Primära aktörer

**Kund**

Båtägare som vill ha sin båt hos klubben samt personer som är båtintreserade som vill vara medlemmar i klubben.
Vill enkelt kunna bli registrerade och få lätt tillgänglig information om händelser. 

** Sekreterare ** 

Vill snabbt få information om ändringar i registeringar. Så att uppdateringar av avgiftslista, båtlista och båtplatser kan göra snarast efter ändring. 
För att undvika onödiga frågor och problem från medlemmar.  


** Kassör ** 

Vill att avgiftslistan är uppdaterad, så inga fel görs i samband med fakturering och betalning av båtplats och medlemsavgift. 

** Räddningstjänsten **

Vill snabbt få tillgång till klubbens medlemregister och båtplatser vid eventuell olycka. 

### Sekundär Aktör

** Svenskt båtregister **

Att med hjälp av Svenskt båtregister få information av båttyp, bredd och längd för att kunna tilldela en passande båtplats till kund.  


### Offstage Aktör

** Datainspektionen **

Ser till att registreringen av nya medlemmar följer personuppgiftslagen (PuL). 

## Användningsfall ##

### 1. Sekreterare
* AF1.1 Ny registering av kund.
* AF1.2 Tilldelning av båtplats. 
* AF1.3 Uppdatering av båtlista.
* AF1.4 Uppdatering/Tilläggning av avgiftslista.
* AF1.5 Uppdatering/Tilläggning av informationssida. 
* AF1.6 Ta emot information från kund och kassör.  
* AF1.7 Registrering/Uppdatering av information från kund. 

### 2. Kund
* AF2.1 Uppdatering/registrering av kontaktuppgifter samt båtinformation.
* AF2.2 Kontakt med sekreterare vid fel eller ändringar av AF2.1. 

### 3. Kassör
* AF3.1 Registrering av betalda fakturor. 
* AF3.2 Uppdatering av information om betalstatus. 

### 4. Räddningstjänsten
* AF4.1 Ta emot båtlista vid olycka.  

## Kort beskrivinging av användningsfall ##

### AF1.1 Registering av kund.
Sekreteraren tar emot uppgifter av kund. 
Personuppgifterna samt båtuppgifterna registreras. 
Kassören tar emot ev. fakturor. 
Kunden får ett unikt användar id samt lösenord för att själv kunna ändra viktig information i framtiden.

### AF1.2 Tilldelning av båtplats.
Beroende av båttyp och kund, tilldelas en/flera båtplatser. 
Detta registreras tillsammans med personuppgifter av kund i avgiftslistan för kassören. 
Ändring av båtplatser uppdateras i båtlistan så att räddningstjänsten vid behov kan få tillgång till rätt information. 

### AF1.7 Registrering/Uppdatering av information från kund och kassör. 
Om kunden uppdaterar information, kommer detta meddelas sekreteraren.
När dessa uppgifter sedan validerats av sekreteraren kommer de olika listorna att uppdateras. 

### AF3.1 Registrering av betalda fakturor. 
Kassören registrerar betalda fakturor. Kassören stämmer av betald summa med avgiftslistan och uppdaterar därefter betalstatusen.


## AF1.1 Ny registering av kund. ##

###Primär Aktör

Kund
Sekreterare

###Sekundär Aktör

Svenskt båtregister

###Offstage Aktör

Datainspektionen 

### Huvudscenario

1. En ny kund vill bli medlem i båtklubben. 
2. Registrering av kundens personuppgifter.
3. Registrering av kundens båt.
4. Uppgifter om båt hämtas från svenskt båtregister. 
5. Avgift av båtplats sätts, änvänds sedan vid uppdatering av avgiftslista. 
6. Kund får inloggnings id samt lösenord till klubbens sida. 

### Alternativa Scenarios

* 2a. Om kund angett felaktiga personuppgifter. 
    * 1. Kund kontaktas. 
        * 1a. Fel rättas vid kontakt med kund. 
        * 1b. Om kund inte är anträffbar eller om uppgifterna fortfarande inte stämmer vid rättning, kontaktas kund och användningsfallet avslutas.

* 3a. Om kund inte har/vill ha båtplats i föreningen.
    * 1. Medlemsavgift tas ut. Gå till steg 6.
    
* 4a. Om information av båttyp ej finns i svenskt båtregister.
    * 1. Uppgifter får registreras manuellt av sekreteraren. Gå till steg 5.

* 5a. Om inga båtplatser finns till förfogande.
    * 1. Kunden tillfrågas om denna vill sättas upp på väntlista. 
        * 1a. Kunden sätts upp på listan. Gå till steg 6.
        * 1b. Kunden är inte intresserad av att vänta. Användningsfallet avslutas.  

### Regler vid registering av kund

** Personuppgiftslagen (PuL) måste följas. ** 

### Frågor

* Exakt vilka båtuppgifter ska registreras? 
* Medlemsrabatt med flera medlemmar ur samma familj?
* Båtplattsrabatt vid fler än en båt?
* Hur ska sekreteraren/kassören hantera tekniska problem? 
* Vid avregistrering ska medlems/båtplatsavgift betalas tillbaka? 

    
