## Le côté obscur
```js
Points: 50
Solves: 36
```
<br>

*🇫🇷 – Quelle drôle d'application ! Une fois lancée, celle-ci semble être une façade dissimulant les activités cybercriminelles du groupe APT-509. L’un de nos experts a analysé l'application et a constaté, en examinant son code source, qu'une adresse e-mail y était potentiellement dissimulée. Malheureusement, il n'a pas réussi à la localiser.*
*En naviguant sur l'application, pouvez-vous aider notre expert à retrouver cette adresse?*

*🇬🇧 – What a strange application! Once launched, it appears to be a front hiding the cybercriminal activities of the APT-509 group. One of our experts analyzed the app and discovered, while inspecting its source code, that an email address might be hidden within it. Unfortunately, he was unable to locate it.*
*While navigating through the application, could you help our expert find this address?*

> *Flag format : cenestpasladressemaildhackolytequonrecherche@stpneflagpasca.fr*

<br>

As none of our team members had an android device, we had to get a little creative. We used an android emulator on our PCs (BlueStacks to be more specific) and downloaded the app there.
Browsing through the app, we find the info tab which includes contact details that are hidden for some reason, presumably because white font is not visible on a white background. Switching the app to dark mode with the button reveals the email address.

Flag: `str3etf1sher@mail.com`