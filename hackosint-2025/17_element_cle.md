## L'élément clé
```js
Points: 100
Solves: 38
```

<br>

*🇫🇷 – En analysant les différentes informations dont vous disposez sur Bravo, une conversation mentionnant une application paraît particulièrement intéressante.*
*Quel est l'identifiant (ID) de cette application mentionnée ?*

*🇬🇧 – By analyzing the various pieces of information you have about Bravo, a conversation mentioning an application seems particularly interesting.*
*What is the ID of this mentioned application ?*

> *Flag format : tarte.aux.pommes*

<br>

In one of the previous challenges we find Lise's website: https://mymemoriegram.xyz/ where she posts a lot of stuff. Useless stuff. What we actually need is the content of the `robots.txt` file, which is usually meant for scrapers, today its also meant for us.
We can see an endpoint called `/private` which we can only access with the user agent `bravo`. You can use whichever tool you like to change your user agent, e.g. a chrome extension or burp suite. In the `/private` we find a lot of screenshots.

In one of the conversations they were talking about a fishing app. They also sent a logo of the supposed application. Using the name and logo we can try various combinations on different app stores. Finally we find the app "FishingApp", with the ID `com.hackosint.myapplication`.

[Link to Playstore](https://play.google.com/store/apps/details?id=com.hackosint.myapplication&hl=de_CH)

Flag: `com.hackosint.myapplication`