# Kravspecifikation - Den glade piraten! #

## Aktörer ##

### Primära aktörer

**Kund**

Båtägare som vill ha sin båt hos klubben samt personer som är båtintreserade som vill vara medlemmar i klubben.
Vill enkelt kunna bli registrerade och få lätt tillgänglig information om händelser. 

**Sekreterare** 

Vill snabbt få information om ändringar i registeringar. Så att uppdateringar av avgiftslista, båtlista och båtplatser kan göra snarast efter ändringar. 
Detta för att kunna undvika onödiga frågor och problem från medlemmar.  


**Kassör** 

Vill att avgiftslistan är uppdaterad, så inga fel görs i samband med fakturering och betalning av båtplats samt medlemsavgift. 

**Räddningstjänsten**

Vill snabbt få tillgång till klubbens medlemsregister samt båtplatser vid eventuell olycka. 

### Sekundär Aktör

**Svenskt båtregister**

Att med hjälp av Svenskt båtregister få information om båttyp, bredd och längd för att kunna tilldela en passande båtplats till kund.  


### Offstage Aktör

**Datainspektionen**

Ser till att registreringen av nya medlemmar följer personuppgiftslagen (PuL). 

## Användningsfall ##

### 1. Sekreterare
* **AF1.1** Ny registering av kund.
* **AF1.2** Tilldelning av båtplats. 
* **AF1.3** Uppdatering av båtlista.
* **AF1.4** Uppdatering/Tilläggning av avgiftslista.
* **AF1.5** Uppdatering/Tilläggning av informationssida. 
* **AF1.6** Ta emot information från kund och kassör.  
* **AF1.7** Registrering/Uppdatering av information från kund. 

### 2. Kund
* **AF2.1** Uppdatering/registrering av kontaktuppgifter samt båtinformation.
* **AF2.2** Kontakt med sekreterare vid fel eller ändringar av AF2.1. 

### 3. Kassör
* **AF3.1** Registrering av betalda fakturor. 
* **AF3.2** Uppdatering av information om betalstatus. 

### 4. Räddningstjänsten
* **AF4.1** Information om medlemmar samt båtar vid olycka.  

## Kort beskrivinging av användningsfall ##

### AF1.1 Registering av kund.
Sekreteraren tar emot uppgifter av kund. 
Personuppgifterna samt båtuppgifterna registreras. 
Kassören tar emot eventuella fakturor. 
Kunden får ett unikt användar id samt lösenord för att själv kunna ändra viktig information i framtiden.

### AF1.2 Tilldelning av båtplats.
Beroende av båttyp och kund, tilldelas en/flera båtplatser. 
Detta registreras tillsammans med personuppgifter av kund i avgiftslistan för kassören. 
Ändring av båtplatser uppdateras i båtlistan så att räddningstjänsten vid behov kan få tillgång till rätt information. 

### AF1.7 Registrering/Uppdatering av information från kund och kassör. 
Om kunden uppdaterar sin information, kommer detta meddelas till sekreteraren.
När dessa uppgifter sedan validerats av sekreteraren kommer alla listor att uppdateras. 

### AF3.1 Registrering av betalda fakturor. 
Kassören registrerar betalda fakturor. Kassören stämmer av betald summa från kund med avgiftslistan, och uppdaterar därefter betalstatusen.


## AF1 Ny registering av kund. ##

###Primär Aktör

* Kund
* Sekreterare

###Sekundär Aktör

* Svenskt båtregister

###Offstage Aktör

* Datainspektionen 

### Huvudscenario

1. Alternativet ny medlem väljs. 
2. Systemet frågar efter aktörens personuppgifter. 
3. Aktören ger systemet sina personuppgifter.
4. Systemet frågar efter aktörens båttyp.
5. Aktören anger båttyp till systemet. 
6. Systemet hämtar uppgifter om båt från sekundär aktör. 
7. Aktören väljer båtplats. 
8. Systemet tilldelar aktören båtplats. 
9. Aktören väljer inloggnings uppgifter till systemet. 
10. Systemet uppdaterar alla listor med information om ny aktör. 


### Alternativa Scenarios

* 3a. Om aktören angett felaktiga personuppgifter. 
    * 1. aktören kontaktas. 
        * 1a. Fel rättas vid kontakt med aktören. 
        * 1b. Om aktören inte är anträffbar eller om uppgifterna fortfarande inte stämmer vid rättning, meddelas aktören och användningsfallet avslutas.

* 4a. Om aktören inte vill ha båtplats i föreningen.
    * 1. Medlemsavgift tas ut. Gå till steg 10.
    
* 6a. Om information av båttyp ej finns hos sekundär aktör.
    * 1. Systemet får kompletterande information av aktören.

* 8a. Om systemet inte hittar ledig båtplats.
    * 1. Aktören tillfrågas om väntlista.
        * 1a. Aktören sätts upp på väntlistan. Gå till steg 10.
        * 1b. Aktören är inte intresserad av att vänta. Användningsfallet avslutas.

### Regler vid registering av kund

**Personuppgiftslagen (PuL) måste följas.** 

### Frågor

* Exakt vilka båtuppgifter ska sytemet registrera? 
* Medlemsrabatt om flera aktörer ur samma familj finns i systemet? 
* Ska aktören få båtplattsrabatt vid fler än en båt?
* Hur ska systemet hanteras vid tekniska problem? 
* Vid avregistrering av aktör ska medlems/båtplatsavgift betalas tillbaka? 

    
