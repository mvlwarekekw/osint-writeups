## L'allié
```js
Points: 50
Solves: 18
```

<br>

*🇫🇷 – En explorant ce site de location de bateaux, il semble qu’un enquêteur allié mène également des recherches sur le groupe APT-509. Il aurait réussi à infiltrer le système de dashboarding caché de l’organisation et à en extraire des fichiers sensibles. Il aurait volontairement laissé une trace, destinée à ceux qui souhaitent l’aider à faire tomber la menace que représente le groupe 509.*
*En enquêtant à votre tour sur ce site, pouvez-vous identifier le pseudonyme utilisé par cet enquêteur ?*

*🇬🇧 – While exploring this boat rental website, it appears that an allied investigator is also conducting research on the APT-509 group. He is believed to have successfully infiltrated the organization's hidden dashboard system and extracted sensitive files. He may have deliberately left a trace, intended for those willing to help bring down the threat posed by Group 509.*
*As you investigate the site in turn, can you identify the pseudonym used by this investigator ?*

<br>

Checking the web archive of `loueuneencre.online` we find a hidden URL: https://loueuneencre.online/CMNoCxqsn321.php with an extremely scary and completely real login panel.

Cross referencing the site on the web archive we can find the hidden paragraph tag with the login data. 
`Admin:Captain@Brise2025!VoileBleue`

We get an extremely real admin panel with loads of dangerous commands. Running the `alert` command we can access the logs where we find the user.

Flag: `3ND0FW47CH509`
