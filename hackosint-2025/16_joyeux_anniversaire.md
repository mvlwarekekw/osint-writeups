## Joyeux Anniversaire
```js
Points: 75
Solves: 35
```

<br>

*🇫🇷 – Pour compléter notre dossier d'enquête, pourriez-vous nous fournir la date de naissance complète de Bravo ainsi que son département de naissance ? Grâce à ces informations, nous pourrions vérifier dans nos archives si elle est déjà impliquée dans d’autres affaires de cybercriminalité.*

*🇬🇧 – To complete our investigation file, could you please provide us with Bravo's full date of birth as well as her department of birth ? With this information, we could check our records to see if she has been involved in any other cybercrime cases.*

> *Flag format : JJ/MM/AAAA Yonne*

<br>

Using the linktree from the previous challenge we can find the link to her personal website, as well as the birthday from the Google calendar. Scrolling down a bit we  find a picture of what seems to be her.

Decoding the bar code on her left forearm we get the number `293088400300522`. This has the format of a card all french citizens have.
<br><br> The first digit is the gender: 1 is male, 2 is female
<br> The second and third digits are the year of birth, so 93 means 1993
<br> The fourth and fifth digits are the month of birth, so 08 means August
<br> The sixth and seventh digits are the department of birth, so 84 means Vaucluse
<br> The following three digits are the number of the commune of birth, irrelevant for us though
<br> The last three digits are a serial number, also irrelevant for us
<br> The last digit is a checksum, which we can ignore for our purposes

Flag: `14/08/1993 Vaucluse`