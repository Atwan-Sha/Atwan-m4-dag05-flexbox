# Dag 5 · Flexbox

*Modul 4, UI/UX & Frontendutveckling, Lexicon IT-Proffs*

## Vad du ska göra idag

Du lägger ut menyn, sidhuvudet och sidfoten med Flexbox, och lär dig skillnaden mellan huvudaxel och korsaxel.

## Bakgrund

Flexbox ordnar element i **en dimension**: en rad eller en kolumn. Du sätter `display: flex` på **parent**, och children ordnar sig. Det är samma tänk som Auto layout i Figma, och du har redan gjort det i modul 3.

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

## Kontrollista: så vet du att du är klar

- [ ] Menyn, sidhuvudet och sidfoten är byggda med Flexbox.
- [ ] Du har använt `gap` istället för marginaler mellan flex items.
- [ ] Priset ligger längst ned i varje kort.
- [ ] `flex-wrap: wrap` finns där det behövs, och sidan går inte sönder på smal skärm.
- [ ] Du kan förklara huvudaxel och korsaxel.
- [ ] Du har pushat till din fork och skickat in länken.

## Tips om du fastnar

- Inget händer? `display: flex` ska på PARENT, inte på children.
- `justify-content` och `align-items` byter roller när du ändrar `flex-direction`. Det är normalt.
- Använd DevTools: klicka på `flex`-ikonen bredvid elementet, så ritas axlarna ut.

## Inlämning

**Deadline: imorgon klockan 09.00.** Allt lämnas in i Microsoft Forms. Du behöver inte redovisa något muntligt.

I formuläret fyller du i:

1. Länk till din fork av det här repot.
2. Reflektion: Vilken Flexbox-egenskap var mest förvirrande, och hur skulle du förklara den för en kollega?

## Vill du mer? (frivilligt)

- Gör menyn till en hamburgarmeny-liknande layout för smal skärm med enbart CSS.
- Använd `flex-grow` för att låta ett fält i formuläret fylla resten av raden.
