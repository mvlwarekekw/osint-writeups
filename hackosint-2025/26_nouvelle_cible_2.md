## Nouvelle Cible 2
```js
Points: 100
Solves: 34
```

<br>

*🇫🇷 - Après l’arrestation d'une partie de leurs membres en 2024, les activités du groupe APT 509 sont en net déclin. Leur attaque prévue cette même année contre la ville de Geelong, en Australie, a échoué. Par conséquent, leur trésorerie a été directement impactée. Pour tenter de se relancer, le groupe envisage désormais une cyberattaque contre un établissement français.*
*Pouvez-vous identifier quelle entreprise est visée par APT 509 ?*

*🇬🇧 - Following the arrest of several of its members in 2024, the activities of the APT 509 group have significantly declined. Their planned attack that same year on the city of Geelong, Australia, failed. As a result, their financial resources have been directly affected. In an attempt to recover, the group is now planning a cyberattack against a French organization.*
*Can you identify which company is being targeted by APT 509? (company name)*

> Flag format : Société nationale des chemins de fer français

<br>

In a previous challenge we found the telegram channel, APT509TMP. There's a drive link to another CryptPad, this time protected by a password. In one of the conversations between November and Bravo, they mentioned a password: `kmMBRAS9J&$jonnF`

There's one folder that stands out: Target. It contains a drawing of a town which has a train station on the left and a red arrow pointing at their target.
Checking multiple cities in eastern France (title) we finally find the the town: Riems, which matches all criteria. Using some attributes from the drawing, we can find that their next target is the CIC, also known as the Crédit Industriel et Commercial. 

Flag: ``Crédit Industriel et Commercial``
