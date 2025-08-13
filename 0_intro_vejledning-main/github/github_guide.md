# Git & GitHub Guide: Brug af Terminalen └[∵┌]└[ ∵ ]┘[┐∵]┘


Denne guide hjælper dig med at komme i gang med Git og GitHub direkte fra din terminal. Du lærer, hvordan du initialiserer et Git-repository, laver commits, og uploader dit projekt til GitHub.

## Forudsætninger

Før du starter, skal du have følgende på plads:

- Git skal være installeret på din computer. [Download Git her](https://git-scm.com/downloads)
- Du skal have en GitHub-konto. [Opret en konto her](https://github.com/)

## Github Desktop App'en

Hvis du ikke er komfortable med brugen af kommandoer og arbejde i terminal, så kan github appen være et godt alternativ. Du kan download den her: [Download Github Desktop her](https://github.com/apps/desktop)

Hvis du heller vil prøve kræfter med github kommandoer (som typisk bruges meget mere i virksomheder) så er der her en guide. 

<br></br>

# Github Push, Pull og Merge ¯\_(シ)_/¯

## 1 - Opret en GitHub Repository

1. Gå til [GitHub](https://github.com) og log ind.
2. Klik på "New" for at oprette et nyt repository.
3. Giv dit repository et navn, og vælg om det skal være "Public" eller "Private".
4. Klik på "Create repository".


## 2 - Opsæt Git Lokalt

1. Åbn terminalen på din computer.
2. Konfigurer dit Git-brugernavn og e-mail:

   ```
   git config --global user.name "DitNavn"
   git config --global user.email "dinemail@example.com"
   ```



## 3 - Opret Git Repository

1. Naviger til den mappe, hvor dit projekt ligger, eller opret en ny mappe:
    ```
    cd path/to/your/project
    ```

2. Initialiser et nyt Git repository:
    ```
    git init
    ```


## 4 - Tilføj filer til Git

1. Tilføj de filer, du ønsker at spore:
    ```
    git add .
    ```

   `.` betyder "alle filer". Hvis du kun vil tilføje en specifik fil, brug filnavnet:
    ```
    git add filnavn.txt
    ```


## 5 - Lav en Commit

1. Lav en commit med en valgfri besked:
    ```
    git commit -m "Initial commit"
    ```


## 6 - Opret forbindelse til GitHub

1. Gå til [GitHub](https://github.com) og opret et nyt repository. Kopier URL'en til dit GitHub repository.

2. Tilføj GitHub som remote repository:
    ```
    git remote add origin https://github.com/dit-brugernavn/din-repo.git
    ```

3. Bekræft at remote blev tilføjet:
    ```
    git remote -v
    ```


## 7 - Push projektet til GitHub

1. Push dine ændringer til GitHub:
    ```
    git push -u origin main
    ```

    Hvis din hovedgren hedder "master", skal du bruge:
    ```
    git push -u origin master
    ```

   Du kan typisk også bare bruge:
   ```
    git push
   ``` 

## 8 - Pull ændringer fra GitHub

1. Hvis der er ændringer i dit GitHub repository, som du vil hente lokalt:
    ```
    git pull origin main
    ```

    eller bare
    ```
    git pull 
    ```


## 9 - Tilføj `.gitignore`-fil

1. Opret en `.gitignore`-fil i roden af dit projekt og tilføj filer eller mapper, du vil ignorere. Eksempel på indhold:
    ```
    node_modules/
    .DS_Store
    .env
    ```

Disse er typisk filer du ikke behøver gemme i dit online repo da de installeres eller konfigueres lokalt ved npm install

<br></br>

# Gode tips til når i arbejder med jeres repo (især til gruppe arbejde) (-.-(-.(-(-.(-.-).-)-).-)-.-)

## 1 - Opret nye Branches (Valgfrit men anbefalet!)

Branches hjælper jer holde styr på forskellige versioner af jeres produkt. Ved at arbejde på en branch, sikre du dig at din master branch altid er den seneste stable version af jeres produkt. Kommer i til at lave ændringer der ødelægger jeres app, så har i altid en backup i kan komme tilbage til.

1. Opret en ny branch:
    ```
    git checkout -b ny-branch-navn
    ```

2. Skift mellem branches:
    ```
    git checkout main
    ```

## Merge Branches

1. Skift til hovedbranchen:
    ```
    git checkout main
    ```

2. Merge ændringerne:
    ```
    git merge ny-branch-navn
    ```


## 2 - Brug af Git Stash

Hvis du arbejder på noget, men ikke er klar til at committe, kan du midlertidigt gemme dine ændringer med `git stash`:

1. Stash dine ændringer:
    ```
    git stash
    ```

2. Se alle dine stashes:
    ```
    git stash list
    ```

3. Gendan de ændringer, du har stashet:
    ```
    git stash apply
    ```

4. Hvis du vil slette den seneste stash efter anvendelse:
    ```
    git stash drop
    ```

5. Hvis du vil gendanne og fjerne stashen på samme tid:
    ```
    git stash pop
    ```


## 3 - Se status på dit repository

Du kan altid tjekke status på dit repository for at se hvilke filer, der er ændret, eller hvilke der skal committes:
    ```
    git status
    ```


## 4 - Se commit historik

For at se historikken for commits i dit repository, brug:
    ```
    git log
    ```


## 5 - Fejlretning og TIlbagetrækning (╯°□°)╯︵ ɢɪᴛ --ʀᴇꜱᴇᴛ --ʜᴀʀᴅ ⎯┻━┻

1. Hvis du vil tilbagetrække en fil, som du allerede har tilføjet til staging-området:
    ```
    git reset filnavn.txt
    ```

2. Hvis du vil tilbagetrække den sidste commit (uden at miste ændringerne):
    ```
    git reset --soft HEAD^
    ```

3. Hvis du vil tilbagetrække den sidste commit og også slette ændringerne:
    ```
    git reset --hard HEAD^
    ```
