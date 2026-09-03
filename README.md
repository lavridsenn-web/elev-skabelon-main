# Elevskabelon – personlig portfolio og projektside

Denne skabelon er lavet som en enkel hjemmeside, hvor du kan præsentere dig selv og dokumentere de projekter og opgaver, du arbejder med.

Du behøver ikke kunne alt om HTML og CSS, før du går i gang. Formålet er netop, at du kan ændre lidt ad gangen, se hvad der sker og lære af det.

Skabelonen indeholder allerede de vigtigste byggeklodser:

- en top med navn og klasse
- en menu
- et område med **Om mig**
- projektblokke, som kan kopieres
- billeder med billedtekst
- kodeblokke
- links og knapper
- en tabel til test og resultater
- refleksion over dit arbejde
- en separat CSS-fil, der bestemmer udseendet

---

## 1. Mappens indhold

Når skabelonen er pakket ud, skal strukturen omtrent se sådan ud:

```text
elev-skabelon/
│
├── index.html
├── style.css
├── README.md
│
└── billeder/
    └── LAES_MIG.txt
```

### Hvad bruges filerne til?

**`index.html`**  
Her ligger selve indholdet på hjemmesiden: overskrifter, tekst, billeder, links, kode, projekter osv.

**`style.css`**  
Her bestemmes hjemmesidens udseende: farver, afstande, skrifttyper, knapper, bokse osv.

**`README.md`**  
Det er denne vejledning.

**`billeder/`**  
Her skal du lægge de billeder, du vil vise på hjemmesiden.

> Vigtigt: Flyt ikke `style.css` væk fra `index.html`, medmindre du også ændrer stien i HTML-filen.

---

# 2. Kom godt i gang

Arbejd i små trin. Gem filen og se resultatet efter hver ændring.

En god rækkefølge er:

1. Åbn hele projektmappen i VS Code.
2. Åbn `index.html`.
3. Ret dit navn og din klasse.
4. Gem filen.
5. Åbn siden i en browser og kontroller resultatet.
6. Ret teksten i **Om mig**.
7. Tilføj eller udskift et billede.
8. Ret den første projektblok.
9. Lav først derefter større ændringer.

Hvis noget pludselig ser forkert ud, er det meget lettere at finde fejlen, hvis du kun har ændret én eller to ting siden sidste test.

---

# 3. Sådan åbner du hjemmesiden

Du kan åbne `index.html` direkte i en browser.

Hvis du bruger en VS Code-udvidelse som Live Server eller Live Preview, kan du også bruge den. Fordelen er, at det bliver hurtigt at se dine ændringer undervejs.

Uanset metode gælder:

**Gem filen, før du forventer at se ændringen.**

I VS Code kan du normalt gemme med:

```text
Ctrl + S
```

På Mac er det normalt:

```text
Cmd + S
```

---

# 4. De vigtigste HTML-regler

HTML består af tags. Mange tags har en start og en slutning.

Eksempel:

```html
<p>Dette er et afsnit.</p>
```

Her er:

```html
<p>
```

starten på afsnittet, og:

```html
</p>
```

slutningen.

Et andet eksempel:

```html
<h2>Mit projekt</h2>
```

Hvis du ved en fejl sletter et `<`, et `>`, et citationstegn eller et afsluttende tag, kan browseren få svært ved at forstå resten af siden.

### En god regel

Når du ændrer almindelig tekst, så prøv først kun at ændre teksten **mellem tags**.

Fra:

```html
<h2>Skriv projektets titel</h2>
```

til:

```html
<h2>Automatisk plantevanding</h2>
```

Du behøver altså ikke ændre selve `<h2>` og `</h2>`.

---

# 5. Kommentarer i HTML-filen

Skabelonen indeholder mange kommentarer, der hjælper dig.

De ser sådan ud:

```html
<!-- Dette er en kommentar -->
```

Kommentarer vises ikke på hjemmesiden. De er kun en besked til den person, der arbejder med koden.

Du må gerne beholde kommentarerne. De gør det lettere at finde rundt i filen.

---

# 6. Ret navn, klasse og sidens titel

Øverst i `index.html` finder du blandt andet:

```html
<title>Min portfolio</title>
```

Teksten i `<title>` vises blandt andet i browserens fane.

Længere nede finder du toppen af selve siden:

```html
<header class="top">
    <h1>Min portfolio</h1>
    <p>Navn: Dit navn</p>
    <p>Klasse: Din klasse</p>
</header>
```

Ret for eksempel til:

```html
<header class="top">
    <h1>Min portfolio</h1>
    <p>Navn: Anna Jensen</p>
    <p>Klasse: 1.x</p>
</header>
```

---

# 7. Skriv din præsentation

Find området:

```html
<section class="blok" id="om-mig">
```

Her kan du rette teksten i `<p>...</p>`.

Eksempel:

```html
<p>
    Jeg hedder Anna og går på HTX. Jeg interesserer mig for programmering,
    teknologi og design. På denne side samler jeg mine projekter.
</p>
```

Du kan lave flere afsnit ved at tilføje endnu et `<p>...</p>`.

```html
<p>Dette er første afsnit.</p>
<p>Dette er andet afsnit.</p>
```

---

# 8. Sådan tilføjer du et billede

## Trin 1 – læg billedet i den rigtige mappe

Læg billedfilen i mappen:

```text
billeder
```

Et godt filnavn kan være:

```text
robot.jpg
```

eller:

```text
projekt1.png
```

### Brug helst enkle filnavne

Det er en god idé at bruge:

- små bogstaver
- tal
- bindestreg `-`
- underscore `_`

Eksempler:

```text
projekt-1.jpg
robot_arm.png
sensor2.jpg
```

Undgå helst mellemrum og specialtegn i filnavne.

Mindre godt:

```text
Mit flotte billede 1.JPG
```

Bedre:

```text
mit-flotte-billede-1.jpg
```

---

## Trin 2 – ret filnavnet i HTML

Skabelonen bruger for eksempel:

```html
<img src="billeder/mit-projekt.jpg" alt="Billede af mit projekt">
```

Hvis dit billede hedder `robot.jpg`, skal du skrive:

```html
<img src="billeder/robot.jpg" alt="Billede af min robot">
```

### `src` betyder billedets placering

```html
src="billeder/robot.jpg"
```

betyder:

> Find filen `robot.jpg` inde i mappen `billeder`.

### `alt` beskriver billedet

```html
alt="Billede af min robot"
```

`alt`-teksten er en kort beskrivelse af billedet. Den er blandt andet vigtig for tilgængelighed og vises også som hjælp, hvis billedet ikke kan indlæses.

---

# 9. Billedtekst

Et billede i skabelonen står inde i en `<figure>`:

```html
<figure>
    <img src="billeder/robot.jpg" alt="Billede af min robot">
    <figcaption>
        Figur 1: Robotten under den første test.
    </figcaption>
</figure>
```

Ret teksten mellem:

```html
<figcaption>
```

og:

```html
</figcaption>
```

så den passer til dit billede.

---

# 10. Profilbilledet er slået fra fra starten

I området **Om mig** er profilbilledet pakket ind i en HTML-kommentar.

Det ser omtrent sådan ud:

```html
<!--
<figure>
    <img src="billeder/profil.jpg" alt="Billede af mig">
    <figcaption>Et billede af mig.</figcaption>
</figure>
-->
```

Hvis du vil vise billedet, skal du fjerne:

```html
<!--
```

og:

```html
-->
```

så der kun står:

```html
<figure>
    <img src="billeder/profil.jpg" alt="Billede af mig">
    <figcaption>Et billede af mig.</figcaption>
</figure>
```

Husk også at lægge den rigtige billedfil i `billeder`-mappen.

---

# 11. Sådan retter du et link

Et link kan se sådan ud:

```html
<a href="https://example.com">Klik her</a>
```

Adressen står efter:

```text
href=
```

Teksten, som brugeren ser, står mellem `<a>` og `</a>`.

Eksempel:

```html
<a href="https://wokwi.com">Åbn Wokwi</a>
```

---

# 12. Link som knap

Skabelonen indeholder også links, der ser ud som knapper:

```html
<a class="knap"
   href="https://example.com"
   target="_blank"
   rel="noopener">
    Åbn mit projekt
</a>
```

Du behøver normalt kun at ændre to ting:

1. adressen i `href="..."`
2. teksten `Åbn mit projekt`

Eksempel:

```html
<a class="knap"
   href="https://wokwi.com/projects/123456"
   target="_blank"
   rel="noopener">
    Åbn mit Wokwi-projekt
</a>
```

`target="_blank"` betyder, at linket åbner i en ny fane.

---

# 13. Sådan indsætter du kode

Kode vises i denne type blok:

```html
<pre><code># Indsæt din kode her

for i in range(5):
    print("Hej verden")
</code></pre>
```

Skriv din kode mellem:

```html
<code>
```

og:

```html
</code>
```

`<pre>` gør blandt andet, at linjeskift og indrykninger bliver bevaret.

Det er særlig vigtigt i for eksempel Python, hvor indrykning er en del af koden.

---

## Hvis du vil vise HTML-kode som tekst

Her er en særlig situation:

Hvis du skriver almindelig HTML-kode direkte inde i en kodeblok, kan browseren tro, at den skal udføre koden i stedet for at vise den.

Hvis du for eksempel vil vise:

```html
<h1>Hej</h1>
```

som kode på din hjemmeside, skal `<` og `>` skrives som HTML-tegn:

```html
&lt;h1&gt;Hej&lt;/h1&gt;
```

De vigtigste er:

```text
<   bliver til   &lt;
>   bliver til   &gt;
&   bliver til   &amp;
```

Dette er normalt ikke nødvendigt for Python-kode.

---

# 14. Sådan laver du et nyt projekt

Det vigtigste område i skabelonen er projektblokken.

Den starter med:

```html
<section class="blok projekt">
```

og slutter med:

```html
</section>
```

For at lave et nyt projekt skal du kopiere **hele projektblokken**.

## Fremgangsmåde

1. Find starten:

```html
<section class="blok projekt">
```

2. Find det `</section>`, der afslutter netop denne projektblok.
3. Markér hele området.
4. Kopiér det.
5. Indsæt kopien nedenunder.
6. Ret titel, tekst, billede, kode, links og testresultater i kopien.

### Pas på

En almindelig fejl er kun at kopiere en del af projektblokken.

Hvis den næste projektblok pludselig ligger inde i den forrige, eller sidens bokse ser mærkelige ud, mangler der ofte et afsluttende:

```html
</section>
```

---

# 15. Projektets titel

Ret:

```html
<h2>Projekt 1: Skriv projektets titel</h2>
```

for eksempel til:

```html
<h2>Projekt 2: Afstandsmåler</h2>
```

Du bestemmer selv, om du vil nummerere projekterne.

---

# 16. Dokumentér dit arbejde

En projektside bliver mere nyttig, hvis den ikke kun viser slutresultatet.

Du kan for eksempel beskrive:

- Hvad var opgaven?
- Hvad ville du forsøge at bygge eller programmere?
- Hvilke valg traf du?
- Hvad testede du?
- Hvilke fejl opstod?
- Hvordan fandt du fejlen?
- Hvad ændrede du?
- Hvad virker nu?
- Hvad ville du forbedre næste gang?

Det er helt i orden at dokumentere noget, der ikke virkede første gang. Det viser arbejdsprocessen.

---

# 17. Testtabellen

Skabelonen indeholder en simpel tabel:

```html
<tr>
    <td>Hvad tester jeg?</td>
    <td>Hvad forventer jeg?</td>
    <td>Hvad skete der?</td>
</tr>
```

Hvis du skal have flere tests, kan du kopiere hele `<tr>...</tr>`-blokken.

Eksempel:

```html
<tr>
    <td>LED tænder</td>
    <td>LED lyser, når knappen trykkes</td>
    <td>Virker</td>
</tr>

<tr>
    <td>LED slukker</td>
    <td>LED slukker, når knappen slippes</td>
    <td>Virker efter rettelse</td>
</tr>
```

---

# 18. Menuen og `id`

Menuen øverst på siden indeholder links som:

```html
<a href="#om-mig">Om mig</a>
```

Dette link leder til et element, der har:

```html
id="om-mig"
```

For eksempel:

```html
<section class="blok" id="om-mig">
```

Hvis du ændrer `id`, skal menuens `href` ændres tilsvarende.

Eksempel:

```html
<a href="#mine-projekter">Projekter</a>
```

skal passe sammen med:

```html
<section id="mine-projekter">
```

---

# 19. Hvad må du ændre i `style.css`?

`style.css` bestemmer udseendet.

Du behøver ikke ændre CSS for at bruge skabelonen, men du må gerne eksperimentere.

Arbejd gerne med én ting ad gangen.

## Eksempel: sidens baggrund

Find:

```css
body {
    background: #f3f5f7;
}
```

Prøv at ændre farven og se resultatet.

## Eksempel: toppen

Find:

```css
.top {
    background: #243447;
    color: white;
}
```

`background` styrer baggrundsfarven.

`color` styrer tekstfarven.

## Eksempel: knapper

Find:

```css
.knap {
    background: #245d91;
    color: white;
}
```

Her kan du ændre knappens farver.

---

# 20. En sikker måde at eksperimentere med CSS

Når du vil prøve noget nyt:

1. Gem den version, der virker.
2. Ændr én CSS-værdi.
3. Gem.
4. Se siden i browseren.
5. Behold ændringen, hvis den er god.
6. Brug `Ctrl + Z` / `Cmd + Z`, hvis resultatet ikke blev som ønsket.

Lav ikke ti ændringer på én gang, hvis du stadig er usikker på CSS. Så bliver det svært at vide, hvilken ændring der gav problemet.

---

# 21. Git og GitHub – forskellen på at gemme og udgive

Hvis projektet er koblet til GitHub, er der flere trin:

```text
ændr fil → gem → commit → push → GitHub Pages
```

At trykke `Ctrl + S` gemmer kun ændringen på din egen computer.

Den kommer først op på GitHub, når ændringen er committed og pushed.

---

# 22. Et enkelt Git-workflow

Hvis din mappe allerede er koblet til et repository, kan du kontrollere status i terminalen:

```bash
git status
```

Tilføj ændrede filer:

```bash
git add .
```

Lav et commit:

```bash
git commit -m "Opdateret portfolio"
```

Send ændringen til GitHub:

```bash
git push
```

Du kan også bruge **Source Control** i VS Code, hvis det er den arbejdsgang, I bruger på holdet.

Skriv gerne korte og konkrete commit-beskeder, for eksempel:

```text
Tilføjet projekt 2
Rettet billede
Opdateret refleksion
Rettet link til Wokwi
```

---

# 23. GitHub Pages

Hvis repository'et skal vises som en hjemmeside via GitHub Pages, kan GitHub Pages konfigureres til at udgive fra en branch.

Til en helt enkel HTML/CSS-side bruges typisk repository'ets hovedbranch og rodmappen.

På GitHub findes indstillingen under:

```text
Repository → Settings → Pages
```

Under **Build and deployment** kan kilden sættes til:

```text
Deploy from a branch
```

og derefter for eksempel:

```text
Branch: main
Folder: / (root)
```

Når ændringer pushes til den valgte kilde, kan GitHub Pages udgive den opdaterede side.

---

# 24. Før du går i panik: en hurtig fejlsøgningsmetode

Når noget ikke virker, så prøv denne rækkefølge:

1. **Gem filen.**
2. **Genindlæs browseren.**
3. Kig på den sidste ændring, du lavede.
4. Brug `Ctrl + Z` / `Cmd + Z`, hvis fejlen kom efter den ændring.
5. Kontroller filnavne og stier.
6. Kontroller citationstegn `"..."`.
7. Kontroller start- og sluttags.
8. Se efter røde eller gule markeringer i VS Code.
9. Sammenlign med en blok i skabelonen, der stadig virker.
10. Hvis siden virker lokalt, men ikke på GitHub, kontroller commit, push og GitHub Pages.

Det er ofte hurtigere at finde den **seneste lille fejl** end at omskrive hele siden.

---

# 25. Troubleshooting – billedet vises ikke

Dette er en af de mest almindelige fejl.

Kontroller følgende:

### A. Ligger billedet faktisk i mappen `billeder`?

Hvis HTML siger:

```html
src="billeder/robot.jpg"
```

skal strukturen være:

```text
index.html
billeder/
    robot.jpg
```

### B. Er filnavnet stavet præcis ens?

Disse kan blive opfattet som forskellige filnavne:

```text
Robot.jpg
robot.jpg
ROBOT.JPG
```

Dette er især vigtigt, når siden ligger på GitHub Pages.

### C. Er filtypen rigtig?

Hvis filen hedder:

```text
robot.png
```

må HTML ikke sige:

```html
robot.jpg
```

### D. Er der en tastefejl i stien?

Forkert:

```html
src="billederrobot.jpg"
```

Rigtigt:

```html
src="billeder/robot.jpg"
```

### E. Er billedfilen blevet pushed til GitHub?

Et billede kan godt virke lokalt på din computer, selv om du har glemt at committe og pushe selve billedfilen.

Kør eventuelt:

```bash
git status
```

og se, om billedfilen stadig står som ny eller ændret.

---

# 26. Troubleshooting – CSS virker ikke

Hvis siden pludselig ser helt uden design ud, er HTML-filen muligvis ikke forbundet med `style.css`.

I `<head>` skal der stå:

```html
<link rel="stylesheet" href="style.css">
```

Kontroller også, at filerne ligger sådan:

```text
index.html
style.css
```

Hvis du for eksempel har flyttet CSS-filen ind i en mappe med navnet `css`, skal stien også ændres:

```html
<link rel="stylesheet" href="css/style.css">
```

---

# 27. Troubleshooting – jeg ændrer CSS, men intet sker

Prøv:

1. Gem `style.css`.
2. Genindlæs browseren.
3. Kontroller, at du har ændret den CSS-regel, der faktisk bruges.
4. Kontroller, at du ikke mangler `{`, `}` eller `;`.
5. Kontroller, at `style.css` stadig er linket korrekt fra `index.html`.

Eksempel på korrekt CSS:

```css
.top {
    background: #243447;
    color: white;
}
```

Hvis en `}` mangler, kan efterfølgende CSS-regler blive påvirket.

---

# 28. Troubleshooting – hele siden ser mærkelig ud efter en HTML-ændring

Det skyldes ofte et manglende eller forkert tag.

Kontroller især:

```html
</p>
</section>
</div>
</a>
```

og citationstegn i attributter:

```html
href="..."
src="..."
class="..."
id="..."
```

Eksempel på en fejl:

```html
<img src="billeder/robot.jpg alt="Min robot">
```

Her mangler et citationstegn efter `.jpg`.

Korrekt:

```html
<img src="billeder/robot.jpg" alt="Min robot">
```

---

# 29. Troubleshooting – mit nye projekt ligger inde i det gamle

Du har sandsynligvis ikke kopieret hele projektblokken, eller et `</section>` mangler.

En projektblok skal have denne grundform:

```html
<section class="blok projekt">

    ... projektets indhold ...

</section>
```

Kontroller, at hver projektblok både har en start og en afslutning.

VS Code hjælper ofte ved at vise indrykninger og matchende tags.

---

# 30. Troubleshooting – menuen hopper ikke til det rigtige sted

Et menulink som:

```html
<a href="#refleksion">Refleksion</a>
```

skal passe til et element med:

```html
id="refleksion"
```

Hvis du skriver:

```html
href="#reflektion"
```

men området hedder:

```html
id="refleksion"
```

matcher de ikke.

---

# 31. Troubleshooting – linket virker ikke

Kontroller først adressen.

Et internetlink bør typisk begynde med:

```text
https://
```

Eksempel:

```html
<a href="https://example.com">Åbn siden</a>
```

Kontroller også, at citationstegnene er på plads.

Forkert:

```html
<a href=https://example.com">Åbn siden</a>
```

Rigtigt:

```html
<a href="https://example.com">Åbn siden</a>
```

---

# 32. Troubleshooting – min kodeblok ser forkert ud

Kontroller, at du stadig har både:

```html
<pre><code>
```

og:

```html
</code></pre>
```

Hvis du viser HTML-kode inde i kodeblokken, så husk at erstatte `<` og `>` med `&lt;` og `&gt;`.

---

# 33. Troubleshooting – det virker lokalt, men ikke på GitHub Pages

Hvis hjemmesiden virker på din computer, men GitHub Pages viser en gammel version eller mangler noget, så kontroller:

1. Er filen gemt?
2. Er ændringen committed?
3. Er committet pushed til GitHub?
4. Kan du se den nye fil eller ændring direkte i repository'et på github.com?
5. Er GitHub Pages sat til den branch og mappe, hvor `index.html` ligger?
6. Hedder startsiden præcis `index.html`?
7. Er billeders filnavne og store/små bogstaver korrekte?

På GitHub kan Pages-indstillingerne kontrolleres under:

```text
Settings → Pages
```

Hvis Pages udgiver fra en branch, skal den valgte branch og mappe passe til, hvor dine filer ligger.

---

# 34. Troubleshooting – Git siger, at der ikke er noget at committe

Hvis du ser noget i retning af:

```text
nothing to commit, working tree clean
```

betyder det normalt, at Git ikke kan se nye gemte ændringer.

Kontroller:

- Har du gemt filen?
- Arbejder du i den rigtige projektmappe?
- Har du allerede committed ændringen?

Prøv:

```bash
git status
```

---

# 35. Troubleshooting – `git push` bliver afvist

Læs fejlbeskeden i terminalen. Den er vigtig.

En almindelig situation er, at repository'et på GitHub indeholder ændringer, som din lokale kopi ikke har endnu.

Hvis I arbejder flere på samme repository, eller hvis filer er blevet ændret direkte på GitHub, kan det være nødvendigt først at hente ændringerne.

Brug ikke tilfældige Git-kommandoer fra nettet for at “tvinge” et push igennem, hvis du ikke ved, hvad de gør. Vis i stedet fejlbeskeden til din lærer eller undersøg, hvorfor din lokale og din eksterne version er forskellige.

En god første kommando er stadig:

```bash
git status
```

---

# 36. Troubleshooting – jeg kom til at ødelægge noget

Det sker.

Prøv først:

```text
Ctrl + Z
```

eller på Mac:

```text
Cmd + Z
```

Hvis du bruger Git og tidligere har lavet commits, har du desuden en historik over versioner, der tidligere virkede.

Det er en af grundene til, at det er en god idé at committe, når du når et punkt, hvor siden virker.

Eksempel på en god arbejdsgang:

```text
1. Få billedet til at virke
2. Test siden
3. Commit: "Tilføjet billede til projekt 1"
4. Fortsæt med næste ændring
```

---

# 37. Brug browserens udviklerværktøjer

Når du bliver mere sikker, kan browserens Developer Tools være meget nyttige.

I mange browsere kan de åbnes med:

```text
F12
```

Her kan du blandt andet undersøge:

- hvilken HTML browseren ser
- hvilke CSS-regler der bruges
- fejl i konsollen
- om en fil ikke kunne hentes

Du behøver ikke forstå alt, hvad der står. Kig efter fejl og filnavne, du genkender.

Eksempel:

Hvis browseren skriver, at den ikke kan finde:

```text
billeder/robot.jpg
```

ved du, at problemet sandsynligvis handler om billedets navn eller placering.

---

# 38. En god måde at lære på

Når du vil prøve noget, kan du bruge denne metode:

### 1. Lav en lille ændring

For eksempel:

```html
<h2>Mit første robotprojekt</h2>
```

### 2. Gem

### 3. Se resultatet

### 4. Stil dig selv spørgsmålet

> Hvad ændrede min kode på siden?

### 5. Prøv derefter én ting mere

På den måde lærer du sammenhængen mellem kode og resultat.

---

# 39. Forslag til ting du selv kan eksperimentere med

Når grundsiden virker, kan du for eksempel undersøge, hvordan du:

- ændrer farver
- ændrer skrifttype
- gør overskrifter større eller mindre
- laver flere knapper
- laver flere projektblokke
- sætter flere billeder ind
- laver et link til GitHub
- laver et link til Wokwi
- tilføjer en video med HTML
- laver to billeder ved siden af hinanden
- giver hvert projekt sin egen farve
- laver en ekstra underside
- ændrer menuen
- tilføjer en liste

Prøv én forbedring ad gangen og test undervejs.

---

# 40. Små HTML-byggeklodser

## Overskrift

```html
<h2>Min overskrift</h2>
```

## Mindre overskrift

```html
<h3>Min mindre overskrift</h3>
```

## Afsnit

```html
<p>Min tekst.</p>
```

## Fed tekst

```html
<strong>Vigtig tekst</strong>
```

## Punktopstilling

```html
<ul>
    <li>Første punkt</li>
    <li>Andet punkt</li>
    <li>Tredje punkt</li>
</ul>
```

## Nummereret liste

```html
<ol>
    <li>Første trin</li>
    <li>Andet trin</li>
    <li>Tredje trin</li>
</ol>
```

## Link

```html
<a href="https://example.com">Mit link</a>
```

## Billede

```html
<img src="billeder/robot.jpg" alt="Min robot">
```

---

# 41. Før du afleverer eller viser siden

Brug denne tjekliste:

- [ ] Mit navn og min klasse er rettet.
- [ ] Teksten i **Om mig** er min egen.
- [ ] Mine projekter har tydelige titler.
- [ ] Mine billeder vises.
- [ ] Billederne har relevante `alt`-tekster.
- [ ] Mine links virker.
- [ ] Min kode kan læses.
- [ ] Jeg har beskrevet mindst noget af min arbejdsproces.
- [ ] Mine testresultater er opdateret.
- [ ] Jeg har skrevet en refleksion.
- [ ] Siden ser rimelig ud på både stor og lille skærm.
- [ ] Alle ændringer er gemt.
- [ ] Hvis jeg bruger GitHub: ændringerne er committed og pushed.
- [ ] Hvis jeg bruger GitHub Pages: den publicerede side viser den rigtige version.

---

# 42. Når du beder om hjælp

Det er lettere at få god hjælp, hvis du kan forklare præcist, hvad problemet er.

I stedet for kun at sige:

> Det virker ikke.

kan du for eksempel sige:

> Mit billede vises lokalt, men ikke på GitHub Pages. Filen hedder `Robot.JPG`, og min HTML siger `billeder/robot.jpg`.

eller:

> Efter jeg kopierede en projektblok, ligger projekt 2 inde i projekt 1. Jeg tror, jeg mangler et `</section>`.

eller:

> Jeg har gemt min ændring, men den kan ikke ses på GitHub. `git status` viser en ændret `index.html`.

Jo mere præcist du beskriver situationen, jo lettere er den at undersøge.

---

# 43. Husk de tre vigtigste ting

Hvis du kun husker tre ting fra denne vejledning, så brug disse:

### 1. Ændr lidt ad gangen

Så er fejl lettere at finde.

### 2. Filnavne og stier skal passe præcist

Især ved billeder og GitHub Pages.

### 3. Gem er ikke det samme som push

Hvis siden ligger på GitHub, skal ændringen også ende på GitHub, før den kan udgives derfra.

---

## Kort reference

```text
HTML      = indhold og struktur
CSS       = udseende
index.html = hjemmesidens startside
style.css  = design og layout
billeder/   = dine billeder
commit      = gem et punkt i Git-historikken
push        = send commits til GitHub
GitHub Pages = vis repository'ets hjemmeside på nettet
```

God arbejdslyst – og brug gerne skabelonen som et sted, hvor du både dokumenterer dit arbejde og eksperimenterer med HTML og CSS.
