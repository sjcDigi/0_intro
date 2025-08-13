# Opsætning af expo - React native Mobil apps

1. Start med at åbn din terminal. 

2. **Hvis du får adgangs problemer med at kører kommandoer i denne guide, skriv `sudo` før hvert kommando for at kører det som administrator**

3. Hvis du oplever fejl med kommandoer, læs først hvad terminalen siger og prøv selv at rette det, hvis det ikke lykkes, tilkald hjælp

## Homebrew
Tjek om det er installeret ved at skrive følgende: `brew -v`
Hvis terminalen svar med et versions nr. gå videre til "Homebrew installeret", hvis du får `zsh: command not found`, eller andet end en versions nr. gå videre til Installere Homebrew.

### Installere Homebrew
1. Gå til: [https://brew.sh/](https://brew.sh/)

2. Kopier install curl i din terminal

3. Tjek om det er installeret korrekte ved at skrive følgende: `brew -v`

### Homebrew Installeret
1. I terminalen, skriv `brew update && brew upgrade`

## Watchman
Expo krever en pakke kaldt Watchman for at kører, derfor skal vi installere den ved kopier følgende i terminalen:
```
brew install watchman
```
For at tjekke om installationen er fuldført korrekt, kør: `watchman --v `

## Node

1. Tjek om det er installeret ved at skrive følgende: `node -v`, Hvis den giver et version nummer som `18.17.1` eller højere så er du good to go.

2. Hvis du alligvel ønsker at opdatere til den nyeste version, læs videre på næste afsnit.

### Download Node

Følg den officiele hjemmeside for at sikre den bedste installation: https://nodejs.org/en

### Opdatere Node
1. Clear npm cache: `npm cache clean --force`

2. Installere n package med kommandoen: `npm install -g n``

3. For at opdatere Node til den sidste version, kør: `n latest``

4. Tjek nu: `node -v` & `npm -v`


## Expo
Før du går videre, tjek om nedenstående er opfyldt:

 - [ ] Watchman er installeret;
 - [ ] Node med version > 18.17.1.

1. Gå til: https://expo.dev/ og lave en konto ved at trykke på "Sign Up"

2. Download Expo Go på din mobil: https://expo.dev/go

3. Vi anbefaler at i laver en mappe "INNT_Exercises", hvor i kan gemme jeres opgaver.

### Start din første expo projekt!
1. Åbn Visual Studio Code (VS Code) eller Webstorm og åbn jeres mappe samt en terminal i VS Code

2. I terminalen kør: npx create-expo-app --template

3. Måske vil den promte jer om at skrive "y" eller "n" til version 3.0 - skriv "y" og godkende.

4. Choose a template: brug arrow-keys og vælg "Blank (Bare)"  template

5. Give dit app et navn, såsom "my_first_app"

6. Expo går i gang med at kreere din app, når den er færdig navigere ind til projektet via terminalen ved at kør: `cd my_first_app`

7. Når du er kommet ind til mappen, kør `npx expo start` for at initiere appen. Hvis du oplever problemer med denne step, kør først `npm install` og derefter `npx expo start --tunnel`

8. Scan QR koden på skærmen og værsgo!


