# Testfall - Den glade piraten! #

## TF AF1 Registering av kund.##

Testar registrering av ny medlem/kund i klubben Den glade piraten. 

####Efterkrav

Kontrollera i systemet att registrering av medlem har genomförts. 

###TF 1.1 Huvudscenario

* 1. Gå till dengladepiraten.se
* 2. Inloggningssida presenteras.
* 2. Logga in som administratör (användarnamn: admin, lösenord: lösen).
* 3. Menyval visas. 
* 4. Välj medlems registrering.
* 5. Formulär för ny medlem visas.
* 6. Skriv in personuppgifter av ny medlem.
* 7. Systemet frågar efter båttyp.
* 8. Ange båttyp.
* 9. Systemet hämtar information om båt, och frågar om tillägsinformation.
* 10. Skriv in eventuell information, välj sedan ok. 
* 11. Systemet validerar uppgifterna som matats in.
* 12. Systemet presenterar lediga båtplatser som passar båttyp. 
* 13. Välj båtplats från alternativ.
* 14. Båtplats registreras.
* 15. Systemet frågar efter önskat inloggnings id, samt lösenord av ny medlem.
* 16. Skriv in önskat användarnamn, samt lösenord. 
* 17. Systemet checkar att användarnamn är ledigt. 
* 18. Ny medlem tilldelas sitt användarnamn och lösenord. 
* 19. Systemet uppdaterar alla listor med information om medlem. 
* 19. Lyckad registrering av ny medlem.  

###TF 1.2 Alternativtscenario, felaktiga personuppgifter.

Testar felhantering av personuppgifter i systemet. 

####Förkrav

Huvudscenario har följts från steg 1 till 5.

####Efterkrav

Fortsätt från steg 7 i huvudscenario. 

####Scenario

* 1. Felaktiga personuppgifter om medlem skrivs in.
* 2. Systemet visar felmeddelande.
* 3. Ändra uppgifter.
* 4. Lyckad registrering av personuppgifter.
    * 4a. Uppgifter stämmer inte, felmeddelande visas.  


###TF 1.3 Alternativtscenario, medlem vill inte ha båtplats. 

Testar registrering av medlem utan båt. 

####Förkrav

Huvudscenario har följts från steg 1 till 6.

####Efterkrav

Fortsätt från steg 15 i huvudscenario. 

####Scenario

* 1. Systemet frågar efter båttyp.
* 2. Välj fortsättning av registrering.
* 3. Systemet frågar om man verkligen vill fortsätta utan att ange båttyp. 
* 4. Ange fortsätt. 

###TF 1.4 Alternativtscenario, ingen båtplats finns.

Testar registrering av medlem, när båtplats önskas men ej finns tillgänglig.  

####Förkrav

Huvudscenario har följts från steg 1 till 11.

####Efterkrav

Fortsätt från steg 15 i huvudscenario.

####Scenario

* 1. Systemet hittar inga lediga båtplatser som passar båttypen, felmeddelande visas.
* 2. Välj kö lista för medlem.
    * 2a. Välj avsluta medlemregistrering om medlem ej vill vänta.  
* 3. Systemet registrerar medlem i kö listan. 
