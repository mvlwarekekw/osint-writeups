## Mine d'or
```js
Points: 100
Solves: 15
```

<br>

*🇫🇷 – Cet enquêteur semble être un véritable allié ! Comme vous avez pu le constater, il est parvenu à extraire des fichiers sensibles concernant APT-509. Nos experts ont réussi à identifier un compte qu’il utilise en ligne, et voici la description qu’il y a laissée :*

*If you're here, it's because you too want to put an end to the 509 menace. GL! I've deliberately left some information about a key character in the group (#A) on the internet. You'll find it useful !*

*Pouvez-vous retrouver ces données et, grâce à elles, potentiellement identifier un autre site-web utilisé par APT-509 ?*

*🇬🇧 – This investigator appears to be a true ally! As you may have noticed, they managed to extract sensitive files related to APT-509. Our experts were able to identify an account they use online, and here is the description they left :*

*If you're here, it's because you too want to put an end to the 509 menace. GL! I've deliberately left some information about a key character in the group (#A) on the internet. You'll find it useful !*

*Can you locate this data and, using it, potentially identify a other website used by APT-509 ?*

<br>

In the last challenge we found the user of an ally, 3ND0FW47CH509. Using the first part of the user 3ND0FW47CH, we can find a pastebin account.
The pastebin account links to a paste, which reveals a Base64-encoded string: "bzI0cHN3d2Jwanp5NmhjMzZtZmJ4cHk2eHFheXk3Y3RhNHc1eGZvb3J0d3ZlaGIyNzJlZWVmeWQ=".
Decoding this reveals a partial onion URL: o24pswwbpjzy6hc36mfbxpy6xqayy7cta4w5xfoortwvehb272eeefyd

Flag: ``o24pswwbpjzy6hc36mfbxpy6xqayy7cta4w5xfoortwvehb272eeefyd.onion``