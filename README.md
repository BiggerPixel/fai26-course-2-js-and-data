## Mål

Vi bygger färdigt ett orderkvitto genom att skriva JavaScript i `script.js`. Vi använder värden, datatyper, `const`, `let`, uttryck och operatorer. Vi förutsäger resultaten innan vi kör koden och använder Console som bevis.

HTML och CSS är redan klara. Allt arbete sker i `script.js`.

## Startfiler

Vi använder dessa filer:

- `index.html` innehåller det färdiga gränssnittet.
- `style.css` innehåller all CSS som behövs.
- `script.js` innehåller startvärden och markerade `TODO`-kommentarer.

Öppna `index.html` i en webbläsare. Öppna sedan DevTools och fliken Console. I början visar kvittot streck och Console visar inga kontroller. Det är den förväntade startpunkten.

## Uppgiften

Kvittot gäller tre skrivbordslampor. Varje lampa kostar `529 kr` och frakten kostar `69 kr`.

Det färdiga kvittot ska visa:

- Produkt: `Skrivbordslampa`.
- Antal: `3 st`.
- Styckpris: `529 kr`.
- Delsumma: `1587 kr`.
- Frakt: `69 kr`.
- Totalt: `1656 kr`.
- Stor order: `false`.
- Status: `Beräknad`.

En stor order betyder minst fyra produkter.

## Steg 1: Läs startvärdena

Öppna `script.js`. Läs värdena för `productName`, `unitPrice`, `quantity`, `shipping`, `largeOrderLimit` och `orderStatus`.

Skriv ned vilken datatyp varje värde har. Kontrollera sedan förutsägelsen genom att tillfälligt använda `console.log` tillsammans med `typeof`.

Ta bort de tillfälliga loggarna när kontrollen är klar.

## Steg 2: Beräkna delsumman

Ett uttryck är kod som beräknar ett värde. Ersätt startvärdet för `subtotal` med ett uttryck som multiplicerar styckpriset med antalet.

Innan sidan laddas om skriver vi ned vilket resultat och vilken datatyp uttrycket bör ge. Lägg sedan till en logg som visar både värdet och typen:

```javascript
console.log("Delsumma:", subtotal, typeof subtotal);
```

Kontrollera att Console visar `1587` och `number`.

## Steg 3: Beräkna totalsumman

Ersätt startvärdet för `total` med ett uttryck som adderar frakten till delsumman. Använd variabelnamnen i uttrycket. Skriv inte in det färdiga resultatet `1656`.

Förutsäg resultatet och datatypen. Lägg sedan till en Console-logg för `total` med samma mönster som i föregående steg.

## Steg 4: Jämför antalet med gränsen

Ett jämförelseuttryck ger värdet `true` eller `false`. Ersätt startvärdet för `isLargeOrder` med en jämförelse som frågar om `quantity` är större än eller lika med `largeOrderLimit`.

Förutsäg resultatet. Lägg sedan till en Console-logg som visar värdet och datatypen för `isLargeOrder`.

## Steg 5: Ändra orderstatus

`orderStatus` är deklarerad med `let` eftersom värdet ska ändras. Tilldela texten `"Beräknad"` till variabeln efter beräkningarna.

Detta är en omtilldelning: variabeln behåller sitt namn men får ett nytt värde.

## Steg 6: Visa värdena i gränssnittet

Ersätt strecken i de markerade raderna längst ned i `script.js`. Tilldela varje element rätt variabel.

När en etikett behövs använder vi strängkonkatenering. Det betyder att vi sätter ihop text och värden med operatorn `+`. Antalet kan exempelvis visas så här:

```javascript
document.querySelector("#quantity").textContent = quantity + " st";
```

Skriv motsvarande tilldelningar för produkt, styckpris, delsumma, frakt, total, stor order och status.

## Steg 7: Kontrollera resultatet

Ladda om sidan och jämför med det förväntade orderkvittot. Läs sedan hela Console.

Utmaningen är klar när vi kan markera alla punkter:

- [ ] Kvittot visar produktnamn, antal, styckpris, delsumma, frakt och total.
- [ ] Delsumma och total beräknas med variabelnamn och uttryck, inte kopierade resultat.
- [ ] Console visar minst tre mellanvärden tillsammans med deras datatyper.
- [ ] Jämförelsen för stor order ger `false`.
- [ ] Statusen ändras från `Påbörjad` till `Beräknad`.
- [ ] Console visar inga felmeddelanden.

## Jämför i par

När kärnuppgiften är klar jämför vi i par:

1. Vi visar våra tre förutsägelser och resultaten i Console.
2. Vi väljer ett uttryck var och förklarar dess värden och operator.
3. Vi kontrollerar att båda lösningarna beräknar resultat i stället för att skriva in slutsummorna direkt.

## Om tid finns

Ändra `quantity` till `4`. Förutsäg först den nya delsumman, totalsumman och om stor order blir `true` eller `false`. Ladda sedan om sidan och kontrollera alla tre resultaten i Console och i kvittot.
