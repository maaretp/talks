# Yhteinen kieli koodiin asti: DDD ja BDD käytännössä

*Kesto: 2 päivää*

Liiketoiminta, määrittely, arkkitehtuuri, kehitys ja testaus käyttävät usein samoja sanoja eri merkityksissä. Kun "hanke", "hakemus" tai "kustannus" tarkoittaa eri asiaa eri pöydän ääressä, ero näkyy ensin keskusteluissa, sitten vaatimuksissa ja lopulta koodissa ja testauksessa korjattavina virheinä. Domain Driven Design (DDD) ja Behavior Driven Development (BDD) ovat tapoja rakentaa yhteinen kieli ja käsitteistö, joka kulkee liiketoiminnan keskustelusta koodiin ja testeihin asti.

Tällä kurssilla opimme tekemällä. Ensimmäisenä päivänä mallinnamme toimialaa: rakennamme yhteistä kieltä, teemme Event Stormingia, jossa seinälle kirjoitettu lappu johtaa keskustelua ja kommentointia, ja tunnistamme alidomainit ja bounded contextit. Seinän tuloksista tuotamme tekoälyn avulla LLM-wiki-tyyppistä määrittelymateriaalia: linkitettyjä sanasto-, tapahtuma-, konteksti- ja päätössivuja, jotka ihminen katselmoi ja jotka kasvavat seuraavissa keskusteluissa. Wikistä johdetaan tekoälyllä myös kuvia, kuten tapahtumien aikajana ja kontekstikartta. Kuva on wikin näkymä, ja kun kuva ja seinä eroavat, ero on löydös.

Toisena päivänä viemme mallin toimitettavaksi ja testattavaksi. Ryhmittelemme työn story mappingilla arvon siivuiksi ja tuotamme ensimmäisestä siivusta tekoälyn avulla klikattavan proton wikin sanastolla. Proto ei ole määrittely vaan keskustelun väline: kun liiketoiminnan asiantuntija käy sen läpi käyttäjän roolissa, havainnot palaavat wikiin uusina kysymyksinä, sääntöinä ja esimerkkeinä. Sen jälkeen konkretisoimme liiketoimintasäännöt esimerkeiksi Example Mappingilla, nimeämme esimerkit Frendit-jaksojen tapaan ("Jakso, jossa...") ja kirjoitamme niistä Gherkin-skenaarioita. Päivän lopuksi katsomme, miten taktisen DDD:n rakennuspalikat ja suoritettavat skenaariot näkyvät koodissa ja testauksessa.

Harjoitukset tehdään organisaation omaan toimintaympäristöön perustuvan casen avulla. Case valmistellaan yhdessä tilaajan kanssa ennen kurssia. Osallistujat työskentelevät sekaryhmissä, joissa jokaisessa on liiketoiminnan, määrittelyn, arkkitehtuurin, kehityksen ja testauksen näkökulma. Kurssin tuotokset (seinäkuvat, wiki, kuvat, story map, proto ja skenaariot) jäävät organisaation käyttöön ja jatkotyön pohjaksi.

Kurssi on tarkoitettu liiketoiminnan asiantuntijoille, tuoteomistajille, määrittelijöille, arkkitehdeille, kehittäjille ja testaajille, jotka tekevät yhdessä samaa järjestelmää. Kurssikerralle mahtuu enintään 24 osallistujaa.

## Oppimistavoitteet

Kurssin jälkeen osallistuja:

* tuntee strategisen DDD:n keskeiset periaatteet: domain, alidomainit (ydin, tukeva, geneerinen), yhteinen kieli ja bounded contextit
* osaa osallistua Event Storming -työpajaan ja fasilitoida sitä sekä tunnistaa sen tuloksista kontekstirajat
* osaa kuvata kontekstien väliset suhteet ja integraatiot Context Mappingilla
* osaa jalostaa työpajan raakasyötteen tekoälyn avulla linkitetyksi, katselmoitavaksi määrittelymateriaaliksi
* osaa tuottaa wikistä tekoälyn avulla kuvia ja klikattavia protoja ja käyttää niitä keskustelun ja palautteen välineinä niin, että havainnot palaavat wikiin
* osaa ryhmitellä toiminnallisuudet story mapilla arvon siivuiksi
* osaa konkretisoida liiketoimintasäännöt ja hyväksymiskriteerit esimerkeiksi Example Mappingilla ja kirjoittaa niistä Gherkin-skenaarioita
* tuntee taktisen DDD:n perusteet ja ymmärtää, miten yhteinen kieli ja esimerkit kulkevat koodiin ja testaukseen

## Sisältö

### PÄIVÄ 1: Toimialan mallintaminen yhdessä

Päivän avaus: Oppimistavoitteet ja casen esittely

* Miksi yhteinen kieli? Määrittelyn, toteutuksen ja testauksen väliin jäävät aukot
* Case: valittu prosessialue ja sen toimijat, säännöt ja järjestelmät

Sessio 1: DDD:n perusajatus – liiketoiminnan ja koodin yhteinen kieli

* Domain, alidomainit ja niiden luokittelu: ydin, tukeva, geneerinen
* Yhteinen kieli (ubiquitous language): sana, jolla on yksi merkitys yhdessä kontekstissa
* HARJOITUS: Casen keskeiset käsitteet – mitä sana tarkoittaa sinun työssäsi?
* Katsaus tehtyyn: mitä opimme?

Sessio 2: Event Storming – lappu johtaa keskustelua

* Big Picture Event Storming: toimialatapahtumat aikajanalla
* Lappu ensin, keskustelu sitten: kirjoita, lue ääneen, kommentoi, siirrä
* Kuumat kohdat (hotspots): ristiriidat, avoimet kysymykset ja kipupisteet näkyviksi
* HARJOITUS: Casen tapahtumat alusta loppuun, poikkeukset mukaan lukien
* Katsaus tehtyyn: mitä opimme?

Sessio 3: Prosessitason Event Storming

* Komennot, toimijat, säännöt (policies), lukumallit ja ulkoiset järjestelmät
* Yhteinen runko ja perustellut muunnelmat: mikä on oikeasti erilaista ja mikä vain historiallisesti eriytynyttä
* HARJOITUS: Yksi casen prosessi tarkemmalle tasolle
* Katsaus tehtyyn: mitä opimme?

Sessio 4: Bounded contextit ja Context Mapping

* Kontekstin raja on siellä, missä kieli muuttuu
* Kontekstien suhteet: customer–supplier, conformist, anti-corruption layer, shared kernel, published language
* Integraatiot ulkoisiin järjestelmiin ja viranomaisiin kontekstikartalla
* HARJOITUS: Casen kontekstikartta seinän tapahtumista
* Katsaus tehtyyn: mitä opimme?

Sessio 5: Seinältä wikiksi – määrittelymateriaali tekoälyn avulla

* LLM-wiki: raakasyöte tallennetaan sellaisenaan, tekoäly jäsentää sen linkitetyiksi sivuiksi, ihminen katselmoi
* Sanasto, tapahtumat, kontekstit, päätökset ja avoimet kysymykset omina sivuinaan
* Kuvat wikin näkyminä: tekoäly piirtää aikajanan ja kontekstikartan sivuista, ei seinästä
* Mitä tekoäly tekee hyvin ja mitä se keksii: lähteettömät väitteet oletuksiksi
* HARJOITUS: Päivän seinäkuvista ja muistiinpanoista wikiksi ja wikistä kuviksi
* Katsaus tehtyyn: mitä opimme?

Keskustelu päivän päätteeksi: Päivän seinästä arkipäivän malleihin

* Milloin mallinnetaan ennen toteutusta, milloin toteutuksen aikana
* Wiki jää auki: kysymykset ja havainnot yön yli

### PÄIVÄ 2: Esimerkeistä toimitettavaan ja testattavaan

Päivän avaus: Oppien kertaus ja wikin katselmointi

* Mitä wikiin tuli yön yli ja mikä muuttui

Sessio 6: Story mapping ja proto – ryhmittely arvon siivuiksi

* Selkäranka Event Stormingin aikajanasta: käyttäjän toiminnot vasemmalta oikealle
* Tarinat toimintojen alle, kiireellisyys ylhäältä alas
* Arvon siivu: pienin käyttöön otettava kokonaisuus, joka opettaa jotain
* Proto määrittelyn rinnalla: tekoäly tuottaa siivusta klikattavan proton wikin sanastolla, ja läpikäynnin havainnot palaavat wikiin
* HARJOITUS: Casen story map, ensimmäinen siivu ja sen proto
* Katsaus tehtyyn: mitä opimme?

Sessio 7: Example Mapping ja Specification by Example

* Tarina, säännöt, esimerkit ja kysymykset: neljä lappuväriä ja 25 minuutin aikalaatikko
* Proto keskustelun tukena: mitä käyttäjä näkee tässä esimerkissä?
* Frendit-jaksot: esimerkin nimi kertoo tilanteen ("Jakso, jossa kustannusselvitys puuttuu")
* Liiketoiminta, kehitys ja testaus samassa keskustelussa: kolme amigoa
* HARJOITUS: Ensimmäisen siivun tarinat esimerkkikartoiksi
* Katsaus tehtyyn: mitä opimme?

Sessio 8: Gherkin – esimerkit hyväksymiskriteereiksi

* Given / When / Then yhteisellä kielellä: wikin sanasto skenaarioiden sanastona
* Deklaratiivinen vai imperatiivinen: kuvataan käyttäytymistä, ei klikkauksia
* Rule, Scenario Outline ja esimerkkitaulukot
* Tekoäly luonnostelee, ihminen katselmoi: puuttuvat poikkeukset ja ristiriidat sääntöihin
* HARJOITUS: Frendit-jaksoista Gherkin-skenaarioiksi ja takaisin wikiin
* Katsaus tehtyyn: mitä opimme?

Sessio 9: Taktisen DDD:n perusteet

* Entiteetti, arvo-olio, aggregaatti, toimialatapahtuma, repository ja toimialapalvelu
* Aggregaatin invariantit ovat Example Mappingin sääntöjä
* Tilakaavio wikistä: tekoälyn piirtämä kuva verrattuna ryhmän omaan
* HARJOITUS: Casen keskeisen aggregaatin invariantit ja niitä vastaavat skenaariot
* Katsaus tehtyyn: mitä opimme?

Sessio 10: DDD ja BDD käytännön kehityksessä ja testauksessa

* Suoritettavat skenaariot: skenaariosta ajettavaksi testiksi (esim. Cucumber, Behave, pytest-bdd)
* Mille tasolle skenaario kuuluu: toimialamalli, rajapinta vai käyttöliittymä
* Jäljitettävyys: lähde → sääntö → esimerkki → skenaario → testi → havainto takaisin wikiin
* Proto, skenaario ja toteutus: mikä on määrittelyä, mikä näkymä ja mikä heitetään pois
* Mitä BDD ei korvaa: tutkiva testaus sille, mitä kukaan ei määritellyt
* DEMO: Skenaario ajettavaksi testiksi agentin avulla

Keskustelu päivän päätteeksi: Päivän esimerkeistä arkipäivän malleihin

* Mistä aloitetaan omassa työssä huomenna
* Tuotosten jatkokäyttö ja osaamisen syventäminen

## Casen valmistelu tilaajan kanssa

Case valmistellaan yhdessä tilaajan kanssa ennen kurssia, jotta harjoitukset tehdään omalla toimialalla ja tuotokset ovat hyödyllisiä myös kurssin jälkeen.

* **Prosessialueen valinta.** Hyvä case on rajattu mutta sisältää poikkeuksia, sääntöjä ja integraatioita. Esimerkiksi päätöksen jälkeinen toimeenpano, kuten maksatus, muutokset tai takaisinperintä, tuo esiin sekä yhteisen rungon että perustellut muunnelmat.
* **Lähtöaineisto.** Nykyiset prosessikuvaukset, ohjeet, lomake- ja päätöspohjat sekä olemassa oleva käsitteistö. Aineisto tallennetaan wikin raakasyötteeksi.
* **Valmistelutapaaminen (2 h).** Käydään läpi aineisto, sovitaan casen rajaus ja tunnistetaan kurssilla paikalla olevat asiantuntijat, joilta kysytään.
* **Ryhmäjako.** Sekaryhmät, joissa kussakin on liiketoiminnan, määrittelyn, arkkitehtuurin, kehityksen ja testauksen edustus.
* **Työkalut.** Seinätila ja laput tai yhteinen digitaalinen taulu sekä tilaajan hyväksymä tekoälytyökalu, joka lukee ja kirjoittaa wikin tiedostoja ja tuottaa kuvia (esim. Mermaid) ja HTML-protoja. Lisäksi tarvitaan tapa näyttää kuvat ja protot ryhmälle, esimerkiksi editorin esikatselu ja selain. Luottamuksellista aineistoa käsitellään vain tilaajan tarjoamilla työkaluilla.

## Koulutuksen erityispiirteitä

* Kurssi on käytännönläheinen ja osallistava: valtaosa ajasta tehdään harjoituksia omalla casella, ja jokaisen harjoituksen jälkeen katsotaan yhdessä, mitä opimme
* Kouluttaja on aihepiirin syvällinen osaaja sekä pidetty puhuja, joka on kouluttanut vaatimusmäärittelyä, hyväksymiskriteerien kirjoittamista ja ensemble-työskentelyä useille organisaatioille ja toimii itse vaihtelevissa rooleissa tekoälyavusteisessa kehityksessä
* Määrittely, kuvat ja protot syntyvät rinnakkain samasta wikistä: kuva ja proto ovat näkymiä, joiden läpikäynti kasvattaa wikiä
* Kurssin tuotokset – Event Storming -seinät, kontekstikartta, wiki kuvineen, story map, ensimmäisen siivun proto ja Gherkin-skenaariot – jäävät tilaajalle jatkotyön pohjaksi
* Koulutussisältö vastaa parasta saatavilla olevaa tietämystä uudistuen, ja saat käyttöösi myös koulutusmateriaalien uudet versiot päivittääksesi omaa osaamistasi koulutuksen jälkeen
* Koulutusmateriaalit on lisensoitu Creative Commons Nimeä-EiKaupallinen-JaaSamoin 4.0 (CC BY-NC-SA 4.0) -lisenssillä. Tämä mahdollistaa oppien jälkikäytön ja tiedon jakamisen osallistujien organisaatioissa ei-kaupallisesti, kun tekijä mainitaan ja muokatut versiot jaetaan samalla lisenssillä
