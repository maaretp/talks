# Nykypäivän testitapaukset

Yliopistolla testausta opettaessani pari vuosikymmentä sitten materiaaleissani oli esimerkkejä testitapauksista. Kun sitten pari vuotta myöhemmin palkkasin kurssilla opettamani ammattilaisen, heidän palautteensa juurtui yhtenä uraani ja ymmärrystä määrittävänä hetkenä:

"Kiva kuulla että teemme tässä testausta järkevästi, eikä niinkuin opetit silloin kurssilla"

Kurssilla opettamani tapa tuotti suuria määriä dokumentaatiota, ja dokumentaation tuottaminen oli aikaa pois hyvän testauksen tekemisestä. Kun yhdessä viimeaikaisessa projektissa perin 1500 testitapausta, laskin että niiden pikainen lukeminen läpi olisi 11 työpäivän investointi. Päätimme laittaa ne sivuun, ja arvioida niiden hyödyllisyyttä kysymysten noustessa. Emme löytäneet tarvitsemiamme vastauksia niistä hauilla seuraavan vuoden aikana. 

Vuosikymmenet ovat opettaneet minulle kompromissin, jossa testitapausten dokumentoinnista on hyötyä. Tämä tapa eroaa kuitenkin projektien käytänteistä, ja siksi käytänkin nimitystä *nykypäivän testitapaukset*. Ne ovat otsikoita toisteisille testaustehtäville, tai vaiheittaista automaation rakentamista.

Käydään siis läpi testauksen tehtävät ja testitapaukset Jira + Jira XRay -testihallintasovelluksen kontekstissa, ja katsotaan mitä nykypäivän testitapaukset testien hallinnan käytäntönä voisi tarkoittaa. Keskustelu on erityisen ajankohtainen generatiivisen tekoälyn tuottaessa meille luettavaa - enemmän kuin 11 työpäivän verran.





Muistiinpanoja:

Nykypäivän testitapaukset
1) pelkkä otsikko monta kertaa tehtävästä testaustehtävästä - jotain jolle on tarpeen pitää varattuna aikaa, joskus puolituntinen joskus puoliviikkoinen, mutta jotain sellaista joka toimii karkeana jäsennyksenä kun miettii että mitäs pitäisi testata tai tuli testattua
2) Todo->Koodiksi testiautomaatiossa. Testitapaukset voivat myös ideavaiheessa elää vain testikoodin yhteydessä. 

Kun kuvaan vanhempia opetuksia siitä mitä on testitapaus, se on joko 
1) Charter - enempi kertakäyttöinen kuvaus tutkivan testauksen tueksi
2) Otsikko, kuvaus, askeleet, odotetut tulokset vaihtelevalle tasolle dokumentoituna. Usein kirjoitettu enemmän todisteeksi testauksesta kuin uudelleenkäytettäväksi tulevissa testauksissa. 