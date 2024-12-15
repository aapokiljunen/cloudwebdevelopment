---
title: "Lopputyön raportti"
layout: default
---

[Lopputyön sivut](https://aapokiljunen.github.io/helsinginkadut)

## Yleistä höpinää
Lopputyössäni pelataan katujen tunnistuspeliä vanhemmista ja uudemmista Helsingin rakennuskuvista. Peli näyttää kuvan, pelaajan pitäisi osata kirjoittaa millä kadulla ollaan. Kymmenen vaihtuvaa kuvaa (yhteensä Finnan palvelusta löytyy 2500 kuvaa, eli pelattavaa riittää), joista pitäisi tunnistaa millä kadulla seikkaillaan. 

Työ nyt ei ehkä ihan täysin vastaa tehtävänantoa "käytännöllisestä sivustosta, jossa olisi hyödyllistä tietoa". Mutta, noh, ehkä tehtävänanto oli sen verran vapaamuotoinen, ettei nyt varsinaisesti sitä vastaankaan ole. Löytyy sieltä myös Firebase ennätystulosten tallentamiseen. Joskus aiemmin pyörittelin vähän päässäni ideaa samansuuntaista pelistä, mutta silloin se ei sopinut tätäkään vähää tehtävänantoon, mutta nyt onneksi pääsin toteuttamaan, aina kiva kuitenkint tehdä joku sinällään itseä kiinnostava projekti. Pelistä tuli kyllä huomattavasti vaikeampi kuin ajattelin tekemään aloittaessani, sillä en nyt lopulta osannut ja jaksanut alkaa katuosotteita yhdistelemään kaupunginosiin, joita oli alunperin tarkoitus arvoitella, joten haastetta riittää.

Eikä haastetta yhtään vähennä se, että arviolta noin 5-10% kadunnimistä on jollain tavalla väärin parsittu, kun nuokin päädyin vaihtelevilla tavoilla muotoilluista kuvien otsikoista parsimaan kasaan, niin virheitä kyllä riittää.

## Ulkoasu ja responsiivisuus
React ja Material UI tuottavat mukavasti automaattisesti varsin responsiivista koodia. Isoin haaste tässä sivustossa oli tuon arvuuttelukuvan koon määrittelemissä. Kuvan haluaisi olevan mahdollisimman iso, mutta toisaalta sivu saisi näkyä kokonaisuutena sivulla. Vaikka kuvan koko sinällään suhteellisesti vaihtuukin, ihan kaikkein pienemmillä läppärin näytöillä taitaa muut elementit kasvaa suhteellisesti niin isoksi, että yläreunan laskuri (tai lähetä-nappi alareunassa) jää piiloon. Peliä kyllä pystyy pelaamaan enterilläkin, että sinällään ongelma on pienehkö ja olisi hiottavissa pois jos aikaa ja jaksamista olisi.

Kännykällä peli toimii yllättävänkin mukavasti ja asettelussa alusta asti pidin vähän mielessäkin, että elementit asettuvat pystysuuntaisesti, jolloin kännykällä peli asettuu hyvin pelattavaksi.

![pieni_läppäri](/finalassignment/pics/pieniff.png)
*Oikein pienellä näytöllä jotkut elementit jäävät piiloon ylä- tai alareunasta* 

## Toimivuus uusimmilla selaimilla
Tarkastin sivuston toiminnan Firefoxilla, Edgellä, Chromella sekä Firefoxin ja Chromen kännykkäversioilla. Kaikilla muilla selaimilla sivusto toimii moitteetta, mutta jostain syystä Chromen kännykkäselain sotkee yläpalkin halutessaan rivittää tekstin. Applea en nyt tähän hätään saanut käsiini.

![android_firefox](/finalassignment/pics/androidfire.jpg)
*Firefoxilla peli toimii puhelimella erinomaisesti*

![android_chrome](/finalassignment/pics/androidchrome.jpg)
*Chrome sotkee jostain syystä yläreunan navigointivalikon rivittämällä tekstin*

## Latausajat
Sivuston nopeus on tietysti pitkälti kiinni rajapintojen nopeudesta. Erityisesti Finnan yhteyden nopeus on merkitsevä tässä tapauksessa: uutta peliä aloittaessa tehdään 10 erillistä peräkkäistä rest-kyselyä (joo, ei ihan tuotantokelpoinen sovellus ole :D) Finnan palveluun haettaessa 10 satunnaista kuvaa, ja tuo ottaa sen ehkä reilun sekunnin, erityisesti yhditettynä samalla tehtävään ison kuvan lataukseen, on pelin aloittaminen ehkä aavistuksen hidas nykystandardeille. Toisaalta sitten pelatessa ei viivettä ole juurikaan kun enää haetaan vain suoraan kuva osoitteella. Ainakin testaillessa on heidän palvelunsa ollut koko ajan hyvin nopea. 

Toinen pullonkaula tulee Firebasen kanssa, josta haetaan ennätystuloksia ja pelaajan aiempia tuloksia. Kysely on luonteeltaan vielä sortBy (toki indeksoitu, että sinällään ei ehkä ihan niin iso asia). Google ei selvästikään ihan kauhean paljon painoarvoa anna testipalvelimille, kun tuokin ottaa oman aikansa (~puolisen sekuntia).

## Loppusanat
Teknisesti sivusto pienistä puutteista huolimatta toimii varsin mukavasti suurimmalla osalla laitteista ja asetuksista ja tuollainen perusmallinen Material UI sopii pelin luonteeseen ihan mukavasti ja sitä myöten sivusto näyttääkin ihan kivalta (toki hiottavaakin olisi). Teknisesti ohjelma ei nyt oikeasti olisi tuotantokelpoinen (sen nojatessa käytännössä täysin Finnan palvelusta ladattaviin kuviin), mutta tällaiseksi koulutyöksi toimiva. Mikään ohjelmointikurssihan tämä ei ollut ja aika paljon sen myötä tuli chatgpt:tä hyödynnettyä koodauksen tukena.


[Lopputyön sivut](https://aapokiljunen.github.io/helsinginkadut)
[GitHub-sivut](https://github.com/aapokiljunen/helsinginkadut)



[Palaa etusivulle](../index.md)