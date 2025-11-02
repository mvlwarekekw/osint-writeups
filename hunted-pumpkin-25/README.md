<div style="display:flex; flex-direction: column; align-items: center;">
<h1> Haunted Pumpkin CTF '25 </h1>
<h3> Fun CTF organized by OSINT Switzerland </h3>

![pumpkin.png](pumpkin.png)
(they're friendly)

</div>

### Dictionary

RIS - Reverse Image Search <br>
Steg - steganography <br>


## Introduction

> Your entry flag, brave investigator, is the key into the Realm of the Pumpkin… 🎃🔑 <br>
> 🎃🎃🎃 hpCTF{Th4nk5_4_F0ll0w1ng_Th3_Ru135} 🎃🎃🎃

Arguably one of the hardest challenges. Jokes aside, the flag was at the end of the text.

<details>

<summary>Flag</summary>

Flag: `hpCTF{Th4nk5_4_F0ll0w1ng_Th3_Ru135}`

</details>


## Horror Clowns

> A few years ago, there were some people dressing up as Horror Clowns, showing up out of nowhere scaring the hell out of people as can be seen in the following staged video.
> Link: https://www.youtube.com/watch?v=vaXjN3zChyE <br><br>
> Can you find the name of the train station at minute 01:56? <br><br>
> Flag format: `hpCTF{station name}` <br>
> Flag example: `hpCTF{******* ***********}`

<details>
    <summary>Steps</summary>

1. Get a frame from the video that includes a decent amount of context
![001_horror_clowns.png](001_horror_clowns.png)
2. Use Google RIS on the match and click on the station, it should auto select
![002_horror_clowns.png](002_horror_clowns.png)
3. Going to the website of the first/second match you'll find the image, which leads you to the station
![003_horror_clowns.png](003_horror_clowns.png)


</details>

<details>
    <summary>Flag</summary>

    Flag: `hpCTF{Perugia Silvestrini}`
</details>

## My identity
> We recorded a grave raider last night. <br>
> Every information that can lead finding this person is a big help. <br>
> Maybe start with the birthday? <br><br>
> Flag Format: `hpCTF{YYYYMMDD}` <br>
> Flag Example: `hpCTF{19900615}` <br><br>
> Challenge image:
![004_my_identity.png](004_my_identity.png)

<details>
    <summary>Steps</summary>

1. Zooming closer in to the wallet, you'll see a coupe lines of gibberish. In Switzerland we call it bureaucracy though, anyways

![005_my_identity.png](005_my_identity.png)

2. Doing some research, this code seems to follow the MRZ TD1 standard, more specifically the second line

![006_my_identity.png](006_my_identity.png)

3. Simply extract the first 6 digits and you'll have the birthday

</details>

<details>
    <summary>Flag</summary>

    Flag: `hkCTF{19640812}`
</details>


## My identity - 2

> Great, the birthday is a good start! <br>
> But tell me, belongs this passport really to the man in the image? <br>
> Answer with yes or no. <br><br>
> Flag Format: hpCTF{<yes|no>}

<details>
    <summary>Steps</summary>

1. Reusing the image from last challenge you'll have to figure out if this passport belongs to the person on the image
2. You can clearly see that the person in the image is male, the MRZ TD1 on the image however shows that person is a female (The 8th character is a "F") 
    -> gender mismatch
</details>

<details>
    <summary>Flag</summary>

Flag: `hpCTF{no}` <br>
Reason: Different Gender
</details>


## Ghost Ship

> A Ghost Ship was found ashore. <br>
> Can you find the IMO number of the ship. <br><br>
> Flag Format: hpCTF{IMO_nr} <br><br>
> Challenge image:

![007_ghost_ship.png](007_ghost_ship.png)

<details>
    <summary>Steps</summary>

1. Usually these types of locations are pretty easily findable with Google RIS, so that's what I did

![007_ghost_ship.png](007_ghost_ship.png)

2. Google found multiple exact matches for the image which all relate to the ship "MV Alta"

![008_ghost_ship.png](008_ghost_ship.png)

3. Using a quick google dork `"MV Alta" + "IMO"` you'll find the IMO pretty quickly

</details>

<details>
    <summary>Flag</summary>

Flag: `hpCTF{7432305}`
</details>


## Ghost Ship - 2

> Can you also find out where the ship currently is ?

Of course I can.

<details>
    <summary>Steps</summary>

1. I proceeded to google dork the ships name with location ("MV Alta" + "location") again and got the following match: https://www.theultimateroadtripresource.com/location/discover-new-adventures/ghost-ship-mv-alta
2. The website showed a location near Ballyandreen Beach (51.81141248317834, -8.056514248978711), which I confirmed using satellite imagery

![009_ghost_ship.png](009_ghost_ship.png)

(Source: Google Maps)
</details>

<details>
    <summary>Flag</summary>

Flag: `51.81141248317834, -8.056514248978711` (on the map)
</details>

