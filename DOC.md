# Projet Next JS Table

## Intro

## Créer NextApp

version 13.1.1 avec typescript sans EsLint

npm run dev pour lancer l'application sur le localhost:3000

App>page.tsx est le composant react qui contient la page d'acceuil

## Ajout de TailWind

cf [DOC](https://tailwindcss.com/docs/installation)

npm install -D tailwindcss@3.2.4 postcss@8.4.20 autoprefixer@10.4.13

npx tailwindcss init -p qui initialise tailwind et ajoute 2 fichier :

- postcss.config.js
- tailwind.config.js
  - on ajoute le path des composant et on définis les extenssions js, tsx, etc ... pour que les composant accept tailwindcss

on ajoute les directive au composant app>globals.css

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

puis j'ajoute une className pour verifier que ça fonctionne dans page.tsx

on modifie les size dans taillwind.config.js

## File Base Routing

On importe les template html dans le dossier html

On associe les route a un template html :

- opentable.ca = homePage.html
- opentable.ca/search = searchPage.html
- opentable.ca/reastaurant/shakeshack = restaurantDetailsPage.html
- opentable.ca/reastaurant/shakeshack/menu = restaurantMenuPage.html
- opentable.ca/reserve/shakeshack = reservationPage.html

Pour les nom des restaurant on les pace dans un dossier nommé [slug]

puis on implemente les route avec le fichier html associé avec le **File Based Routing**

## Navigation across pages

On a importer les different template html et maitenant nous allons créer un systeme de naviguation

La documentation nous dis qu'il y a 2 façon de faire.

- link components
- useRouter Hook

sur notre menu/page.tsx on importe Link
puis on change les <a> en <Link>