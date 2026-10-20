# Dag 7 · Responsiv design

*Modul 4, UI/UX & Frontendutveckling, Lexicon IT-Proffs*

## Vad du ska göra idag

Du gör hela sajten responsiv enligt *mobile first*, med brytpunkter vid 600 px och 900 px, och testar den i DevTools enhetsläge.

## Bakgrund

Responsiv design betyder att samma sida fungerar på alla skärmar. **Mobile first** innebär att du skriver CSS för den minsta skärmen först, och lägger till mer med `@media (min-width: ...)` när det finns plats. Du har redan en bra grund eftersom du byggt layouten med flex och grid.

## Så arbetar du (samma som alltid)

1. **Forka** dagens repo på GitHub (*Fork → Create fork*).
2. **Klona din fork:** *Code → HTTPS → kopiera adressen*. I terminalen (Ctrl+ö i VS Code): `git clone <adressen>`. Öppna den nya mappen i VS Code och starta *Live Server*.
3. **Gör uppgiften.** Spara och kontrollera i webbläsaren efter varje steg. Gör en commit efter varje avslutat steg: `git add .` och `git commit -m "Beskriv vad du gjorde"`.
4. **Skicka upp** när du är klar: `git push`.
5. **Lämna in i Microsoft Forms.**

Fastnar du: skriv ner exakt var och vad du försökt, och ta det först i nästa handledda pass.

## Uppgiften steg för steg

### Steg 1. Kontrollera viewport-taggen

Båda HTML-filerna måste ha `<meta name="viewport" ...>`. Utan den fungerar inget av det du gör idag.

### Steg 2. Testa i enhetsläget

Öppna DevTools och klicka på enhetsikonen (Ctrl+Shift+M). Testa 360, 768 och 1280 px. Skriv ner tre saker som är fel eller trånga.

### Steg 3. Skriv mobile first

Se till att den grundläggande CSS:en (utan media query) ser bra ut på 360 px bredd: en kolumn, rimlig padding.

### Steg 4. Brytpunkt 1: 600 px

Lägg till `@media (min-width: 600px) { ... }`: mer `padding` i `main`, större hero-rubrik.

### Steg 5. Brytpunkt 2: 900 px

Lägg till `@media (min-width: 900px) { ... }`: Om oss i två kolumner, bredare sidhuvud.

### Steg 6. Bilder och formulär

Kontrollera att inga bilder sticker ut och att formulärfälten inte är för breda eller smala på någon storlek.

### Steg 7. Testa på riktigt

Öppna din sida på en riktig mobil (Live Server visar en nätverksadress, eller använd enhetsläget om du inte kan). Skriv vad du lade märke till.

## Kontrollista: så vet du att du är klar

- [ ] Viewport-metataggen finns i båda filerna.
- [ ] Sidan fungerar utan horisontell scroll på 360 px.
- [ ] Det finns minst två brytpunkter med `min-width` (mobile first).
- [ ] Layouten ändras på ett vettigt sätt mellan mobil, mellanläge och desktop.
- [ ] Du har testat i DevTools enhetsläge på minst tre bredder.
- [ ] Du har pushat till din fork och skickat in länken.

## Tips om du fastnar

- Horisontell scroll? Något element har fast bredd. Hitta det med DevTools: håll musen över elementen.
- Media query verkar inte gälla? Kolla klamrarna och att den ligger EFTER grundreglerna i filen.
- Brytpunkter ska bestämmas av när *innehållet* går sönder, inte av specifika enheter.

## Inlämning

**Deadline: imorgon klockan 09.00.** Allt lämnas in i Microsoft Forms. Du behöver inte redovisa något muntligt.

I formuläret fyller du i:

1. Länk till din fork av det här repot.
2. Reflektion: Vid vilken bredd gick din sida sönder först, och hur löste du det?

## Vill du mer? (frivilligt)

- Lägg till en tredje brytpunkt vid 1200 px för stora skärmar.
- Använd `clamp()` för att göra hero-rubriken flytande utan media query.
