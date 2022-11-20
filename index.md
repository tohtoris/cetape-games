---
layout: default
---
> You got the enemy flag!
> ...Captured!

Tervetuloa Cetape -lanidokumentaatioon. Tänne on koottuna olennaisimmat vinkit pelaamiseen ja laineihin osallistumiseen.

# Yleistä

Suosittelen avaaman tämän sivuston omalle kännykällesi pelien ajaksi, jolloin voit katsoa ohjeita poistumatta peli-ikkunasta.

Tämän sivun saat selaimeen esim. seuraavasta: 
![Cetape_QR_Code](https://github.com/tohtoris/cetape-games/raw/gh-pages/cetape-games-qr.png)

## Tietokone ja oheislaitteet
Jos mahdollista niin valitse/päätä ajoissa (hyvissä ajoin ennen kun pelit alkaa) laitekokoonpano jolla osallistut laneihin. Lainakoneena olevat setupit pyritään testaamaan ajoissa, jotta vierailevien tähtien osallistuminen olisi mutkatonta. Esim. headsettien osalta tämä ei ole välttämättä mahdolista joten varaudu testaamaan nämä heti saavuttuasi paikalle.

## Tarvittavat käyttäjätilit ja oheisohjelmat

Cetape-laneilla pelataan ensisijaisesti pelejä, jotka eivät vaadi kirjautumista tai erillisiä tunnuksia. Tästä voidaan poiketa erikseen sovittaessa. Tavoitteena on, että normaalisti vähän pelaavat pääsevät helposti mukaan. 

Voip-keskusteluissa käytetään **Discord**-palvelua, johon sinun tulee rekisteröindä oma tunnus ja liittyä kanavalle. Linkki Discordin Cetape-kanavalle löytyy Lani-kutsuista. Discordia voi käyttää selaimella tai erillisellä sovelluksella.

Vara-Voipina on käytetty **Mumblea**.

Testaa Laneilla pelattavaa peliä etukäteen, selvitä pääkontrollit, pikanäppäimet. Vinkkejä löydät täältä tai kysymällä.

# Pelit

### Asennus

#### Kotikone 

Pelipaketista jonka saat Cetape-kanavilta on binäärit **Linux, Mac, Win** -käyttiksille. Testaa pelin toiminta omalla konellasi ajoissa. Tarjolla on myös [puavo-pkg-asentimet](https://github.com/tohtoris/cetape-games) ja puavomenu template.

Kotikoneille asennuspaketit saa WA, Discord, Mattermost jne. kanavien kautta kyselemällä. Asennuspaketeissa pääpaino on x86-Linuxissa. Win & Mac löytynee kanssa, mutta näihin ei ole kiinnitetty erityistä huomiota ja joudut testaamaan nämä itse.

#### puavo-pkg asennus
```
git clone https://github.com/tohtoris/cetape-games
cd cetape-games
make
sudo puavo-pkg install peli.tar.gz
```

## OpenArena Truecombat

Yleisin pelattava peli on **Quake 3 (Openarena) modi Truecombat**. Alkuperäinen openarena löytyy [täältä](https://openarena.ws) ja truecombat [täältä](https://truecombat.com). Pelin idea:
* Truebombat on CS-tyylinen taistelupeli ja realismimodi Quake3-moottorille. Pelissä ei siis pysty loputtomasti juoksemaan, pomppimaan ja ottamaan iskua, vaan välillä pitää levätä ja nuolla haavoja. 
* Mitä enemmän kannat kamaa (Aseita, kypärä, liivit jne.) sitä kömpelömpi ja hitaampi olet.
* Yleensä pelataan joukkuettain "Lipun ryöstöä"
* Sama kenttä pelataan yleensä molempiin suuntiin
* Ennen peliä on mahdollista pitää yhdessä kenttäkatselmus jossa katsotaan yhdessä "laukkujen" paikat

### FAQ / Hyvä tietää

* Miten saan konsolin auki? `Shift + Esc`
* Miten pääsen työpöydälle sulkematta peliä? Ensin `Alt + Enter` ja sitten `Shift + Esc`
* Miten pääsen työpöydältä takas peliin? Etsi ikkuna ja sitten sama kuin yllä toisin päin ^ 
* Miten vaihdan joukkuetta? Avaa konsoli `Shift + Esc` ja kirjoita `/team red` tai `blue`

### Pelin käynnistäminen ja peliin liittyminen

**Käynnistäminen ja asetukset (ennen laneja)**
1. Käynnistä OpenArena
2. Valitse Modit
3. Valitse TrueCombat
4. Mene asetuksiin (Options > Player)
-- Aseta pelaajallesi nimi
-- Etsi näpäin asetukset ja muokkaa mieleiseksi
5. Testaa peliä/näppäimiä jne. luomalla itsellesi paikallinen serveri (voit lisätä botteja)

Eniten laneissa pelatut kentät: Bahamut, Casino...... muita pitää kaivella listaa

**Peliin liittyminen (Lanit)**
* Käynnistä Openarena
* Valitse Multiplayer > Specify > Kirjoita pelipalvelimen osoite
* Paina `Esc` ja valitse `Join`
* Valitse aina Autoteam (Joukkue kannattaa valita jälkeen päin komentoriviltä)
* Muista valita ase ja siihen lippaita

### Resoluution asettaminen

Openarena ei ymmärrä mitään laajakuvaresoluutioista, joten saatat joutua editoimaan resoluutioita käsin pelin q3config.cfg-tiedostosta. Resoluutio on oletuksena pyritty asettamaan FullHD-asetuksella. Lanikoulussa olevilta koneilta tiedosto löytyy suoraan pikalinkkinä käynnistys (Menu)-valikosta. Voit editoida myös haluamallasi tekstiedotorilla komentoriviltä seuravasti.

```
cd .openarena/truecombat
gedit q3config.cfg
```
Etsi seuraava asetus ja...
```
seta r_customheight "1080"
seta r_customwidth "1920"
seta r_noborder "0"
seta r_fullscreen "1"
seta r_mode "-1"
```
1. syötä oma resoluutio. 
2. huolehdi että set `r_mode on -1`
3. tallenna
4. käynnistä peli uudelleen

### Oletusnäppäimet

Oletuksina käytettävät kontrollit ovat (nämä tietysti voit muokata mieleiseksesi)

| **Tapahtuma**             | **Kontrolli**          | **Huomioita**                                                |
|---------------------------|------------------------|--------------------------------------------------------------|
| Valitse ase / suojat jna. | M                      | Toimii omassa basessa / tulee voimaan kun "synnyt uudelleen" |
| Liikkuminen               | WASD                   |                                                              |
| Katseen liikutus          | Hiiri                  |                                                              |
| Kurkkaa nurkan taakse     | Q & E                  |                                                              |
| Hyppy                     | Välilyönti             |                                                              |
| Kykkyyn                   | C                      |                                                              |
| Juokse                    | Shift                  |                                                              |
| Kerää lippu/laukku        | Kyykisty laukun päälle |                                                              |
| Aseen lataaminen          | R                      |                                                              |
| Pudota ase                | Z                      |                                                              |
| Oven avaus                | Enter                  |                                                              |
| Tähtääminen               | Vasen hiiri            |                                                              |
| Haavan sitominen (bandage) | B                      |                                                              |
| Puhu kaikille             | P                      |                                                              |
| Puhu tiimille             | T                      |                                                              |





##### Tulee joskus....

#### ETLegacy



#### Doom


#### Quake

