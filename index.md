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

Yleisin pelattava peli on **Quake 3 (Openarena) modi Truecombat**. Alkuperäinen openarena löytyy [täältä](https://openarena.ws) ja truecombat [täältä](http://www.truecombatelite.com). Pelin idea:
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
cd .openarena/baseoa  # (jos liityt peliin käynnistämällä Openarena > Multiplayer [yleisin]) TAI  cd .openarena/truecombat (Jos liityt peliin Openarena > Mods > Truecombat)
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
| Haavan sitominen (bandage) | B                      |                                                             |
| Puhu kaikille             | P                      |                                                              |
| Puhu tiimille             | T                      |                                                              |





## ETLegacy

### Asennus

#### Oma Puavo-kone
Helpoin tapa on, että 
1. haet pelipaketin chätti-kanavilla saatavista linkeistä
2. purat paketin kotikansioon
3. käynnistät pelin kotikansiostasi 

#### Oma koti-linux-kone
Linuxilla tällä pelillä on riippuvuuksia joita ei välttämättä ole järjestelmässäsi asennettuna.  
Tässä Debian/Ubuntu-kohtaiset komennot riippuvuuksien asentamisesta, muokkaa tarvittaessa itse sopivaksi omalle distrollesi:
```
sudo dpkg --add-architecture i386
sudo apt update
sudo apt install libasound2-plugins libdrm2:i386 libexpat1:i386 libglu1-mesa:i386 libgl1:i386 libsdl2-2.0-0:i386 libxext6:i386
```
Lataa pelin **32-bittinen** (i386) versio osoitteesta [ETLegacy.com](https://www.etlegacy.com/download) tai puavo-pkg-asennuksella (ohje ylempänä)

### FAQ / Hyvä tietää

* Miten saan konsolin auki? `½§ -näppäin (Esc ja Tab -näppäinten välissä, 1-näppäimen vasemmalla puolella)`
* Miten pääsen työpöydälle sulkematta peliä? `Esim. Alt-Tab tai Win/Super/Meta -näppäin` 
* Miten pääsen työpöydältä takas peliin? `Paina sovelluksen kuvaketta järjestelmäsi tehtäväpalkista` 
* Miten vaihdan joukkuetta tai hahmoa? `Palvelimella ollessasi, avaa "Limbo-menu" L-näppäimestä.`

### Pelin käynnistäminen ja peliin liittyminen

#### Puavo-koneet
Lähtökohtaisesti on suositeltavaa purkaa ja asentaa pelipaketti omaan kotikansioon (kuten yllä neuvottu). Voit käynnistää pelin  **`run-etl.sh`** -skriptillä.

Lainakoneille peli on saatettu asentaa kivasti valmiiksi puavo-pkg:nä ja se löytyy sovellusvalikosta.

#### Omat koneet

Jos pelaat Linuxilla omalla koneella (ei Puavo), ETLegacyn sivuilta ladattava asennin kannattaa siirtää esim. käyttäjäsi home-kansioon. Tällöin peli asentuu homen alle `etlegacy-(versionumero)` kansioon.
Tällöin tee kansioon tiedosto **`run-etl.sh`** jonka sisältö on `LD_PRELOAD=/usr/lib/i386-linux-gnu/libXext.so.6 ./etl.i386` (Linuxillä tätä on käytettävä! Tarvittaessa salli tekemäsi tiedoston suorittaminen ohjelmana).  
Voit myös ladata puavo-pkg-asentimen sisältä löytyvän linkin kautta uusimman ETLegacy paketin, johon on tämä tärkeä tiedosto lisätty jo kivasti mukaan.

Muilla järjestelmillä asennusohjelman pitäisi tehdä kivasti pikakuvake josta pelin saa käyntiin.

**Käynnistäminen ja asetukset (ennen laneja)**
1. Käynnistä ET:Legacy.  
2. Säädä pelaajanimesi ja asetuksesi pelin antamalla ensikäynnistysruudulla. Loput asetukset voit tämän jälkeen säätää kohdilleen Menusta "Options -> Game/View/Controls/System".  
3. Testaa yhdistää palvelimelle joko etsimällä se palvelinlistauksesta nimellä "ceTAPE Joululaniserveri" tai konsolin kautta komennolla `/connect wolf.risusama.eu:27960` - salasanan saat ceTAPE -viestintäkanavilta.  
4. Mikäli yhdistämisessä tulee ongelmia (eritoten virheilmoitus `... invalid GUID ...`, kopioi  
   a. Linuxilla: tiedosto `$HOME/.etlegacy/etmain/etkey` sijaintiin `$HOME/.etlegacy/silent/etkey`  
   b. Windowsilla tiedosto `%userprofile%\Documents\ETLegacy\etmain\etkey` sijaintiin `%userprofile%\Documents\ETLegacy\silent\etkey`  
   c. Mikäli tiedostoa ei ole etmain-kansiossa, generoi sen sisältö [ETclan.de -sivulla](https://www.etclan.de/etkey.php) ja tallenna se kumpaankin sijaintiin.  
5. Muussa tapauksessa voit olla myös yhteydessä esim. Risuun, joka osannee auttaa ja selvitellä ETLegacyyn liittyviä vikatilanteita.

### Oletusnäppäimet

Oletuksina käytettävät kontrollit ovat (nämä tietysti voit muokata mieleiseksesi)

| **Tapahtuma**                                            | **Kontrolli**             | **Huomioita**                                                |
|----------------------------------------------------------|------------------------   |--------------------------------------------------------------|
| Valitse tiimi, hahmo, aseet jne.                         | L                         | Toimii missä vaan, tulee voimaan kun "synnyt uudelleen"      |
| Liikkuminen                                              | WASD                      |                                                              |
| Katseen liikutus                                         | Hiiri                     |                                                              |
| Kurkkaa nurkan taakse                                    | Q & E                     |                                                              |
| Hyppy                                                    | Välilyönti                |                                                              |
| Kykkyyn                                                  | C                         |                                                              |
| Makuulle                                                 | X                         |                                                              |
| Juokse                                                   | Shift                     |                                                              |
| Kerää esine (esim. healthpack) tai objective             | Kävele esineen päältä     |                                                              |
| Käytä esinettä/ovea/poimi uusi ase maasta (kädenkuva)    | F                         |                                                              |
| Kädessä olevan esineen vaihto                            | 1-8 tai hiiren rulla      |                                                              |
| Aseen lataaminen                                         | R                         |                                                              |
| Tähtääminen                                              | Oikea hiiri               |                                                              |
| Ampuminen                                                | Vasen hiiri               |                                                              |
| Hahmokohtaisten erikoisasioiden käyttö                   | 6 ja sitten vasen hiiri   |                                                              |
| Puhu kaikille                                            | T                         |                                                              |
| Puhu tiimille                                            | Y                         |                                                              |



##### Tulee joskus....

#### Doom


#### Quake

