## L'oublié(e)
```js
Points: 50
Solves: 14
```

<br>

*🇫🇷 – Les informations révélées sur ce nouveau site suggèrent qu’un individu menait un double jeu... Pouvez-vous identifier son nom de code ainsi que son rôle au sein d’APT-509 ?*

*🇬🇧 – The information uncovered on this new site suggests that someone was playing a double game... Can you identify their code name and their role within APT-509 ?*

> Flag format : Delta administrateur système

<br>

Starting on the onion site from challenge #23 we get a screen that blocks us from viewing the web page. In the source code this is a simple \<div> tag, which we can remove.

On one of the posts about the phishing attack on Charlotte, we find Kilo, who tells us that she pretended to help him, which refers to V1 of Hack'OSINT and the help on the Commentçamarche forum.

Checking the archive.ph of said website reveals, the arrival of the new member Kilo, aka. Ainoa Fernandez.

Flag: `Kilo chargée d’intelligence sociale`