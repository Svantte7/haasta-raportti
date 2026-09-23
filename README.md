# Haasta raportti · UPM

## Projektikuvaus ja prosessi

**Mitä rakensin?**  
Rakensin **Haasta raportti** -selainprototyypin AIEquityReportsille. Käyttäjä voi muuttaa UPM-raportin liikevaihto-, kannattavuus- ja arvostuskerroinoletuksia. Laskennallinen osakearvo, vertailukuvaaja ja muutoksen selitys päivittyvät heti. Mukana ovat kolme skenaariota, lähteet ja näkyvät laskentaoletukset. Laskuri toimii myös itsenäisenä HTML-tiedostona.

[Kokeile demoa](https://haasta-upm-raportti.athirityjt.chatgpt.site/) · [Julkinen lähdekoodi ja käyttöohje](https://github.com/Svantte7/haasta-raportti)

**Kenelle siitä olisi hyötyä?**  
Raporttia lukevalle sijoittajalle, joka haluaa ymmärtää, mistä arvostus riippuu. Palvelulle se voisi toimia kokeiltavana esimerkkinä ennen raportin ostamista.

**Miksi valitsin tämän ongelman?**  
Raportissa oli jo skenaarioita, mutta niiden oletusten vaikutusta oli vaikea kokeilla itse. Halusin tehdä oletusten ja johtopäätöksen yhteyden näkyväksi.

**Mitä AI-työkaluja käytin?**  
Käytin Codexia suunnitteluun, koodiin ja selitysteksteihin. Rinnakkaiset AI-agentit tarkistivat raportin lähdelukuja ja arvioivat laskentamallia. Selainohjauksella testasin käyttöliittymää työpöydällä ja puhelimen kokoisissa näkymissä. Laskurin käytön aikana ei kutsuta AI-palvelua.

**Mitä tekisin kahdessa lisätunnissa?**  
Testaisin demoa muutamalla käyttäjällä, lisäisin omien skenaarioiden tallennuksen ja vertailun sekä toisen yhtiön tarkistaakseni ratkaisun yleistettävyyden.

**Olennainen tekoälylle annettu ohje:**  
> Käyttäjän muutokset pitää erottaa raportin alkuperäisistä luvuista. Kyse on läpinäkyvästä yksinkertaistetusta mallista, ei uudesta virallisesta tavoitehinnasta.

**Hylätty versio ja syy:**  
Hylkäsin alkuversion 527,3 miljoonan osakkeen mallioletuksen, koska sitä ei ollut vahvistettu lähteestä. Käytin raportin ilmoittamaa pyöristettyä 527 miljoonaa ja näytin laskurin sekä raportin väliset senttierot avoimesti.

**Todellinen ajankäyttö:**  
Prototyyppi valmistui **30 minuutissa 29 sekunnissa**, 22.9.2026 klo 14.22.24–14.52.53.

---

[Avaa verkkoversio](https://haasta-upm-raportti.athirityjt.chatgpt.site). Verkkoversio on yksityinen ja vaatii omalle tilillesi kirjautumisen. Muille jaettavaksi sopii alla kuvattu HTML-tiedosto.

Avaa `haasta-raportti.html` tavallisessa selaimessa. Tiedosto sisältää koko demon. Sen voi lähettää toiselle käyttäjälle sellaisenaan; laskuri ei tarvitse asennusta, tunnuksia, verkkoyhteyttä tai maksullista AI-palvelua. Ulkoisten lähdelinkkien avaaminen tarvitsee verkkoyhteyden.

## Kokeile näin

1. Valitse **Heikko**, **Perus** tai **Vahva**.
2. Muuta liikevaihtoa, EBITDA-kannattavuutta tai EV/EBITDA-kerrointa. Voit vetää säädintä, käyttää nuolinäppäimiä tai kirjoittaa lukukenttään. Desimaalipilkku toimii.
3. Seuraa osakearvoa, prosenttieroa ja kuvaajaa. **Mistä muutos johtuu?** erittelee muutoksen euroina.
4. Avaa sivun lopusta laskentaoletukset ja lähteet. **Palauta perus** palauttaa lähtötilanteen.

Oma muutos merkitään omaksi skenaarioksi. Alkuperäisen raportin luvut pysyvät näkyvissä vertailuna. Puhelimessa tulos näkyy myös alareunan palkissa. Sivun uudelleenlataus palauttaa perusskenaarion; skenaarioita ei tallenneta pysyvästi.

## Laskennan rajaus

Lähde on [AI Equity Reportsin UPM-raportti, 1.9.2026](https://www.aiequityreports.com/reports/upm-equity-report.html) ja sen [maksuton PDF](https://files.aiequityreports.com/reports/pdfs/UPMKymmeneOyj_01092026.pdf).

Kaava on `(liikevaihto × marginaali × kerroin − 2 741 − 418) / 527`. Rahamäärät ovat miljoonia euroja, marginaali desimaalina ja osakemäärä miljoonia osakkeita. Tulos on euroa osakkeelta.

Osakemäärä **527 miljoonaa** on raportin sivulla 55 julkaistu pyöristetty luku. Myös marginaali ja kerroin ovat näkyvät, pyöristetyt raporttiluvut. Siksi laskurin perusarvo **27,81 €** eroaa raportin skenaarioarvosta **27,77 €**. Eroa ei piiloteta. Raportin **24,70 €:n 12 kuukauden tavoitehinta** perustuu eri laskentaan ja erotetaan skenaarioarvoista.

Vertailukurssi **24,06 €** on raportin päiväykseltä, ei reaaliaikainen kurssi. Velka, oikaisut ja osakemäärä pidetään vakioina. Malli ei sisällä erillistä kassavirtalaskentaa, diskonttausta, osinkoja tai todennäköisyyspainoja. Säädinrajat ovat demon valintoja, eivät ennustevälejä. Kyse ei ole uudesta virallisesta tavoitehinnasta tai henkilökohtaisesta sijoitussuosituksesta.

## Tarkistus

- Raportin keskeiset PDF-sivut 36, 44, 48 ja 55 tarkistettiin.
- Laskennasta tarkistettiin kaikki **623 781** sallittua säädinyhdistelmää: äärelliset ja positiiviset tulokset, oletusten johdonmukainen vaikutus sekä muutoksen erittelyn täsmääminen sentilleen.
- Selaimessa testattiin esiasetukset, kaikki kolme säädintä, numerokentät, desimaalipilkku, virhesyötteet, palautus, avattavat tiedot, näppäimistökäyttö sekä työpöytä- ja puhelinnäkymät (390 ja 320 pikseliä).
- Laskurin tarkistusarvot: heikko **12,93 €**, perus **27,81 €**, vahva **37,84 €**. Rajayhdistelmät **1,60 €** ja **74,18 €**.
- Käyttöliittymä testattiin paikallisessa selain-esikatselussa. Suoran tiedosto-osoitteen avaaminen ei ollut testiympäristössä sallittu. Tiedostossa ei ole ulkoisia ohjelmisto- tai kirjasinriippuvuuksia.

## AI:n käyttö

AI:ta käytettiin raporttilukujen jäsentämiseen, selitysten luonnosteluun, toteutukseen ja tarkistuksiin. Demon selitykset ovat laskennasta päivittyviä ennalta laadittuja tekstejä. Käytön aikana ei kutsuta AI-palvelua eikä käyttäjän oletuksia lähetetä palvelimelle.

Tämä on itsenäinen prototyyppi. AIEquityReports.comin tuotantoympäristöä ei muutettu.

Toteutus alkoi 22.9.2026 klo 14.22.24 ja valmistui noin klo 14.52 (Europe/Helsinki). Kokonaisaika oli noin 30 minuuttia annetusta 60 minuutista, mukaan lukien lähdetarkistus, toteutus, testaus ja julkaisu.
