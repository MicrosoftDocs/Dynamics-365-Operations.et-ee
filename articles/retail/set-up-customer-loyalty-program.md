---
title: Püsikliendi ülevaade
description: Selles teemas kirjeldatakse rakenduse Microsoft Dynamics 365 for Retail püsikliendi võimalusi ja vastavaid seadistusetappe, mis aitavad jaemüüjal hõlpsasti oma püsikliendiprogrammiga algust teha.
author: scott-tucker
manager: AnnBe
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailLoyaltyPrograms, RetailPriceDiscGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16201
ms.assetid: f79559d2-bc2d-4f0b-a938-e7a61524ed80
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 94f8cf5b5753c530c42327e251a2102b876c1c8a
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606868"
---
# <a name="loyalty-overview"></a>Püsikliendi ülevaade

[!include [banner](includes/banner.md)]

Püsikliendiprogrammid aitavad suurendada klientide lojaalsust, premeerides kliente teie Retaileri kaubamärgiga suhtlemise eest. Rakenduses Microsoft Dynamics 365 for Retail saate seadistada lihtsaid või keerulisi püsikliendiprogramme, mis kehtivad kõikide teie juriidiliste isikute kõikides jaemüügikanalites. Selles teemas kirjeldatakse rakenduse Microsoft Dynamics 365 for Retail püsikliendi võimalusi ja vastavaid seadistusetappe, mis aitavad jaemüüjal hõlpsasti oma püsikliendiprogrammiga algust teha.

Saate seadistada püsikliendiprogrammi nii, et see hõlmaks järgmisi valikuid.

- Seadistage mitu püsikliendiprogrammides pakutavat preemiate tüüpi ja jälgige osalust püsikliendiprogrammides.
- Seadistage püsikliendiprogrammid, mis näitavad erinevaid pakutavaid preemiaid. Saate kaasata püsikliendiprogrammi järke, et pakkuda lisaimpulssi ja suuremaid preemiaid klientidele, kes ostavad sagedamini või kes kulutavad teie poodides rohkem raha.
- Määrake teenimisreeglid, et panna paika tegevused, mida klient peab preemia saamiseks tegema. Samuti saate määrata lunastamisreeglid, et panna paika, millal ja kuidas klient preemia lunastada saab.
- Väljastage kliendikaarte mis tahes teie püsikliendiprogrammis osalevast jaemüügikanalist ja siduge kliendikaardid vähemalt ühe püsikliendiprogrammiga, milles klient saab osaleda. Samuti saate kliendikirje kliendikaardiga siduda, et klient saaks püsikliendipunkte koguda mitmelt kaardilt ja neid lunastada.
- Kliendi andmete korrigeerimiseks või tema premeerimiseks saate kliendikaarte käsitsi kohandada või kandke püsikliendipreemiate saldo ühelt kaardilt teisele.

## <a name="setting-up-loyalty-programs"></a>Püsikliendiprogrammide seadistamine

Püsikliendifunktsiooni võimaldamiseks rakenduses Dynamics 365 for Retail peate seadistama mitu komponenti. Järgmisel joonisel on kujutatud püsikliendiprogrammi komponendid ja nende omavahelised seosed.

![Püsikliendiprogrammi seadistuse protsessivoog](./media/loyaltyprocess.gif "Püsikliendiprogrammi komponendid ja nende omavahelised seosed")

## <a name="loyalty-components"></a>Püsikliendiprogrammi komponendid

Järgmises tabelis kirjeldatakse kõiki komponente ja nende kasutuskohta püsikliendiprogrammi seadistamisel.

| Komponent                                        | Kirjeldus | Kus seda kasutatakse? |
|--------------------------------------------------|-------------|-----------------|
| Allahindluste seadistamine (eeltingimus)                  | Seadistage püsiklientidele pakutavad allahindlused. Näiteks saate teha 5-protsendise allahindluse kõigile rõivatoodetele. | Allahindlused tuleb lisada hinnagruppidele, enne kui need saab kaasata püsikliendiprogrammi. Hinnagrupid määratakse püsikliendiprogrammidele ja püsikliendijärkudele. |
| Hinnagruppide seadistamine (eeltingimus)               | Hinnagruppe kasutatakse jaetoodete hindade ja allahindluste loomiseks ning haldamiseks. Seadistage hinnagrupid, mis sisaldavad teie püsikliendiprogrammidele kehtivaid allahindlusi. | Hinnagrupid määratakse püsikliendiprogrammidele ja püsikliendiprogrammi järkudele. |
| Kanalite seadistamine (eeltingimus)                   | Jaemüügikanalid on püsikliendiprogrammides osalevad poed, nagu tavakauplus, e-pood või kõnekeskus. Peate seadistama jaemüügikanalid, enne kui saate neile püsikliendiprogrammid määrata. | Määrake püsikliendiprogrammile jaemüügikanalid, kui jaemüügikanal püsikliendiprogrammis osaleb. |
| Püsikliendi makseviisi seadistamine (eeltingimus) | Enne kui kliendikaarti saab registris kasutada ja boonuspunkte püsikliendiprogrammi osana lunastada, peate seadistama makseviisi. Peate püsikliendi makseviisi lisama ka jaemüügikanalile, enne kui kliendid saavad lunastada oma boonuspunkte toodete eest tasumiseks. | Seadistage püsikliendi makseviis ja määrake seejärel püsikliendiprogrammis osalevate jaemüügikanalite jaoks püsikliendi makseviis. |
| Kuupäevaintervallide seadistamine                            | Kuupäevaintervallid võimaldavad paindlikult püsikliendijärkudele kehtivat ajavahemikku seadistada. Kuupäevaintervallidega saate määrata, kui kaua saab klient ühes järgus olla või kui palju aega on kliendil järku kvalifitseerumise jaoks tegevuse lõpetamiseks. | Kuupäevaintervallid kehtivad ainult siis, kui kasutate püsikliendiprogrammides järkusid. Valige kuupäevaintervall, mis kehtib programmi järkudele, ja kuupäevavahemikud, mis kehtivad programmi järgu reeglitele. |
| Preemiapunktide seadistamine                             | Preemiapunktid on teatud tüüpi preemiad, mida klientidele pakute. Preemiapunktid võivad olla lunastatavad või mittelunastatavad. Lunastatavaid preemiapunkte saab vahetada toodete vastu. Mittelunastatavaid preemiapunkte kasutatakse jälgimiseks või kliendi edendamiseks püsikliendiprogrammi järgmisesse järku. | Preemiapunktidele viidatakse järgureeglites ja neid kasutatakse selleks, et klient kvalifitseeruks konkreetse järgu jaoks. Preemiapunktidele viidatakse ka püsikliendiskeemide teenimise ja lunastamise reeglites. Teenimisreeglites määrate preemiad, mille klient saab konkreetse tegevuse eest teenida. Lunastamisreeglites määrate preemia, mille klient lunastada saab. |
| Püsikliendiprogrammide seadistamine                          | Püsikliendiprogrammid on peamine püsikliendiüksus, mida pakute. Igale püsikliendiprogrammile võivad olla määratud püsikliendijärgud. Allahindlused ja hinnagrupid määratakse püsikliendiprogrammidele kas programmi tasemel või järgu tasemel. | Looge püsikliendiprogrammide jaoks püsikliendiskeeme. Määrake püsikliendiprogrammidele kliendikaardid ja kliendikaarte saab kliendile määrata. Jaemüügikanalid osalevad püsikliendiprogrammides, mida püsikliendiskeemidele määratakse. Kõik kliendikaardiga kliendid saavad osaleda kaardile määratud püsikliendiprogrammides. |
| Püsikliendijärkude ja järgureeglite seadistamine              | Püsikliendijärgud on valikulised tasemed, mille saate püsikliendiprogrammides määrata. Saate seadistada baasallahindlused ja -preemiad kõikidele püsikliendiprogrammis osalevatele klientidele ning täiendavad allahindlused ja preemiad programmis erinevatele tasemetele jõudvatele klientidele. Igale määratletud püsikliendijärgule saate seadistada reeglid, mis kliendi selle järgu jaoks kvalifitseerivad. Samuti saate määratleda, kui kauaks saavad kliendid jõutud järku jääda. | Püsikliendijärgud ja püsikliendijärgu reeglid on määratud püsikliendiprogrammis. Kui te püsikliendijärke ei määra, kvalifitseeruvad kõik püsikliendiprogrammis osalevad kliendid allahindlustele, mille püsikliendiprogrammi hinnagrupis määrate. Kui määrate püsikliendijärgud, saate seadistada püsikliendiskeemi püsikliendijärkudele teenimis- ja lunastamisreeglid. |
| Boonusskeemide häälestamine                           | Püsikliendiskeemid määravad teenimis- ja lunastamisreeglid, mis kehtivad valitud püsikliendiprogrammis. Määrake püsikliendiskeemile jaemüügikanalid, et panna paika, millised püsikliendiprogrammid, teenimis- ja lunastamisreeglid jaemüügipoele kehtivad. | Püsikliendiskeem määratakse püsikliendiprogrammile ja jaemüügikanalitele. Saate samale püsikliendiprogrammile määrata mitu püsikliendiskeemi ja mitmele jaemüügikanalile mitu püsikliendiskeemi. |
| Kliendikaartide häälestamine                             | Kliendikaart annab kaardiomanikule õiguse osaleda kaardile määratud püsikliendiprogrammides. Kliendikaarte saab väljastada anonüümselt või määrata need konkreetsele kliendile. Saate vaadata konkreetse kaardi kandeid ja kokkuvõtet boonuspunktidest, mis on kaardile kogunenud. Kliendikaarte saate väljastada ükskõik millisest jaemüügikanalist. Samuti saate kliendikaarti käsitsi korrigeerida, et tõsta klient uude järku, lisada boonuspunkte või kanda boonuspunktide saldo ühelt kaardilt teisele. | Määrake kliendikaardile püsikliendiprogramme. |

## <a name="loyalty-processes"></a>Püsikliendi protsessid

Järgmises tabelis kirjeldatakse protsesse, mida tuleb käitada, et saata püsikliendiprogrammi konfiguratsioonid ja andmed kauplustesse ning võtta kauplustest püsikliendikanded vastu.

| Protsessi nimi                         | Kirjeldus | Lehe nimi |
|--------------------------------------|-------------|-----------|
| 1050 (püsikliendi teave)           | Käitage seda protsessi, et saata püsikliendiprogrammi konfigureerimise andmed rakendusest Dynamics 365 for Retail jaekauplustesse. Soovitatav on ajastada see protsess sageli käivituma, et püsikliendiandmed edastataks kõigisse kauplustesse. | Jaotusgraafik |
| Boonusskeemide töötlemine              | Käitage seda protsessi, et seostada püsikliendiskeemid jaemüügikanalitega, millele püsikliendiskeem määratud on. Seda protsessi saab käitada pakktöötlusena. Peate seda protsessi käitama, kui muudate püsikliendi konfiguratsiooniandmeid, nagu püsikliendiskeemid, püsikliendiprogrammid või püsikliendi preemiapunktid. | Boonusskeemide töötlemine |
| Töötle võrguühenduseta boonuskandeid | Käitage seda protsessi, et värskendada kliendikaarte kaasamaks neisse võrguühenduseta töödeldud kandeid. See protsess rakendub ainult siis, kui lehel **Jaemüügi ühisparameetrid** on märgitud ruut **Teeni võrguühenduseta**, et preemiaid saaks teenida ka võrguühenduseta. | Töötle võrguühenduseta boonuskandeid |
| Uuenda kliendikaartide järke            | Käitage seda protsessi, et hinnata kliendi teenimisaktiivsust püsikliendiprogrammi järgureeglite suhtes ja värskendada kliendi järgu olekut. See protsess on nõutav ainult siis, kui muudate püsikliendiprogrammide järgureegleid ja soovite, et värskendatud reeglid kehtiksid tagasiulatuvalt juba väljastatud kliendikaartide puhul. Seda protsessi saab käitada pakktöötlusena või üksikute kaartide puhul. | Uuenda kliendikaartide järke |

## <a name="loyalty-enhancements"></a>Püsikliendiprogrammi täiustused

Rakendusel Retail on osana 2018. aasta oktoobri väljaandest uus püsikliendiprogrammi funktsioon. Iga uut täiustust kirjeldatakse allpool.

- Osana eelmiste väljaannete boonusskeemist said jaemüüjad luua erinevaid teenimis- ja lunastamisreegleid püsikliendijärkude järgi, et eristada ei järkude klientide preemiaid. Jaemüüjad saavad nüüd osana teenimis- ja lunastamisreeglitest kaasata "alluvused", et teatud kliendigrupp saaks olla olemasolavate järkude osa, kuid neid premeeritakse siiski teisiti. See väldib vajadust täiendavate järkude loomiseks.
    
    > [!NOTE]
    > Boonusskeemi teenimisreeglid on täiendavad. Näiteks kui loote reegli, et premeerida kullajärgu klienti 10 punktiga iga USA dollari eest ning loote ka reegli premeerida iga "veterani" staatusega klienti 5 punktiga iga USA dollari, siis veteran, kes on ka kullajärgu klient, teeniks iga 1 USA dollari eesti 15 punkti, kuna see klient kvalifitseerub mõlemale reeglile. Kuid kui veteran-klient ei ole küllajärgu liige, teenib ta iga dollari eest 5 punkti. Kanalites muudatuste kajastamiseks käivitage **Boonusskeemide töötlemise** ja **1050** (püsikliendi teabe) tööd.
    
    ![Alluvusel põhinev tulu](./media/Affiliation%20based%20earning.png "Alluvusel põhinevad tulud")

- Jaemüüjatel on sageli teatud kliendigrupile erihinnad, kellele nad ei soovi püsikliendiprogrammi rakendada. Näiteks hulgimüüjad või töötajad, kes saavad erihindu kuid mitte boonuspunkte. Tavaliselt kasutatakse sellistele kliendigruppidele erihindade tegemiseks "alluvusi". Selleks, et piirata tetud kliendigruppe või kliente boonuspunkte teenimast, saab jaemüüja määrata ühe või rohkem alluvust boonunusskeemi jaotises **Välistatud alluvused**. Sel viisil ei saa kliendid, kes on olemasolevad püsikliendid, kuid kuuluvad välistatud alluvuste alla, oma ostude eest boonuspunkte teenida. Kanalites muudatuste kajastamiseks käivitage **Boonusskeemide töötlemise** ja **1050** (püsikliendi teabe) tööd.

    ![Välistatud alluvused](./media/Excluded%20affiliations.png "Välistab alluvusi boonuspunkte teenimast")
    
- Jaemüüjad saavad luua kanalites kliendikaardi numbreid. Enne 2018. aasta oktoobri värskendust said jaemüüjad kliendikaartide loomiseks kasutada füüsilisi kliendikaarte ja kordumatut klienditeavet nt telefoninumbrit. Kliendikaartide automaatseks loomiseks kauplusteks lülitage kauplusega seotud funktsiooniprofiilil sisse **Kliendikaardi numbri loomine**. Võrgukanalites saavad jaemüüjad kasutada IssueLoyaltyCard API-t, et klientidele kliendikaarte väljastada. Jaemüüjad saavad sellele API-le anda kliendikaardi numbri, mida kasutatakse kliendikaardi loomiseks, või kasutab süsteem kliendikaardi numbriseeriat rakenduses Dynamics 365 for Retail. Kuid kui numbriseeriat ei ole ja jaemüüja ei sisesta API-t kutsudes kliendikaardi numbrit, kuvatakse tõrge.

    ![Loo kliendikaarti](./media/Generate%20loyalty%20card.png "Looge automaatselt kliendikaardi number")

- Teenitud ja lunastatud püsikliendipunktid salvestatakse nüüd iga kande ja müügitellimuse müügirea suhtes, et sama summa saaks täieliku või osalise tagastuse korral tagasi maksta või tagasi võtta. Lisaks annab punktide nägemine müügireal kõnekeskuse kasutajatele võimaluse vastata klientide küsimustele teenitud või lunastatud punktide kohta igal real. Enne seda muudatust kalkuleeriti boonuspunktid tagastustel alati ümber, mille tulemuseks oli originaalist erinev summa, kui teenimis- või lunastusreegleid oli muudetud ning kõnekeskuse kasutajatel ei olnud ülevaadet punktide jaotumisest. Punkte saab vaadata iga kliendikaardi **Kaardikannete** alt. Funktsiooni lubamiseks lülitage sisse konfiguratsioon **Sisesta boonuspunktid müügirea kohta** vahekaardil **Jaemüügi ühisparameetrid** \> **Üldine**.

    > [!NOTE]
    > Soovitame tungivalt see funktsioon sisse lülitada, et tagastuste korral saaks kliendile tagasi anda või temalt võtta õige arvu punkte.

- Jaemüüjad saavad nüüd määrata iga boonuspunkti üleandmisperioodi. Üleandmisperioodi konfiguratsioon määrab kestuse alates teenimiskuupäevast, pärast mida on boonuspunktid klientidele saadavad. Üleandmata punkte saab vaadata **Üleandmata punktide** veerus **Kliendikaartide** lehel. Lisaks saavad jaemüüjad määratleda maksimaalse püsikliendiprogrammi preemiapunktide määra ühe klinedikaardi kohta. Seda välja saab kasutada püsikliendiprogrammi pettuste vähendamiseks. Kui maksimaalne boonuspunktide summa on saavutatud, ei saa kasutaja rohkem punkte teenida. Jaemüüja võib otsustada sellised kaardid blokeerida, kuni nad on uurinud võimalikke pettuseid. Kui jaemüüja tuvastab pettuse, saab ta lisaks kliendikaardi blokeerimisele märkida ka kliendi blokeerituks. Selleks määrake **Blokeerida kliendi püsikliendiprogrammi registreerimise** atribuut olekusse **Jah** **Retaili** kiirkaardil **Kõigi klientide** all. Blokeeritud kliendile ei saa väljastada kliendikaarti ühestki teisest kanalist.

    ![Pensionireeglid ja maksimaalsed preemiapunktid](./media/Vesting%20and%20maximum%20reward%20points.png "Määratlege pensionireeglid ja maksimaalsed preemiapunktid")

- Alluvusi kasutatakse erihindade ja allahindluste pakkumiseks, kuid mõningaid alluvusi ei soovi jaemüüjad klientidele näidata. Näiteks alluvus pealkirjaga "Palju kulutav klient", ei pruugi mõndadele klientidele meeldida. Lisaks on mõned alluvused, mida ei peaks kaupluses haldama, näiteks töövõtjate alluvused, sest te ei soovi, et kassapidajad otsustaksid, kes on töövõtjad ning pakuksid seega töövõtja-põhiseid allahindlusi. Jaemüüjad saavad nüüd valida alluvused, mis peaksid jaemüügikanalites peidetud olema. Alluvused, millele on märgitud **Kanalites peita**, ei saa kassas vaadata, lisada või eemaldada. Kuid alluvusega seotud hinnad ja allahindlused rakendatakse siiski toodetele.

    ![Peida alluvused](./media/Hide%20affiliations.png "Alluvuste peitmine kanalites")
    
- Kõnekeskuse kasutajad saavad nüüd hõlpsamalt kliente nende kliendikaardi teabe põhjal otsida ning navigeerida kliendikaardi ja kliendikaardi kannete lehele **Klienditeeninduse** leheküljelt.

    ![Klienditeenindus](./media/Customer%20service.png "Kliendi püsiklienditeave leidmine")
    
- Kui kliendikaart on kompromiteeritud, tuleb luua uus kaart ja olemasolevad punktid uuele kaardile üle tuua. Selles väljaandes on lihtsustatud asenduskaardi voogu. Lisaks saavad kliendid kõik või osa oma boonuspunktidest sõpradele ja perele kinkida. Punktide ülekandmisel luuakse igale kliendikaardile punktide korrigeerimise kirjed. Asenduskaardi ning ülekande saldo funktsioonile pääseb ligi **Kliendikaartide** lehelt.

    ![Punktide asendamine ja ülekandmine](./media/Replace%20and%20transfer%20points.png "Kliendikaardi asendamine või saldo ülekandmine")
    
- Jaemüüjad võivad soovida kasutada kindla kanali efektiivsust klientide registreerimiseks püsikliendi programmi. Nüüd salvestatakse kliendikaartide registreerimise allikad, et jaemüüjad saaksid nende andmete kohta aruandeid luua. Registreerimiste allikas salvestatakse automaatselt kõikide väljastatud kliendikaartide kohta MPOS/CPOS või e-Commerce'i kanalitest. Kliendikaartidele, mis on väljastatud varukontori avaldusega, saab kõnekeskuse kasutaja valida sobiva kanali.
- Varasemates väljaannetes said jaemüüjad kasutada MPOS/CPOS-i, et klientidele poes boonuspunkte lunastada. Kuid kuna nendes väljaannetes kuvati boonussaldo boonuspunktides, ei saanud kassiir vaadata kandele kohaldatavat valluta väärtuse summat. Kassapidaja pidi enne boonuspunktide maksmist punktid valuutasse teisendama. Praeguses väljaandes näeb kassapidaja pärast ridade kandega liitmist summat, mida boonuspunktid praeguses kandes katavad, hõlbustades kõikide või osade boonuspunktide kandes kasutamist. Lisaks näeb kassapidaja punkte, mis järgmise 30 päeva jooksul aeguvad, nii et nad saavad teha ülesmüüki või ristmüüki, et motiveerida klienti aeguvaid punkte sellele kandele kulutama.

    ![Kliendikaardi saldoga kaetud punktid](./media/Points%20covered%20by%20loyalty%20balance.png "Boonuspunktidega kaetud saldo kuvamine")

    ![Aeguvad punktid](./media/Expiring%20points.png "Aeguvate punktide kuvamine")

- Väljaandega 8.1.3 oleme lubanud kõnekeskuse kanalis kliendikaardiga tasumise suvandi. Selle suvandi lubamiseks looge püsikliendi maksevahendi tüüp ja seostage see kõnekeskusega. 

    > [!NOTE]
    > Kuna kliendikaardi maksed on seadistatud kaardimaksetena, peate valima kaardi lehelt **Kaardi seadistus**. 

    ![Kliendikaardi seadistus](./media/LoyaltyCardSetup.png "Kliendikaardi seadistus")

    Kui see on seadistatud, saavad kliendid oma boonuspunktid lunastada kõnekeskuses. Peale selle täiustame kasutajakogemust veelgi, kuvades boonuspunktidega kaetud summat, nii et kõnekeskuse kasutajad ei pea boonussaldo nägemiseks liikuma teisele kuvale.

- Paljud jaemüüjad pakuvad boonuspunkte ainult müügikannete põhjal, kuid kliendikesksemad jaemüüjad soovivad premeerida oma kliente mis tahes suhtlustegevuse eest oma kaubamärgiga. Näiteks võivad nad pakkuda preemiaid veebiküsitluse täitmise eest, poe külastamise eest, jaemüüja meeldivaks märkimise eest Facebookis või jaemüüja kohta säutsumise eest Twitteris. Selleks saab jaemüüja määrata mis tahes arvu muid tegevusetüüpe ja määratleda nendele tegevustele vastavad teenimisreeglid. Avaldatud on ka jaemüügiserveri API PostNonTransactionalActivityLoyaltyPoints, mida saab kutsuda, kui tuvastatakse tegevus, mis määrab kliendile boonuspunkte. See API eeldab kliendikaardi ID-d, kanali ID-d ja muu tegevusetüübi ID-d, et leida klient, kellele tuleb boonuspunktid määrata, ja tuvastada tegevuse teenimisreegel. 

    Preemiapunktid kannetega mitteseotud tegevuste puhul koosnevad tavaliselt kahest põhietapist.

    - Arusaamine, et on toimunud tegevus, mille eest tuleb määrata preemiapunktid.
    - Asjakohaste punktide andmine.

    Esimene etapp toimub rakendusest Microsoft Dynamics 365 for Retail väljaspool, näiteks kaubamärgist säutsumine või kaubamärgi Facebookis meeldivaks märkimine. Kui tegevus on tuvastatud, saavad jaemüüjad kutsuda ülalnimetatud jaemüügiserveri API ja määrata boonuspunktid reaalajas. Sellistel juhtudel pole ülevaatusetapp vajalik, kuna tegevus on toimunud ja vastavad punktid tuleb määrata. Esineb aga ka stsenaariume, mille puhul jaemüüja soovib kirjed enne punktide määramist üle vaadata. Näiteks on jaemüüja korraldanud kaupluses töötoa, mille puhul kliendid registreeruvad e-poe veebisaidil või muu sündmuste registreerimise rakenduse kaudu. Boonuspunkte teenivad aga ainult osalevad kliendid. Selliste stsenaariumide puhul võtsime versioonis 10.0 kasutusele andmeüksuse nimega **Jaemüügi püsikliendi tegevusetüübi read**. See andmeüksus võimaldab jaemüüjatel kasutada kas andmete impordi/ekspordi raamistikku (DIXF) või OData API-t registreerimaks tegevusi, mille puhul määratakse klientidele boonuspunkte. Andmeüksus talletab tegevused töölehele **Püsikliendi muude tegevuste read**, mida saab kasutada ülevaatamiseks ja muutmiseks. Kui andmed on üle vaadatud, saab IT-kasutaja tegevuseread kas käsitsi sisestada või käivitada töö nimega **Muu tegevusetüübi töötlemine püsikliendi ridade puhul**, mis sisestab kõik sisestamata tegevuseread ja määrab klientidele teenimisreeglite põhjal punktid. Ülaltoodud stsenaariumi puhul kutsub sündmuse registreerimise rakendus OData API, et saata kliendi teave rakendusse Dynamics 365 for Retail. IT-kasutaja saab siiski sisestada tegevuseread ainult nende klientide kohta, kes osalesid töötoas, ja kustutada tegevuseread teiste klientide puhul. 

    > [!NOTE]
    > Praegu sunnib süsteem kasutajaid seadistama muude tegevusetüüpide kohta numbriseeria, kuid see pole tulevastes väljaannetes vajalik etapp. Numbriseeria seadistamiseks minge jaotisse **Jaemüügi ühisparameetrid** \> **Numbriseeriad** ja valige numbriseeria suvandile **Püsikliendi muu tegevusetüübi ID**.

- Hea klienditeeninduse pakkumiseks ja kliendipäringute tõhusaks lahendamiseks peab kassapidajatel olema juurdepääs kliendi täielikule profiilile. Väljaandes 10.0 saavad kassapidajad näha kassas püsikliendi ajaloolisi üksikasju koos seostatud püsikliendiprogrammi ja järguteabega.
- Tasuta või allahindlusega tarne on üks kõrgelt motiveeriv tegur, mis paneb kliente veebist ostma. Tarnimiskampaaniate loomiseks võtsime väljaandes 10.0 kasutusele uut tüüpi kampaania nimega Saatmisläve allahindlus, kus jaemüüja saab määratleda läved, mille täitmisel kvalifitseerub klient allahindlusega või tasuta tarnele. Näiteks tuleb kõigil püsiklientidel kulutada 35 eurot kahepäevase tarne või tasuta kahepäevase tarne saamiseks. See funktsioon mõjutab uut täpsemate automaatsete kulude võimalust. Vaadake [täpsemate automaatsete kulude dokumentatsiooni](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges). Täpsemad automaatsed kulud tuleb lubada tarnimiskampaaniate toimimiseks. Need saab lubada lehe **Jaemüügi parameetrid** vahekaardil **Kliendi tellimused**, kui sisse lülitada konfiguratsioon Kasuta täpsemaid automaatseid kulusid. Kuna jaemüüja saab seadistada mitut tüüpi tasusid, nt käsitlemise või paigaldamise eest, peab ta määrama, millist tasu peetakse saatekuluks. Saatmise allahindlused kohalduvad ainult saatekulule. Tasu määramiseks saatekuluna liikuge vormile **Kulukoodid**, mille leiate jaotisest **Jaemüük** \> **Jaemüügi IT** \> **Kanali seadistus** \> **Kulud** ja märkige soovitud kulude jaoks märkeruut Kättetoimetamise tasu. Nüüd saate liikuda vormile **Jaemüügi tarne läve allahindlus** ja määrata allahindluse.

    Nagu ka toodete allahindlused, arvestab see allahindlus kõiki olemasolevaid tavalisi allahindlusvõimalusi, näiteks lubamine jaemüüjal piirata neid allahindlusi kupongidega, nii et allahindlusi saavad ainult kupongidega kliendid. Samuti kasutavad need allahindlused hinnagruppide võimalust määrata sobilikkust neile allahindlustele. Näiteks saab jaemüüja käivitada need soodustused ainult veebikanalites ja/või teatud kliendigruppide, näiteks püsiklientide, kanalites. Kui määratud tarneviisiga tellimuseread vastavad määratletud lävele, kohaldub saatmisele allahindlus ja vähendab saatekulu seadistatud allahindluse põhjal. 

    > [!NOTE]
    > Erinevalt muudest perioodilistest allahindlustest, nagu koguse, liht-, segamise ja sobitamise ning läveallahindlused, ei loo saateallahindlus allahindlusridu, pigem redigeerib saatekulu otse ja lisab allahindluse nime kulu kirjeldusele.
