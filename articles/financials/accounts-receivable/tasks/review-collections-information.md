--- 
title: "Sissenõuete teabe ülevaatamine"
description: "Selles protseduuris selgitatakse sissenõuete teabe ülevaatamist ning ka mitmesuguseid häälestussuvandeid ja sissenõudekandeid."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: eb0866505702ec5d047b6c8f3f0657aae787bedc
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="review-collections-information"></a>Sissenõuete teabe ülevaatamine

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Selles protseduuris selgitatakse sissenõuete teabe ülevaatamist ning ka mitmesuguseid häälestussuvandeid ja sissenõudekandeid. See protsess kasutab demoettevõtte USMF-i andmeid.


## <a name="create-customer-pools"></a>Kliendikaustade loomine
1. Avage Krediit ja sissenõuded > Seadistus > Kliendikaustad.
    * Sellel lehel saate häälestada kliendikaustad, mis on päringud, mis määravad kliendikontode grupi, mida saab sissenõuete või aegumisprotsesside jaoks kuvada ja hallata. Kliendikaustadega saate filtreerida teavet sissenõuete loendilehel ja seotud loendilehtedel. Kliendikaustadega saate ka filtreerida kliendikontosid, mis kaasatakse aegumise hetktõmmiste loomisel.  
    * Kliendikaustadega saate filtreerida kliendikontosid, mis kaasatakse aegumise hetktõmmiste loomisel.  
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Kausta ID.
4. Sisestage väärtus väljale Kausta kirjeldus.
5. Klõpsake käsku Vali kausta kriteeriumid.
6. Sisestage väärtus väljale Kriteeriumid.
7. Klõpsake nuppu OK.
8. Klõpsake suvandit Kliendikausta eelvaade.

## <a name="create-collections-agents"></a>Inkassaatorite loomine
1. Tehke valik Krediit ja sissenõuded > Seadistus > Inkassaatorid.
    * Sellel lehel saate määrata töötajaid inkassaatoriteks ja soovi korral määrata neile kliendikaustu. Inkassaator on isik, kes teeb koostööd klientidega, et makseid kogutaks õigeaegselt.  
    * Sellel lehel häälestatud inkassaatorid lisatakse automaatselt sissenõuete töörühma. Kui lehe Müügireskontro parameetrid väljal Töörühm on valitud töörühm, lisatakse inkassaatorid sellesse töörühma. Kui töörühm pole valitud, luuakse automaatselt uus töörühm nimega Sissenõuded ja inkassaatorid lisatakse sellesse rühma.  
2. Klõpsake valikut Uus.
3. Klõpsake vahekaarti Lisa.
4. Klõpsake valikut Sule.
5. Klõpsake vahekaarti Lisa.
6. Märkige loendis valitud rida.
7. Klõpsake väljal Kausta ID otsingu avamiseks ripploendi nuppu.
8. Otsige loendist ja valige soovitud kirje.
9. Märkige või tühjendage ruut Vaikekaust.
    * Tehke see valik kõigi kliendikaustade lisamiseks valitud inkassaatori filtriloenditesse. Kui seda valikut pole tehtud, on filtriloendites saadaval ainult sellele inkassaatorile määratud kliendikaustad.  

## <a name="create-aging-period-definition"></a>Aegumisperioodi määratluse loomine
1. Tehke valik Krediit ja sissenõuded > Seadistus > Aegumisperioodi määratlused.
    * Saate kasutada aegumisperioodi definitsioone kliendi- ja hankijakontode vanuse analüüsiks teie sisestatavate andmete alusel. Iga aegumisperioodi definitsiooni jaoks seadistatud aegumisperiood vastab analüüsi tegemise käigus loendilehel, vormis või aruandes olevale veerule.  
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Aegumisperioodi määratlus.
4. Sisestage väljale Kirjeldus soovitud väärtus.
    * Määrake perioodi nimi, ühik ja iga aegumisperioodi intervalli aegumisperioodi määratlusse kaasamiseks. Nulliga (0) rida väljal Üksus näitab analüüsi käivitamiskuupäeva. Enne nulli olevatel ridadel on väljal Ühik vaikekirjeks –1 ning peale nulli olevatel on 1, kuid seda saab muuta.  Kasutage nuppe Üles ja Alla ridade ümberkorraldamiseks. 0 (null)-rida ei saa muuta.  
    * Asetage kursor sinna, kuhu soovite sisestada uue rea, ning klõpsake käsku Lisa.  
    * Valige sissenõuete vormil ja loendilehel aegumisperioodi tähistav indikaator. Näiteks võite valida praegusele perioodile rohelise indikaatori, viimase 30 päeva pikkusele perioodile kollase indikaatori ja viimase 90 päeva pikkusele perioodile punase indikaatori.  
    * Valige aegumisperioodi määratluse printimissuund. See valik määrab veergude kuvamise järjekorra kliendi või hankija aegumisaruandes.  Edasi: veerud prinditakse samas järjekorras, milles pealkirjad tabelis kuvatakse, alustades ülemisest reast.  Tagasi: veerud prinditakse vastupidises järjekorras sellele, milles pealkirjad tabelis kuvatakse, alustades alumisest reast.    

## <a name="setup-collections-parameters"></a>Sissenõuete parameetrite seadistamine
1. Tehke valik Krediit ja sissenõuded > Seadistus > Ostureskontro parameetrid.
2. Klõpsake vahekaarti Sissenõuded.
3. Laiendage või ahendage jaotist Sissenõuete vaikesätted.
    * Valige aegumisperioodi definitsioon aegumise vaikehetktõmmise jaoks, mida kasutatakse sissenõuete vormis.  
    * Valige töörühm, millesse inkassaatorid vormil Inkassaator määratakse. Loendis kuvatakse ainult töörühmad, mille tüüp on Sissenõuded.  
4. Laiendage või ahendage jaotist Mahakandmine.
    * Valige igapäevaste pearaamatu töölehtede jaoks häälestatud töölehe nimi, mida kasutada kande mahakandmisel vormil Sissenõuded või seotud loendilehtedel.  
    * Valige põhjuse vaikekood, mida kasutada mahakandmise kannete loomisel vormil Sissenõuded või seotud loendilehtedel.  
    * Tehke see valik, et luua eraldi töölehe rida käibemakssummade jaoks mahakandmise kannete loomisel, kasutades lehte Sissenõuded või seotud loendilehti. Selle valiku puhul saate hõlpsasti jälgida käibemaksusummasid, mis on seotud mahakandmise kannetega. Saate jälgida käibemaksusummasid eraldi, et kohandada hõlpsamini vastava perioodi käibemaksukohust.  
5. Laiendage või ahendage jaotist Meilimall.
    * Valige meilimall, mida kasutada meili saatmisel, kasutades valikut Meil > Kontakti kanded vormil Sissenõuded.  
    * Valige meilimall, mida kasutada vormi Sissenõuded valiku Meil > Väljavõte kontaktile kaudu kliendi väljavõtte saatmisel meilisõnumi manuses.  
    * Valige meilimall, mida kasutada meilisõnumi saatmisel vormi Sissenõuded valiku Meil > Müügiesindaja kanded abil.  

## <a name="age-customer-balance"></a>Kliendi saldo aegunuks märkimine
1. Tehke valik Krediit ja sissenõuded > Perioodilised ülesanded > Klientide saldode aegumine.
    * Valige aegumisperioodi definitsioon. Aegumise hetktõmmise töötlemine märgib kanded aegunuks vastavalt valitud aegumisperioodi määratluses määratletud aegumisperioodidele.  
    * Valige kliendikaust või jätke see väli tühjaks aegumise hetktõmmise loomiseks kõigile klientidele. Kliendikausta valimisel rakendatakse aegumise hetktõmmise töötlemist ainult kliendikausta kuuluvatele kliendikontodele. Valitud kliendi kausta tüüp peab olema Aegumise hetktõmmis.  
    * Valige kuupäeva tüüp, millel aegumise hetktõmmis põhineb.    Kande kuupäev: iga kande aegumine põhineb selle kande kuupäeval.    Tähtaeg: iga kande aegumine põhineb selle tähtajal.    Dokumendi kuupäev: iga kande aegumine põhineb selle dokumendi kuupäeval.  
    * Valige kuupäev, mida kasutada aegumise hetktõmmise praeguse kuupäevana. Aegumisperioodid arvutatakse selle kuupäeva alusel.    Tänane kuupäev: kasutage süsteemi kuupäeva. Tehke see valik, kui töötlemine on seadistatud toimuma korduva partiina. Kui kasutate seda kuupäeva, saab korduvat partiid perioodiliselt käitada ja kasutatakse süsteemi kuupäeva sellel ajal.    Valitud kuupäev: kasutage enda määratud kuupäeva. Selle valiku korral sisestage aegumiskuupäev.  
2. Klõpsake nuppu OK.

## <a name="view-aged-customer-balances"></a>Aegunud kliendi saldode vaatamine
1. Tehke valik Krediit ja sissenõuded > Sissenõuded > Aegunud saldod.
    * Kasutage loendilehte kliendisaldode ja aegunud summade vaatamiseks aegumisperioodi järgi. See teave salvestatakse aegumise hetktõmmisesse. Aegumisperioodid on määratud kasutatava aegumisperioodi definitsiooniga. Aegumisperioodi definitsioon võetakse kliendikaustast, kui see on kaustale määratletud. Kui kliendikaustal ei ole aegumisperioodi definitsiooni, kasutatakse vormis Müügireskontro parameetrid määratud vaikimisi aegumisperioodi definitsiooni.  
2. Laiendage kiirinfo Kontakt.
    * Kliendi sissenõuete kontakt.  
    * Kliendi vaikemüüja.  
3. Laiendage kiirinfo Krediidilimiit.
    * Krediiditeabe kiirinfo abiga saate vaadata kliendi krediidilimiidi ja praeguse saldo teavet.  

## <a name="view-customer-collections-details"></a>Kliendi sissenõuete üksikasjade kuvamine
1. Klõpsake loendis valitud real olevat linki.
2. Laiendage kiirinfot Aadress.
3. Laiendage kiirinfot Kontakt.
4. Laiendage kiirinfo Ajaline jaotus.
5. Laiendage kiirinfo Krediidilimiit.
6. Klõpsake toimingupaanil suvandit Sissenõudmine.
    * Uuendage kliendi aegumise hetktõmmist, kasutades tänast kuupäeva aegumiskuupäevana, millega kande kuupäevi võrreldakse. Kui aegumise hetktõmmis hõlmab mitme juriidilise isiku teavet, hõlmab uuendatud aegumise hetktõmmis samade juriidiliste isikute teavet. Summad talletatakse aegumise hetktõmmise uuendamise ajal sisselogitud juriidilise isiku arvestusvaluutas.  
    * Valige aegumisperioodi definitsioon. Vaikimisi kuvatakse kliendi aegumise hetktõmmisega seostatud aegumisperioodi määratlus. Aegumisperioodi määratlus juhib aegumisperioode ja summasid, mis on näidatud kiirinfos Aegunud saldod ja Krediiditeave.  
    * Avage menüü, mis sisaldab järgmisi elemente: Ettevõte – aegunud saldode summade ja krediiditeabe kiirinfo kuvamine juriidilise isiku arvestusvaluutas.    Klient – aegunud saldode ja krediiditeabe kiirinfo kuvamine kliendi arvestusvaluutas.  
    * Valige kliendi aegumise hetktõmmises üks või mitu juriidilist isikut, kelle teavet soovite vaadata. Loendis olevad juriidilised isikud olid aegumise hetktõmmise loomisel valitud.  
    * Vaadake kliendi väljavõtet Microsoft Exceli vormingus. Saate valida kannete vahemiku alguskuupäeva, mis kaasatakse väljavõttesse, ja otsustada, kas soovite kaasata ainult avatud kanded või nii avatud kui ka tasakaalustatud kanded. Kui aegumise hetktõmmis hõlmab mitme juriidilise isiku teavet, kaasatakse kõigi juriidiliste isikute kanded.  
    * Avage vorm Dokumendid, kus saate luua või redigeerida dokumente või märkmeid.  
7. Klõpsake toimingupaanil valikut Suhtlus.
    * Avage Outlook, kus saate saata meilisõnumi väljal Kontakt määratud kontaktile. Kui sissenõuete kontakt määramata, kasutatakse kliendi konto peamist aadressi. Kui esmane kontakt ei ole määratud, saadetakse meilisõnumid esimesele aadressile vormil Kontaktid. Valitud kanded kaasatakse manustena. Manus on Exceli vormingus ja hõlmab kolme töölehte. Kliendi kontaktidele saadetavate sõnumite meilimalli saate määrata vormil Müügireskontro parameetrid.  
    * Nupp ei ole saadaval, kui sellel vormil valitud kontakti meiliaadress on häälestamata.  
    * Valmistage väljavõte ette ja avage Outlook, kus saate väljal Kontakt määratud aadressile saata meilisõnumi, mille manuses on väljavõte. Kui sissenõuete kontakt määramata, kasutatakse kliendi konto peamist aadressi. Kui esmane kontakt ei ole määratud, saadetakse meilisõnumid esimesele aadressile vormil Kontaktid.  
    * Nupp ei ole saadaval, kui sellel vormil valitud kontakti meiliaadress on häälestamata.  
    * Avage Outlook, kus saate saata meilisõnumi kliendile määratud müügigrupi müügiesindajaks määratud töötajale. Kui kanded on valitud, kaasatakse need manustena. Manus on Exceli vormingus ja hõlmab kaht töölehte. Müüjatele saadetavate sõnumite meilimalli saate määrata vormil Müügireskontro parameetrid.  
    * Nupp ei ole saadaval, kui sellel vormil kuvatud müüja meiliaadress on häälestamata.  
    * Saate kuvada kliendi kanded ja teha nendega seotud toiminguid. Tsentraliseeritud maksete kasutamisel kaasatakse kõigi kliendi aegumise hetktõmmises olevate juriidiliste isikute teave. Juriidilise isiku teabe piiramiseks kasutage tegumiriba grupis Vali olevat nuppu Ettevõte.  
    * Muutke valitud kannete sissenõudeolekut.    Vaidlustamata: kande puhul ei ole sissenõudetegevust toimunud.    Vaidlustatud: klient on teid teavitanud kandega seotud probleemist.    Lubatud maksta: klient on nõustunud maksma kandesumma.    Lahendatud: kõik kande probleemid on lahendatud ja mingeid täiendavaid sissenõudmistegevusi ei ole vaja.  
    * Avage menüü ja valige üks järgmistest elementidest, et määrata, millised kanded sellel lehel kuvatakse: Avatud – kuvatakse ainult tasakaalustamata kanded.    Avatud ja suletud – kuvatakse kõik kanded, nii tasakaalustatud kui tasakaalustamata.  
    * Töödelge valitud makset ebapiisavate vahendite (NSF) maksena.    See nupp on saadaval ainult siis, kui valitud kanne on maksete töölehele sisestatud makse (arveta kreeditsaldo), kandele on määratud pangakonto ja makset ei ole varem tühistatud.  
    * Kandke valitud kanded maha.  
    * Märkige valitud kanded üksteisega tasakaalustamiseks.  
    * Avage vorm Algne dokument, kus saate vaadata ja printida valitud kande dokumendi.  
    * Avage menüü, mis sisaldab järgmisi elemente: Võlanõuded – ainult vormis Võlanõuded loodud tegevuste kuvamine.    Kõik – kõigi selle kliendi tegevuste kuvamine olenemata nende loomiskohast.  
    * Avage menüü, mis sisaldab järgmisi elemente: Avatud – ainult nende tegevuste kuvamine, mis ei ole suletud.    Avatud ja suletud – kõigi tegevuste kuvamine olenemata nende olekust.  
    * Valige kliendile määratud sissenõuete juhtum või jätke väli tühjaks. Kui juhtum on valitud, kuvatakse vormil ainult selle juhtumiga seostatud kanded ja tegevused.  
8. Klõpsake käsku Kuva loend.
    * Valige kliendi konto või nõustuge vaikesisestusega. Vaikimisi on see loendilehel või vormil, millelt avasite selle vormi, valitud kliendi konto. Kui avasite vormi loendilehelt, on loendis kliendid, kes on kaasatud loendilehel kasutatavasse kliendikausta.  


