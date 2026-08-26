# Tehtäväraportti

Tämä teksti on kirjoitettu vastauksena Tero Karvisen [Tunkeutumistestaus-kurssin](https://terokarvinen.com/tunkeutumistestaus/) kotitehtävään h1 Kybertappoketju.

### Herrasmieshakkerit, jakso 0x3f, vieraana Niko Nirvi

- Valtaosaan ihmisistä ei kohdistu suoraa hyökkäystä tai uhkaa, vaan he joutuvat sivullisiksi uhreiksi.
- Suurimmat uhat tavallisille käyttäjille:
  - Varmuuskopioiden puute (esim. kuvat tai muu tärkeä data katoaa).
  - Tunnusten ja salasanojen päätyminen vääriin käsiin (samat tunnukset kaikkialla, yksi vuotaa -> kaikkialle pääsee sisään).
  - Huijaukset (pankkihuijaukset, valepoliisit, romanssihuijaukset).
- Lunnastroijalaiset eivät ole kotikäyttäjien ongelma, vaan lähinnä yrityskäyttäjien.
- Suuret pilvipalvelut ovat hyviä valintoja varmuuskopioille.
- Hyvä käytäntö, että jos ei ole kolmea kopiota, asiaa ei ole olemassa (hyvä ottaa talteen lisäksi esimerkiksi ulkoiselle kovalevylle).
- Tärkeä ymmärtää, miten huijarit pyrkivät huijaamaan uhriaan vetoamalla mm. kiireeseen tai poliisiin.
- Paineistettu tilanne -> rauhoita, puhelu pitoon, keskustele muiden kanssa ennen päätöksiä.
- Salasanalompakot ovat hyvä vaihtoehto.
- Lataa aina päivitykset.
- Selainlaajennukset voivat päätyä vääriin käsiin, jos alkuperäinen kehittäjä hylkää projektin tai myy sen jollekin muulle.
  - Jos käyttää laajennuksia -> tarkista kehittäjän taustat.

- Tekoälytyökalut auttavat löytämään lähdekoodista haavoittuvuuksia yhä useammin.

#### Vieras – pelijournalisti Niko Nirvi
- Tilanne muuttunut 90-luvulta: ennen pelaajat ja ei-pelaajat olivat napit vastakkain, nykyisin pelaaminenkin on politisoitunut ja jakautunut äärilaitoihin.

#### Miksi Herrasmieshakkerit tekevät podcastia?
- Näkevät toiminnan yhteiskunnallisena sivistystehtävänä.
- Positiivinen palaute perustelee tekemistä, kysyntää ja kuuntelijoita löytyy.

  **Oma huomio:**
  Mikko Hyppönen kertoi, että ei käytä mitään selainlaajennuksia. Oletettavasti ei siis edes mainosten estäjää. Jäi siis hieman avoimeksi, onko hänen käyttämässään selaimessa mainosten esto vakiona vai onko Hyppösen hermot terästä?

**Lähde:**  
Hyppönen, M. & Tuominen, T. 30.12.2025. Niko Nirvi 0x3f. Herrasmieshakkerit-podcast. Kuunneltavissa: https://herrasmieshakkerit.fi/. Kuunneltu: 22.8.2026.

---

### Kill Chain (suom. tappoketju, hyökkäysketju):

- Viittaa hyökkäyksen toteuttamisen prosessiin.
- Yhdenkin vaiheen epäonnistuminen keskeyttää hyökkäyksen.
- Lockheed Martinin tunkeutumisia koskevassa mallissa on seuraavat osat:
  - Tiedustelu (Reconnaissance): Kohteen tutkiminen ja valitseminen.
  - Aseistaminen (Weaponization): Haittaohjelman paketoiminen hyödynnettävään muotoon.
  - Toimitus (Delivery): Aseistetun tiedoston, verkkosivun tai muun toimittaminen kohteeseen.
  - Hyväksikäyttö (Exploitation): Haittaohjelman käynnistäminen hyödyntämällä käyttöjärjestelmässä olevaa haavoittuvuutta tai käyttäjän erhettä.
  - Asennus (Installation): Pysyvämmän etähallinnan mahdollistavan ohjelmiston asentaminen.
  - Komentaminen ja haltuunotto (Command and Control): Etähallintayhteyden käyttöönotto saastuneelta laitteelta hyökkääjän laitteelle.
  - Toiminta kohteessa (Actions on Objectives): Varsinaiset teot, kuten tiedon haltuunotto, muokkaaminen tai tuhoaminen.

**Lähde:**  
Hutchins, E. M., Cloppert, M. J. & Amin, R. M. 2011. Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains. Lockheed Martin. Luettavissa: https://lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/LM-White-Paper-Intel-Driven-Defense.pdf. Luettu: 23.8.2026.

---

### Porttiskannaus ja hakkerointi (O'Reilly)

- Porttiskannauksesta monesti saattaa tulla ilmoitus, mutta kukaan ihminen ei ole huomaamassa sitä.
- **Nmap:** Suosituin ja monikäyttöisin porttiskanneri.
- **Masscan:** Nopein porttiskanneri, jos skannaa laajasti. Samankaltainen kuin Nmap, nopeampi muttei yhtä monikäyttöinen.
- **Udpprotoscanner:** UDP-porttien skannaamiseen.
- Nmap-kohdalla hyvä huomioida:
  - `-Pn` on tärkeä parametri, muuten skannaus saattaa hypätä kohteen yli, jos se luulee kohteen olevan offline-tilassa.
  - Valmiita skriptejä on olemassa paljon.

**Lähde:**  
Santos, O., Taylor, R., Sternstein, J. & McCoy, C. The Art of Hacking (Video Collection): 4.3 Surveying Essential Tools for Active Reconnaissance. Katsottavissa: https://learning.oreilly.com/videos/the-art-of/9780135767849/9780135767849-SPTT_04_00/. Katsottu: 22.8.2026.

---

### Korkeimman oikeuden ratkaisu KKO:2003:36

- Pidetään historiallisena ennakkotapauksena.
- Luvattoman tunkeutumisen yrittäminen siinä varsinaisesti edes onnistumatta tulkittiin tietomurron yritykseksi.
- **Oma huomio:** Tärkeä siis tämänkin pohjalta huomioida, että yleisesti harjoitteissa ja tämän kurssin ohjeissa ihan syystäkin neuvotaan käyttämään virtuaalikonetta ja erillistä verkkoympäristöä.

**Lähde:**  
Korkein oikeus. Ennakkopäätös KKO:2003:36. Luettavissa: https://www.finlex.fi/fi/oikeuskaytanto/korkein-oikeus/ennakkopaatokset/2003/36. Luettu 24.8.2026.

---

## Tehtävät a–e

### a) Virtuaalikoneen ensiasetukset

Kalin asentaminen virtuaalikoneeseen tapahtui suoraviivaisesti lataamalla [Kali.org-verkkosivulta](https://www.kali.org/get-kali/#kali-virtual-machines) valmiiksi luotu virtuaalikone (pre-built virtual machine), purkamalla se tiedostonhallinnassa ja sen jälkeen valitsemalla VirtualBox-ohjelmiston näkymästä `Open` ja valitsemalla kyseinen `.vbox`-tiedosto. 

Kone ilmestyi virtuaalikoneiden listaan, mutta vielä ennen käynnistämistä klikattiin koneen kohdalta hiiren oikealla `Settings...` ja allokoitiin virtuaalikoneelle 4 Gt muistia. 

Käynnistämisen jälkeen ensimmäisenä päivitettiin pakettilistat ja asennettiin päivitykset komennolla:

`sudo apt update && sudo apt upgrade -y`

### b) Virtuaalikoneen irrottaminen verkosta

Virtual Boxin yläpalkista siirryttiin `Devices -> Network -> Network Settings... Attached to` -kohtaan ja valittiin `Host-only adapter`. Tämän myötä virtuaalikoneella on yhteys vain isäntäkoneeseen, mutta ei verkkoon. Tästä varmistuttiin pingaamalla Googlen DNS-palvelinta komennolla `ping 8.8.8.8`.

---

### c) Porttiskannaus

Porttiskannauksen yhteydessä skannattiin 1000 yleisintä tcp-porttia komennolla `nmap -T4 -A 127.0.0.1`

Tässä yhteydessä käytettiin suoraan IP-osoitetta, koska määreen `localhost` käyttäminen tuotti virheen, sillä verkosta eristämisen vuoksi kone ei saanut yhteyttä oletusarvoisesti tavoittelemaansa DNS-palvelimeen. Asian olisi voinut ratkaista myös vaihtoehtoisesti pakottamalla konetta käyttämään omaa sisäistä nimenselvennystä, jolloin komento kokonaisuudessaan olisi ollut muodossa `nmap -T4 -A --system-dns localhost`.

Komennossa `nmap` viittaa yleisesti käytettyyn työkaluun, minkä avulla on mahdollista skannata verkkoja. Seuraava `-T4` on puolestaan hakuprofiili mikä nopeuttaa skannausta. Hakuprofiileja on numerovälillä 0–5, suuremman numeron ollessa nopein. Määre `-A` lisää mukaan käyttöjärjestelmän ja versioiden tunnistuksen, skriptien ajamisen sekä reitin jäljityksen. Viimeisenä on localhost-osoite eli `127.0.0.1` mikä on koneen itseensä viittaama osoite.

Skannauksen tuloksena oli nähtävissä, että kaikki skannatut portit ovat kiinni eli toisin sanoen käynnissä ei ollut mitään palvelua, joka hyödyntäisi portteja ja olisi valmis vastaanottamaan yhteyksiä.



---

### d) Demoneiden asentaminen ja uudelleenskannaus

Seuraavaksi käynnistettiin kaksi asennettua taustapalvelua eli Apache2-webpalvelin ja OpenSSH-etähallintapalvelu komennoilla `sudo systemctl start apache2` ja `sudo systemctl start ssh`.

Kun porttiskannaus suoritettiin tämän jälkeen uudelleen, voitiin havaita, että portti 22 ja portti 80 ilmestyivät tulosteeseen listattuina avoimina portteina, sillä nämä palvelut odottavat mahdollisia yhteyksiä näiden porttinumeroiden kautta. Komennon sisältämän `-A` myötä myös versionumerot listattiin.

<img width="1350" height="536" alt="avoimet_portit" src="https://github.com/user-attachments/assets/1102a39f-8d17-4a9f-8e57-0eb7a3818015" />

---

### e) Hack the Box: Fawn

Ensimmäisenä Hack the Box harjoitteena suoritin aloittelijana helpommasta päästä olevan Fawn-harjoitteen.

Ensimmäiseksi sivu tarjosi OpenVPN-tiedostoa, jonka latasin ja otin käyttöön Linuxin yläpalkista klikkaamalla ethernet-portin symbolia ja `Add a VPN Connection...`, johon valittiin ladattu `.ovpn`-tiedosto.

Yhdistämisen jälkeen varmistuttiin, että yhteydet toimivat oikein lähettämällä `ping`-kutsu Googlen DNS-osoitteeseen `8.8.8.8` sekä VPN:n kytkettynä että pois päältä. VPN:n päällä yhteys ei toiminut, mutta pois päältä toimi, joten toiminta kuten piti.

<img width="1028" height="652" alt="vpn_yhteys" src="https://github.com/user-attachments/assets/5f93f794-af99-43f2-81c7-37137b9b3610" />

Fawn-harjoituksessa oli alkuun useita yleisluontoisia kysymyksiä, missä kysyttiin muun muassa FTP-lyhenteen alkuperää, porttinumeroita ja muita samassa yhteydessä hyödynnettäviä komentoja.

Ensimmäiset kysymykset, joissa tuli hyödyntää `nmap`-työkalua koskivat niin FTP:n kuin käyttöjärjestelmän versionumeroita. Näiden selvittäminen tapahtui komennolla `nmap -sV 10.129.171.49` vastauksien ollessa `vsftpd 3.0.3` ja `unix`.

FTP:n kautta kirjautuminen tapahtui puhtaasti arvaamalla anonyymin kirjautumisen tunnus `anonymous`. Salasanakenttä ei vaatinut syötettä ja onnistuneen kirjautumisen yhteydessä tuli koodi `230`, mikä toimi vastauksena HTB:ssä olleeseen kysymykseen.

Harjoituksen kohteena olleen `flag.txt`-tiedoston lataus tapahtui kirjautumisen jälkeen komennolla `get flag.txt`, mistä haettu merkkijono syötettiin Hack The Box -sivustolle näin viimeistellen harjoitteen suorituksen.

<img width="814" height="274" alt="flag_merkkijono" src="https://github.com/user-attachments/assets/f24e8884-ee03-4a51-bc88-555beecc9879" />

<img width="1586" height="1094" alt="fawn_ratkaistuna" src="https://github.com/user-attachments/assets/bb6ae27c-be37-4d29-9f97-fd0ab043ec73" />

