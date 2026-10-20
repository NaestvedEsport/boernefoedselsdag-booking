# Børnefødselsdag – bookingportal (Næstved Esport)

Statisk bookingside til børnefødselsdage. Ingen build-trin – kun `index.html` og `assets/`.

## Sådan fungerer den
- Gæsten vælger dato (tidligst 2 uger frem, kun fredag fra kl. 14 samt lørdag og søndag), tid, varighed (3-12 t, brugerdefineret), deltagere (maks. 20), mad/drikke og ønsker.
- Prisen beregnes: 500 kr./t, +150 kr./t ved 16 eller flere deltagere. Mad og drikke er kun information (kioskdrikke 10 kr./stk. betales på dagen).
- Ved afsendelse åbnes en færdigudfyldt e-mail til Info@nesport.dk.
- Optagne tider vises **kun** hvis siden kører på claude.ai (delt kalender). På GitHub Pages er der ingen server, så kalenderen er slået fra, og e-mail er den eneste kanal.

## Udgiv med GitHub Pages
1. Læg filerne i et repo på `main`.
2. Settings → Pages → Source: **GitHub Actions**.
3. Siden ligger på `https://<org>.github.io/<repo>/`.

## Tilpasning
Priser og grænser: konstanterne `PRICE`, `EXTRA`, `KIOSK`, `MIN_H`, `MAX_N`, `FREE_N` i scriptet nederst i `index.html`.
Farver: CSS-variablerne øverst i `<style>`. Åbningstider: løkken der fylder `#start`.
