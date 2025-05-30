****## TocTocToc
```js
Points: 100
Solves: 15
```

<br>



<br>

(sadly only solved this after the CTF)

TocTocToc was arguably the hardest challenge in the whole CTF with only 15 teams solving it, 9 out of them solving the whole CTF. 

We got some information from reading through all the chats:
- There's a Lycee privée Saint-Joseph in the town
- He lives in district 01, which is Ain
- The house is under construction in 2023, which can be seen on streetview
- The road was closed in Feb 2024

Using that information in order we find 4 possible places, which I checked with the streetview requirement:

- Miribel
- Saint Dider sur Chalaronne (streetveiw only in 2022/2024),
- Bourg-en-Bresse (most recent streetview I found was 2022),

Going forward with the only possiblity, which is Miribel. My first idea was to just try and bruteforce my way through every street in Miribel to find houses under construction, which turned out to be a herculean task and was straight up impossible with there being too many options. 

Usually towns give their citizens information on about road works beforehand, so using the web archive on their town website, I found a post regarding some road works around Rue de la Pellera.

Entering streetview there was one building on that street which matches all criteria.

Flag: `45.8325025412702, 4.948845285320925`