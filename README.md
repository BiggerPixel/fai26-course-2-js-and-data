## Mål

Vi felsöker ett orderkvitto med bevis från Console och sidan.

För varje fel skriver vi först vad vi tror är fel.  
Sedan samlar vi ett synligt bevis innan vi ändrar koden.

När vi är klara ska kvittot visa rätt värden och Console ska vara utan felmeddelanden.

## Startfiler

Vi använder dessa färdiga filer:

- `index.html` innehåller gränssnittet för kvittot.
- `style.css` innehåller all CSS som behövs.
- `script.js` innehåller JavaScript med fem avgränsade fel.

Öppna `index.html` i en webbläsare. Öppna sedan **DevTools** och fliken Console. Vi ändrar bara `script.js`.

## Roller i gruppen

Vi arbetar i grupper och gör följande:

- läs koden och formulerar gruppens förutsägelse innan vi kör.
- spara och kör den ändring som gruppen har valt.
- Anteckna vad Console eller sidan faktiskt visar.

## Förväntat orderkvitto

Det färdiga kvittot ska visa:

- Produkt: `USB-C-hubb`.
- Antal: `2 st`.
- Styckpris: `399 kr`.
- Delsumma: `798 kr`.
- Frakt: `49 kr`.
- Totalt: `847 kr`.
- Stor order: `false`.

## Arbetssätt

Vi undersöker ett fel i taget. Vi undviker att ändra flera rader samtidigt eftersom det då blir svårt att veta vilken ändring som gav ett nytt resultat.

För varje fel dokumenterar vi följande i gruppens anteckningar:

1. **Förutsägelse:** vilken rad eller vilket uttryck tror vi orsakar problemet?
2. **Bevis:** vilket värde, vilken datatyp eller vilket felmeddelande ser vi?
3. **Ändring:** vilken enda ändring gör vi?
4. **Kontroll:** vad visar Console och sidan efter omladdning?

## Steg 1: Samla första beviset

1. Öppna sidan och läs hela Console från den första raden till felmeddelandet.
2. Jämför sidans värden med det förväntade orderkvittot.
3. Skriv ned allt som avviker utan att ändra koden ännu.
4. Leta upp filnamn och radnummer i felmeddelandet.

## Steg 2: Undersök värden och datatyper

1. Läs loggarna för `Antal`, `Delsumma`, `Frakt` och `Totalt`.
2. Jämför både värdet och resultatet från `typeof` med det som beräkningen behöver.
3. Välj ett avvikande värde och följ arbetsmönstret: förutsägelse, bevis, en ändring och kontroll.

## Steg 3: Undersök uttryck och operatorer

1. Räkna ut delsumman på papper med det förväntade antalet och styckpriset.
2. Läs uttrycket som skapar `subtotal` från vänster till höger.
3. Kontrollera vilken operator koden använder och vilket resultat Console visar.
4. Gör en avgränsad ändring och ladda om sidan.

## Steg 4: Följ följdfel

Ett fel tidigt i koden kan skapa flera felaktiga resultat senare. Vi fortsätter från `subtotal` till `total` och jämför efter varje ändring.

1. Förutsäg det nya värdet för `total` innan sidan laddas om.
2. Kontrollera värdet och datatypen i Console.
3. Leta efter nästa avvikelse om resultatet fortfarande är fel.

## Steg 5: Kontrollera jämförelsen

En stor order betyder i den här övningen minst tre produkter. Med två produkter ska jämförelsen därför ge `false`.

1. Läs jämförelseuttrycket utan att ändra det.
2. Förutsäg om uttrycket ger `true` eller `false`.
3. Jämför förutsägelsen med Console.
4. Korrigera operatorn om uttrycket beskriver en annan fråga än "minst tre".

## Steg 6: Läs felmeddelandet

1. Läs feltypen och namnet som nämns i Console.
2. Gå till angivet radnummer i `script.js`.
3. Jämför namnet på raden med de variabler som faktiskt har deklarerats.
4. Ändra endast det felaktiga namnet och ladda om sidan.

## Slutkontroll

Övningen är klar när vi kan markera alla punkter:

- [ ] Kvittot visar exakt de förväntade värdena.
- [ ] Console visar inga felmeddelanden.
- [ ] Console visar rimliga värden och datatyper för alla loggade variabler.
- [ ] Gruppen har dokumenterat fem fel med förutsägelse, observerat bevis, ändring och kontroll.

## Om tid finns

Ändra `quantity` till `3`. Förutsäg först `subtotal`, `total` och resultatet av jämförelsen. Kontrollera sedan förutsägelsen i Console och på sidan.
