# Dag 5 · Flexbox

*Modul 4, UI/UX & Frontendutveckling, Lexicon IT-Proffs*

## Vad du ska göra idag

Du lägger ut menyn, sidhuvudet och sidfoten med Flexbox, och lär dig skillnaden mellan huvudaxel och korsaxel.

## Bakgrund

Flexbox ordnar element i **en dimension**: en rad eller en kolumn. Du sätter `display: flex` på **föräldern**, och barnen ordnar sig. Det är samma tänk som Auto layout i Figma, och du har redan gjort det i modul 3.

## Så arbetar du (samma som alltid)

1. **Forka** dagens repo på GitHub (*Fork → Create fork*).
2. **Klona din fork:** *Code → HTTPS → kopiera adressen*. I terminalen (Ctrl+ö i VS Code): `git clone <adressen>`. Öppna den nya mappen i VS Code och starta *Live Server*.
3. **Gör uppgiften.** Spara och kontrollera i webbläsaren efter varje steg. Gör en commit efter varje avslutat steg: `git add .` och `git commit -m "Beskriv vad du gjorde"`.
4. **Skicka upp** när du är klar: `git push`.
5. **Lämna in i Microsoft Forms.**

Fastnar du: skriv ner exakt var och vad du försökt, och ta det först i nästa handledda pass.

## Uppgiften steg för steg

### Steg 1. Menyn på rad

`nav ul` ska visa länkarna på en rad med `display: flex` och `gap: 20px`. Testa sedan `flex-direction: column` och byt tillbaka.

### Steg 2. Sidhuvudet med justering

Gör `header` till en flexbehållare. Rubriken ska ligga till vänster och menyn till höger (`justify-content: space-between`), vertikalt centrerade (`align-items: center`). Lägg till `flex-wrap: wrap` så att det bryter snyggt när det är trångt.

### Steg 3. Sidfoten

Samma teknik: copyrightraden till vänster, adressen till höger, med `gap` för luft.

### Steg 4. Kort med jämn höjd

Gör `article` till en flexbehållare i kolumn (`flex-direction: column`). Ge `.pris` `margin-top: auto` så att priset alltid hamnar längst ned i kortet, oavsett textlängd.

### Steg 5. Experimentera

I DevTools: ändra `justify-content` till `center`, `flex-end`, `space-around`. Ändra `align-items`. Skriv i en kommentar vad varje värde gör, med egna ord.

### Steg 6. Rita axlarna

Rita på papper en flexrad och en flexkolumn och märk ut *huvudaxel* och *korsaxel*. Skriv vilken egenskap som styr var och en.

## AI-spåret (nivå 2: Specificera och jämför)

**Specificera layouten i ord** (cirka 25 minuter, efter att du gjort din egen lösning)

Du beskriver vad som ska byggas, AI föreslår kod, du testar, jämför och förstår. Att kunna beskriva exakt vad som ska byggas är en av de viktigaste färdigheterna när AI skriver koden.

Regler: egen lösning först, du ska kunna förklara varje rad, och du loggar i `docs/ai-logg.md` i `mitt-projekt`. Reglerna finns i `AI-REGLER.md` i `mitt-projekt`.

1. Skriv en specifikation på 3–5 meningar för menyn och sidhuvudet. Beskriv riktning, avstånd och justering.
2. Be AI skriva Flexbox-koden med prompten nedan.
3. Testa resultatet. Fungerar det? Om inte: ändra specifikationen, inte koden, och försök igen.
4. Jämför med din egen lösning från övningen. Förklara varje flex-egenskap i en kodkommentar.
5. Logga hur många försök specifikationen krävde.

Prompt att utgå från:

```
Skriv CSS med Flexbox för detta:
[din specifikation]
Använd klassnamnen i min HTML.
Förklara varje egenskap med en kommentar.

[klistra in din HTML här]
```

**Kontrollera med:**

- Titta på flex-markeringen i DevTools Elements.
- Testa på smal skärm.
- Kan du förklara varje rad utan att titta?

**I ditt projekt:** Skriv en specifikation för en komponent i din design och låt AI bygga den. Förklara varje rad.

## Kontrollista: så vet du att du är klar

- [ ] Menyn, sidhuvudet och sidfoten är byggda med Flexbox.
- [ ] Du har använt `gap` istället för marginaler mellan flexbarn.
- [ ] Priset ligger längst ned i varje kort.
- [ ] `flex-wrap: wrap` finns där det behövs, och sidan går inte sönder på smal skärm.
- [ ] Du kan förklara huvudaxel och korsaxel.
- [ ] Du har pushat till din fork och skickat in länken.
- [ ] Du har gjort AI-uppgiften och skrivit en post i `docs/ai-logg.md`.

## Tips om du fastnar

- Inget händer? `display: flex` ska på FÖRÄLDERN, inte på barnen.
- `justify-content` och `align-items` byter roller när du ändrar `flex-direction`. Det är normalt.
- Använd DevTools: klicka på `flex`-ikonen bredvid elementet, så ritas axlarna ut.

## Ditt projekt: Dagens steg i `mitt-projekt`

Efter övningen här jobbar du vidare i ditt eget projekt (din design från modul 3). Dagens steg står i `PROJEKTSTEG.md` i ditt repo `mitt-projekt`, under **Dag 5**. Det är där ditt riktiga arbete växer. Övningen här är träningsbanan.

## Inlämning

**Deadline: imorgon klockan 09.00.** Allt lämnas in i Microsoft Forms. Du behöver inte redovisa något muntligt.

I formuläret fyller du i:

1. Länk till din fork av det här repot.
2. Länk till ditt `mitt-projekt`.
3. Reflektion: Vilken Flexbox-egenskap var mest förvirrande, och hur skulle du förklara den för en kollega?

## Vill du mer? (frivilligt)

- Gör menyn till en hamburgarmeny-liknande layout för smal skärm med enbart CSS.
- Använd `flex-grow` för att låta ett fält i formuläret fylla resten av raden.
