# Setup Monorepo

Ett **monorepo** är ett git-repository som innehåller flera applikationer. Här är ett exempel på hur man kan sätta upp en react-app och en express-app i samma git repo:

1. Börja i en katalog du skapat med appens namn
2. Kör kommando för att skapa Create React App - vi kallar den för *client*

```sh
npx create-react-app client --template typescript
```

3. React-appen är från början ett eget git-repository vilket vi inte vill (den är ju bara en del i ett annat repo). Ta därför bort git från react-appen:

```sh
cd client
rm -rf .git
```

4. Gå nu ner till ursprungsmappen, skapa en mapp för express-appen - vi kallar den för server:

```sh
cd ..
mkdir server
cd server
touch .gitignore
echo "node_modules/" >> .gitignore
cd ..
```

5. Vi kan nu också initiera vårt git-repo (i rot-mappen)

```sh
git init
```

6. Lägg sedan till filer i server-mappen som krävs för att få till en express-app
