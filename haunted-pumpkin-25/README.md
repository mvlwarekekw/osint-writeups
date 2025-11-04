<div style="display:flex; flex-direction: column; align-items: center;">
<h1> Haunted Pumpkin CTF '25 </h1>
<h3> Fun CTF organized by OSINT Switzerland </h3>
<h4>DISCLAIMER: All of these challenges were made for educational purposes only and should not be used for malicious purposes. I do not own any of the challenge assets below, all credits go to OSINT switzerland.</h4>

![pumpkin.png](pumpkin.png)
(they're friendly)

</div>
<br>

## Dictionary

RIS - Reverse Image Search <br>
Steg - steganography <br>
(Google) dork - advanced search query <br>

<br>

## Introduction

> Your entry flag, brave investigator, is the key into the Realm of the Pumpkin… 🎃🔑 <br>
> 🎃🎃🎃 hpCTF{Th4nk5_4_F0ll0w1ng_Th3_Ru135} 🎃🎃🎃

Arguably one of the hardest challenges. Jokes aside, the flag was at the end of the text.

<details>

<summary>Flag</summary>

Flag: `hpCTF{Th4nk5_4_F0ll0w1ng_Th3_Ru135}`

</details>

<br>

## Horror Clowns

> A few years ago, there were some people dressing up as Horror Clowns, showing up out of nowhere scaring the hell out of people as can be seen in the following staged video.
> Link: https://www.youtube.com/watch?v=vaXjN3zChyE <br><br>
> Can you find the name of the train station at minute 01:56? <br><br>
> Flag format: `hpCTF{station name}` <br>
> Flag example: `hpCTF{******* ***********}`

<details>
    <summary>Steps</summary>

1. Get a frame from the video that includes a decent amount of context
![001_horror_clowns.png](./assets/001_horror_clowns.png)
2. Use Google RIS on the match and click on the station, it should auto select
![002_horror_clowns.png](./assets/002_horror_clowns.png)
3. Going to the website of the first/second match you'll find the image, which leads you to the station
![003_horror_clowns.png](./assets/003_horror_clowns.png)


</details>

<details>
    <summary>Flag</summary>

    Flag: `hpCTF{Perugia Silvestrini}`
</details>

<br>

## My identity
> We recorded a grave raider last night. <br>
> Every information that can lead finding this person is a big help. <br>
> Maybe start with the birthday? <br><br>
> Flag Format: `hpCTF{YYYYMMDD}` <br>
> Flag Example: `hpCTF{19900615}` <br><br>
> Challenge image:
![004_my_identity.png](./assets/004_my_identity.png)

<details>
    <summary>Steps</summary>

1. Zooming closer in to the wallet, you'll see a coupe lines of gibberish. In Switzerland we call it bureaucracy though, anyways

![005_my_identity.png](./assets/005_my_identity.png)

2. Doing some research, this code seems to follow the MRZ TD1 standard, more specifically the second line

![006_my_identity.png](./assets/006_my_identity.png)

3. Simply extract the first 6 digits and you'll have the birthday

</details>

<details>
    <summary>Flag</summary>

    Flag: `hkCTF{19640812}`
</details>

<br>

## My identity - 2

> Great, the birthday is a good start! <br>
> But tell me, belongs this passport really to the man in the image? <br>
> Answer with yes or no. <br><br>
> Flag Format: `hpCTF{<yes|no>}`

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

<br>

## Ghost Ship

> A Ghost Ship was found ashore. <br>
> Can you find the IMO number of the ship. <br><br>
> Flag Format: hpCTF{IMO_nr} <br><br>
> Challenge image:

![007_ghost_ship.png](./assets/007_ghost_ship.png)

<details>
    <summary>Steps</summary>

1. Usually these types of locations are pretty easily findable with Google RIS, so that's what I did

![007_ghost_ship.png](./assets/007_ghost_ship.png)

2. Google found multiple exact matches for the image which all relate to the ship "MV Alta"

![008_ghost_ship.png](./assets/008_ghost_ship.png)

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
2. The website showed a location near Ballyandreen Beach (51.81141248317834, -8.056514248978711), which we confirmed using satellite imagery

![009_ghost_ship.png](./assets/009_ghost_ship.png)

(Source: Google Maps)
</details>

<details>
    <summary>Flag</summary>

Flag: `51.81141248317834, -8.056514248978711` (on the map)
</details>

<br>

## Dude where was this car

> You leave the tunnel where the car enters at the end of the clip: https://www.youtube.com/watch?v=j6-yVoJTCo8 <br>
> There is a little public rest room with a green roof at the parking lot on the left side (Year 2021). <br>
> A few meters further (also on the left side) there is a sign which was build between 2008 and 2009. <br><br>
> What does the sign say? <br><br>
> Flag Format: hpCTF{***** ***** **}


<details>
    <summary>Steps</summary>

1. I started off with extracting a frame from the video, that I thought contained the most information and google RISed it. The Facebook post had a much clearer image without any filter, so I decided to reuse that image to RIS again.

![010_dude_where_was_this_car.png](./assets/010_dude_where_was_this_car.png)
![011_dude_where_was_this_car.png](./assets/011_dude_where_was_this_car.png)

2. Looking at the second RIS, you'll see a lot of sources mentioning Zion national park (Utah, US). As the question mentions a restroom, its safe to assume that its close to the tunnel entrance. 
   I checked both tunnel exits for a parking lot and a house with a green roof and eventually found [this restroom house](https://maps.app.goo.gl/8XbZzcn7VkTiNHAv5).
3. Looking at the streetview from 2009, we were able to find the following sign at the tunnel entrance: 

![012_dude_where_was_this_car.png](./assets/012_dude_where_was_this_car.png)

</details>

<details>
    <summary>Flag</summary>

Flag: `hpCTF{Speed Limit 25}`
</details>

<br>

## I Like Trains

> What classification code is written on the side of that train? <br><br>
> Flag Format: hpCTF{* *** * ****} <br><br>
> Challenge image:

![013_i_like_trains.png.png](./assets/013_i_like_trains.png)

<details>
    <summary>Steps</summary>

1. The image doesn't really have any context, so I decided to google RIS yet again

![014_i_like_trains.png](./assets/014_i_like_trains.png)

2. The first match looks the exact same and seems to be a frame of [this video](https://www.youtube.com/watch?v=kqp9uFIQtMM).
3. As the video contains no identifiers and the description doesn't mention the classification code, we'll have to google dork the name in the description with the site trains.com (`"Markus Zaugg" + "snowplow" site:trains.com`).
4. You'll have to check for yourself, but for me the first match linked to an article with a snowplow. The article mentions the name "Xrot 9213", which with a quick google search revealed the full classification code.

</details>

<details>
    <summary>Flag</summary>

Flag: `hpCTF{X Rot d 9213}`

</details>

<br>

## Trash Belongs Into The Bin

> Look what someone threw into the bin: 6W2XQjJP <br>
> This does not look like a youtube extension to me ... But wait, there is something written next to it: <br>
> “He crafts his games with fear and might, <br>
> A puzzling man who haunts the night.  <br>
> The hash will lead, now take your chance—  <br>
> The file you find with a second glance ” <br> <br>
> Which wicked and malicious file holds this individuums name?  <br> <br>
> Flag Format: `hpCTF{******.***}` <br>
> Flag Example: `hpCTF{sealss.exe}`

<details>
    <summary>Steps</summary>

1. The challenge title and description themselves already have quite a few hints. More specifically "the bin" and "the file". The first thing I thought of checking out was pastebin, as it pretty much checks both boxes.
2. There was a file with that path indeed: https://pastebin.com/6W2XQjJP. It contained a hash, presumably a file hash.
3. Whenever you encounter a file hash, you should check out VirusTotal and look it up there. You can see file names in the details tab, so I decided to check that and there it was!

![015_trash_belongs_into_the_bin.png](./assets/015_trash_belongs_into_the_bin.png)
</details>

<details>
    <summary>Flag</summary>

Flag: `hpCTF{Jigsaw.exe}`
</details>

<br>

## The Halloween Party

> There is Flag is in this room. I guess you know what to do ... <br><br>
> Flag format: `hpCTF{<flag>}` <br><br>
> Challenge Image:

![016_the_halloween_party.png](./assets/016_the_halloween_party.png)

<details>
    <summary>Steps</summary>

1. The objective for this one is quite clear: Scan the QR code. Easier said than done as its slightly obstructed at the top right. 
2. We used QRazybox to reconstruct it, although its arguably easier just drawing the missing lines
 
![017_the_halloween_party.png](./assets/017_the_halloween_party.png)

3. Scanning the QR code gives you the flag

</details>

<details>
    <summary>Flag</summary>

Flag: `hpCTF{051N7_5W17Z3RL4ND_H4LL0W33N_CTF}`
</details>

<br>

## Fake News

> Fake news like these spread more wildely than ever. <br>
> Can you find out who was actually arrested here? <br><br>
> Flag Format: `hpCTF{**** *** ***-*****}` <br><br>
> Challenge image: <br>

![018_fake_news.png](./assets/018_fake_news.png)

<details>
    <summary>Steps</summary>

1. Cutting out a part of an image usually works pretty well most of the time, which worked for this one. The image on the right links to an article which includes part of the name: `Ryan Law`
![019_fake_news.png](./assets/019_fake_news.png)
2. Simply searching for him on google shows the full name
![020_fake_news.png](./assets/020_fake_news.png)

</details>
 
<details>
    <summary>Flag</summary>

Flag: `hpCTF{Ryan Law Wait-kwong}`
</details>

<br>

## Fake News - 2

> Can you also find which age Ryan was when he was arrested? <br>
> Flag Format: hpCTF{**}

<details>
    <summary>Steps</summary>

1. Carefully craft a google dork with his full name and the string "age" (`"ryan law wai-kwong" + "age"`)
2. Click the [first link](https://www.hongkongwatch.org/political-prisoner/2024/10/30/ryan-law-wai-kwong) which shows the age when he was arrested. You could also try to figure out his birthday and calculate the difference, but that's arguably more complicated.
</details>

<details>
    <summary>Flag</summary>

Flag: `hpCTF{46}`
</details>

<br>

## Follow The Money

> a11ab03eeb08f4914bc6d7421dca96ebd6c96ff1c9b3e028d3a268cf44c21aff <br><br>
> Flag Format: `hpCTF{<programming_language>}` <br><br>
> Challenge image:

![021_follow_the_money.png](./assets/021_follow_the_money.png)

<details>
    <summary>Steps</summary>
    
1. The provided image has some japanese text talking about a donation to a software development studio and us having to figure out what programming language they use the least, so lets do that.
2. That looks like a bitcoin TX hash to me, so I'll start looking on btcscan.org. Indeed, there was a TX with said hash, sent to the address `18kj9UWRZC9YxZMoN2iz2A8Xmwqxxdyp8X`, presumably the address of the software development studio referred to in the challenge description. 

![022_follow_the_money.png](./assets/022_follow_the_money.png)

3. Doing a quick google search with that BTC address, you'll find their website: https://flacon.github.io/donate/.
4. Heading to their GitHub, it'll show you the percentages of used programming languages on the right side, which in this case was `Roff`.

![023_follow_the_money.png](./assets/023_follow_the_money.png)

(disclaimer: technically speaking this is a markup language rather than a programming language)
</details>

<details>
    <summary>Flag</summary>

Flag: `hpCTF{Roff}`
</details>