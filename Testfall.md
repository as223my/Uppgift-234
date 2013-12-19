# Testfall - Den glade piraten! #

## TF AF1 Registrering av kund.##

Testar registrering av ny medlem/kund i klubben Den glade piraten. 
####Förkrav

Adminstratören är inloggad på Den glade piratens hemsida.  

####Efterkrav

Kontrollera i systemet att registrering av medlem har genomförts. 

###TF 1.1 Huvudscenario

* 1. Välj registrera ny medlem i menyvalet. 
* 2. Formulär för ny medlem visas, och systemet frågar efter personuppgifter.
* 3. Skriv in förnamn: anna, efternamn: Andersson, personnummer(900526-1234), och telefonnummer 031-44443.  
* 4. Systemet godkänner personuppgiftena och frågar efter medlemmens båttyp. 
* 5. Ange båttyp: Nimbus 34 Nova. 
* 6. Systemet hämtar uppgifter om båt, och frågar efter tilläggsinformation.
* 7. Välj/byt ut båtbredd till 3m, båtlängd till 8m och båtdjup till 1,5m. 
* 8. Systemet letar upp båtplatser som passar till dessa mått.
* 9. Välj båtplats. 
* 10. Systemet registrerar val av båtplats, och frågar efter inloggningsuppgifter. 
* 11. Välj användarnamn: Anna11 lösenord: Anna11.
* 12. Systemet godkänner inloggnings uppgifterna och uppdaterar alla listor med information om ny medlem.

###TF 1.2 Alternativtscenario, felaktiga personuppgifter.

Testar felhantering av personuppgifter i systemet. 

####Förkrav

Huvudscenario har följts från steg 1 till 3.

####Scenario

* 1. Felaktiga personuppgifter om medlem skrivs in.
* 2. Systemet visar felmeddelande.
* 3. Ändra personuppgifter.
* 4. Lyckad registrering av personuppgifter.
    * 4a. Uppgifter stämmer inte, felmeddelande visas.  
* 5. Fortsätter med steg 4 i huvudscenario.

###TF 1.3 Alternativtscenario, medlem vill inte ha båtplats. 

Testar registrering av medlem utan båt. 

####Förkrav

Huvudscenario har följts från steg 1 till 4.

####Scenario

* 1. Systemet frågar efter båttyp.
* 2. Välj fortsättning av registrering.
* 3. Systemet frågar om man verkligen vill fortsätta utan att ange båttyp. 
* 4. Ange fortsätt. 
* 5. Fortsätter med steg 10 i huvudscenario.
 

###TF 1.4 Alternativtscenario, ingen båtplats finns.

Testar registrering av medlem, när båtplats önskas men ej finns tillgänglig.  

####Förkrav

Huvudscenario har följts från steg 1 till 8.

####Scenario

* 1. Systemet hittar inga lediga båtplatser som passar båttypen, felmeddelande visas.
* 2. Välj kö lista för medlem.
    * 2a. Välj avsluta medlemregistrering om medlem ej vill vänta.  
* 3. Systemet registrerar medlem i kö listan. 
* 4. Fortsätter med steg 10 i huvudscenario.
