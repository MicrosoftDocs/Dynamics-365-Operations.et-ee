---
title: Püsikliendi ülevaade
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Commerce püsikliendi võimalusi ja vastavaid seadistusetappe, mis aitavad jaemüüjal hõlpsasti oma püsikliendiprogrammiga algust teha.
author: scott-tucker
manager: AnnBe
ms.date: 07/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailLoyaltyPrograms, RetailPriceDiscGroup
audience: Application User
ms.reviewer: josaw
ms.custom: 16201
ms.assetid: f79559d2-bc2d-4f0b-a938-e7a61524ed80
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 1697c377c8291190f27b2057463ddb98aac1f9b9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264548"
---
# <a name="loyalty-overview"></a>Püsikliendi ülevaade

[!include [banner](includes/banner.md)]

Püsikliendiprogrammid aitavad suurendada klientide lojaalsust, premeerides kliente teie jaemüüja kaubamärgiga suhtlemise eest. Rakenduses Dynamics 365 Commerce saate seadistada lihtsaid või keerulisi püsikliendiprogramme, mis kehtivad kõikide teie juriidiliste isikute kõikides kaubanduse kanalites. Selles teemas kirjeldatakse rakenduse Commerce püsikliendi võimalusi ja vastavaid seadistusetappe, mis aitavad jaemüüjal hõlpsasti oma püsikliendiprogrammiga algust teha.

Saate seadistada püsikliendiprogrammi nii, et see hõlmaks järgmisi valikuid.

- Seadistage mitu püsikliendiprogrammides pakutavat preemiate tüüpi ja jälgige osalust püsikliendiprogrammides.
- Seadistage püsikliendiprogrammid, mis näitavad erinevaid pakutavaid preemiaid. Saate kaasata püsikliendiprogrammi järke, et pakkuda lisaimpulssi ja suuremaid preemiaid klientidele, kes ostavad sagedamini või kes kulutavad teie poodides rohkem raha.
- Määrake teenimisreeglid, et panna paika tegevused, mida klient peab preemia saamiseks tegema. Samuti saate määrata lunastamisreeglid, et panna paika, millal ja kuidas klient preemia lunastada saab.
- Väljastage kliendikaarte mis tahes teie püsikliendiprogrammis osalevast kanalist ja siduge kliendikaardid vähemalt ühe püsikliendiprogrammiga, milles klient saab osaleda. Samuti saate kliendikirje kliendikaardiga siduda, et klient saaks püsikliendipunkte koguda mitmelt kaardilt ja neid lunastada.
- Kliendi andmete korrigeerimiseks või tema premeerimiseks saate kliendikaarte käsitsi kohandada või kandke püsikliendipreemiate saldo ühelt kaardilt teisele.

## <a name="setting-up-loyalty-programs"></a>Püsikliendiprogrammide seadistamine

Püsikliendifunktsiooni võimaldamiseks rakenduses Commerce peate seadistama mitu komponenti. Järgmisel joonisel on kujutatud püsikliendiprogrammi komponendid ja nende omavahelised seosed.

![Püsikliendi seadistuse protsessivoog](./media/loyaltyprocess.gif "Püsikliendiprogrammi komponendid ja nende omavahelised seosed")

## <a name="loyalty-components"></a>Püsikliendiprogrammi komponendid

Järgmises tabelis kirjeldatakse kõiki komponente ja nende kasutuskohta püsikliendiprogrammi seadistamisel.

| Komponent                                        | Kirjeldus | Kus seda kasutatakse? |
|--------------------------------------------------|-------------|-----------------|
| Allahindluste seadistamine (eeltingimus)                  | Seadistage püsiklientidele pakutavad allahindlused. Näiteks saate teha 5-protsendise allahindluse kõigile rõivatoodetele. | Allahindlused tuleb lisada hinnagruppidele, enne kui need saab kaasata püsikliendiprogrammi. Hinnagrupid määratakse püsikliendiprogrammidele ja püsikliendijärkudele. |
| Hinnagruppide seadistamine (eeltingimus)               | Hinnagruppe kasutatakse toodete hindade ja allahindluste loomiseks ning haldamiseks. Seadistage hinnagrupid, mis sisaldavad teie püsikliendiprogrammidele kehtivaid allahindlusi. | Hinnagrupid määratakse püsikliendiprogrammidele ja püsikliendiprogrammi järkudele. |
| Kanalite seadistamine (eeltingimus)                   | Kaubanduse kanalid on püsikliendiprogrammides osalevad poed, nagu füüsiline kauplus, veebipood või kõnekeskus. Peate seadistama kanalid, enne kui saate neile püsikliendiprogrammid määrata. | Määrake püsikliendiprogrammile kanalid, kui kanal osaleb püsikliendiprogrammis. |
| Püsikliendi makseviisi seadistamine (eeltingimus) | Et tagada püsikliendi punktide lunastamine mis tahes kanalis (nt füüsilised kauplused, veebipoed või kõnekeskused), peate lehel **Kaardinumbrid** häälestama kliendikaartide asukohavahemiku. | Seadistage püsikliendi makseviis ja määrake seejärel püsikliendi makseviis püsikliendiprogrammis osalevate kanalite jaoks. |
| Kuupäevaintervallide seadistamine                            | Kuupäevaintervallid võimaldavad paindlikult püsikliendijärkudele kehtivat ajavahemikku seadistada. Kuupäevaintervallidega saate määrata, kui kaua saab klient ühes järgus olla või kui palju aega on kliendil järku kvalifitseerumise jaoks tegevuse lõpetamiseks. | Kuupäevaintervallid kehtivad ainult siis, kui kasutate püsikliendiprogrammides järkusid. Valige kuupäevaintervall, mis kehtib programmi järkudele, ja kuupäevavahemikud, mis kehtivad programmi järgu reeglitele. |
| Preemiapunktide seadistamine                             | Preemiapunktid on teatud tüüpi preemiad, mida klientidele pakute. Preemiapunktid võivad olla lunastatavad või mittelunastatavad. Lunastatavaid preemiapunkte saab vahetada toodete vastu. Mittelunastatavaid preemiapunkte kasutatakse jälgimiseks või kliendi edendamiseks püsikliendiprogrammi järgmisesse järku. | Preemiapunktidele viidatakse järgureeglites ja neid kasutatakse selleks, et klient kvalifitseeruks konkreetse järgu jaoks. Preemiapunktidele viidatakse ka püsikliendiskeemide teenimise ja lunastamise reeglites. Teenimisreeglites määrate preemiad, mille klient saab konkreetse tegevuse eest teenida. Lunastamisreeglites määrate preemia, mille klient lunastada saab. |
| Püsikliendiprogrammide seadistamine                          | Püsikliendiprogrammid on peamine püsikliendiüksus, mida pakute. Igale püsikliendiprogrammile võivad olla määratud püsikliendijärgud. Allahindlused ja hinnagrupid määratakse püsikliendiprogrammidele kas programmi tasemel või järgu tasemel. | Looge püsikliendiprogrammide jaoks püsikliendiskeeme. Määrake püsikliendiprogrammidele kliendikaardid ja kliendikaarte saab kliendile määrata. Kanalid osalevad püsikliendiprogrammides, mis määratakse püsikliendiskeemidele. Kõik kliendikaardiga kliendid saavad osaleda kaardile määratud püsikliendiprogrammides. |
| Püsikliendijärkude ja järgureeglite seadistamine              | Püsikliendijärgud on valikulised tasemed, mille saate püsikliendiprogrammides määrata. Saate seadistada baasallahindlused ja -preemiad kõikidele püsikliendiprogrammis osalevatele klientidele ning täiendavad allahindlused ja preemiad programmis erinevatele tasemetele jõudvatele klientidele. Igale määratletud püsikliendijärgule saate seadistada reeglid, mis kliendi selle järgu jaoks kvalifitseerivad. Samuti saate määratleda, kui kauaks saavad kliendid jõutud järku jääda. | Püsikliendijärgud ja püsikliendijärgu reeglid on määratud püsikliendiprogrammis. Kui te püsikliendijärke ei määra, kvalifitseeruvad kõik püsikliendiprogrammis osalevad kliendid allahindlustele, mille püsikliendiprogrammi hinnagrupis määrate. Kui määrate püsikliendijärgud, saate seadistada püsikliendiskeemi püsikliendijärkudele teenimis- ja lunastamisreeglid. |
| Boonusskeemide häälestamine                           | Püsikliendiskeemid määravad teenimis- ja lunastamisreeglid, mis kehtivad valitud püsikliendiprogrammis. Määrake püsikliendiskeemile kanalid, et panna paika, millised püsikliendiprogrammid, teenimis- ja lunastamisreeglid kauplusele kehtivad. | Püsikliendiskeem määratakse püsikliendiprogrammile ja kanalitele. Saate määrata mitu püsikliendiskeemi samale püsikliendiprogrammile ja saate määrata mitu püsikliendiskeemi mitmele kanalile. |
| Kliendikaartide häälestamine                             | Kliendikaart annab kaardiomanikule õiguse osaleda kaardile määratud püsikliendiprogrammides. Kliendikaarte saab väljastada anonüümselt või määrata need konkreetsele kliendile. Saate vaadata konkreetse kaardi kandeid ja kokkuvõtet boonuspunktidest, mis on kaardile kogunenud. Kliendikaarte saate väljastada ükskõik millisest kanalist. Samuti saate kliendikaarti käsitsi korrigeerida, et tõsta klient uude järku, lisada boonuspunkte või kanda boonuspunktide saldo ühelt kaardilt teisele. | Määrake kliendikaardile püsikliendiprogramme. |

## <a name="loyalty-processes"></a>Püsikliendi protsessid

Järgmises tabelis kirjeldatakse protsesse, mida tuleb käitada, et saata püsikliendiprogrammi konfiguratsioonid ja andmed kauplustesse ning võtta kauplustest püsikliendikanded vastu.

| Protsessi nimi                         | Kirjeldus | Lehe nimi |
|--------------------------------------|-------------|-----------|
| 1050 (püsikliendi teave)           | Käitage seda protsessi, et saata püsikliendiprogrammi konfigureerimise andmed rakendusest Commerce kauplustesse. Soovitatav on ajastada see protsess sageli käivituma, et püsikliendiandmed edastataks kõigisse kauplustesse. | Jaotusgraafik |
| Boonusskeemide töötlemine              | Käitage seda protsessi, et seostada püsikliendiskeemid kanalitega, millele püsikliendiskeem on määratud. Seda protsessi saab käitada pakktöötlusena. Peate seda protsessi käitama, kui muudate püsikliendi konfiguratsiooniandmeid, nagu püsikliendiskeemid, püsikliendiprogrammid või püsikliendi preemiapunktid. | Boonusskeemide töötlemine |
| Sisesta teenitud püsikliendiprogrammi punktid partiidena | Käitage seda protsessi, et värskendada kliendikaarte kaasamaks neisse võrguühenduseta töödeldud kandeid. See protsess rakendub ainult siis, kui lehel **Kaubanduse ühisparameetrid** on märgitud ruut **Sisesta teenitud punktid partiidena**, et preemiaid saaks teenida ka võrguühenduseta. | Sisesta teenitud püsikliendiprogrammi punktid partiidena |
| Uuenda kliendikaartide järke            | Käitage seda protsessi, et hinnata kliendi teenimisaktiivsust püsikliendiprogrammi järgureeglite suhtes ja värskendada kliendi järgu olekut. See protsess on nõutav ainult siis, kui muudate püsikliendiprogrammide järgureegleid ja soovite, et värskendatud reeglid kehtiksid tagasiulatuvalt juba väljastatud kliendikaartide puhul. Seda protsessi saab käitada pakktöötlusena või üksikute kaartide puhul. | Uuenda kliendikaartide järke |

## <a name="loyalty-capabilities"></a>Püsikliendi võimalused

- Püsikliendi programmi ja püsikliendijärguga seostatud hinnagruppide abil saavad jaemüüjad püsiklientidele hõlpsasti erihindu ja allahindlusi luua.

- Osana boonusskeemist saavad jaemüüjad luua erinevaid teenimis- ja lunastamisreegleid püsikliendijärkude järgi, et eristada ei järkude klientide preemiaid. Jaemüüjad saavad ka osana teenimis- ja lunastamisreeglitest kaasata alluvused, et teatud kliendigrupp saaks olla olemasolavate järkude osa, kuid neid premeeritakse siiski teisiti. See väldib vajadust täiendavate järkude loomiseks.
    
    > [!NOTE]
    > Boonusskeemi teenimisreeglid on täiendavad. Näiteks kui loote reegli, et premeerida kullajärgu klienti 10 punktiga iga USA dollari eest ning loote ka reegli premeerida iga "veterani" staatusega klienti 5 punktiga iga USA dollari, siis veteran, kes on ka kullajärgu klient, teeniks iga 1 USA dollari eesti 15 punkti, kuna see klient kvalifitseerub mõlemale reeglile. Kuid kui veteran-klient ei ole küllajärgu liige, teenib ta iga dollari eest 5 punkti. Kanalites muudatuste kajastamiseks käivitage **Boonusskeemide töötlemise** ja **1050** (püsikliendi teabe) tööd.
    
    ![Alluvusel põhinev teenimine](./media/Affiliation-based-earning.png "Alluvusel põhinevad teenimised")

- Jaemüüjatel on sageli teatud kliendigrupile erihinnad, kellele nad ei soovi püsikliendiprogrammi rakendada. Näiteks hulgimüüjad või töötajad, kes saavad erihindu kuid mitte boonuspunkte. Tavaliselt kasutatakse sellistele kliendigruppidele erihindade tegemiseks "alluvusi". Selleks, et piirata tetud kliendigruppe või kliente boonuspunkte teenimast, saab jaemüüja määrata ühe või rohkem alluvust boonunusskeemi jaotises **Välistatud alluvused**. Sel viisil ei saa kliendid, kes on olemasolevad püsikliendid, kuid kuuluvad välistatud alluvuste alla, oma ostude eest boonuspunkte teenida. Kanalites muudatuste kajastamiseks käivitage **Boonusskeemide töötlemise** ja **1050** (püsikliendi teabe) tööd.

    ![Välistatud alluvused](./media/Excluded-affiliations.png "Alluvuste välistamine boonuspunktide teenimisest")
    
- Kassa annab jaemüüjatele paindlikkuse füüsiliste kliendikaartide kasutamiseks või kordumatu kliendikaardi numbri automaatseks loomiseks. Kliendikaartide automaatseks loomiseks kauplusteks lülitage kauplusega seotud funktsiooniprofiilil sisse **Kliendikaardi numbri loomine**. Võrgukanalites saavad jaemüüjad kasutada IssueLoyaltyCard API-t, et klientidele kliendikaarte väljastada. Jaemüüjad saavad sellele API-le anda kliendikaardi numbri, mida kasutatakse kliendikaardi loomiseks, või kasutab süsteem kliendikaardi numbriseeriat rakendusest Commerce. Kuid kui numbriseeriat ei ole ja jaemüüja ei sisesta API-t kutsudes kliendikaardi numbrit, kuvatakse tõrge.

    ![Kliendikaardi loomine](./media/Generate-loyalty-card.png "Kliendikaardi numbri automaatne loomine")

- Teenitud ja lunastatud püsikliendipunkte saab nüüd salvestatada iga kande ja müügitellimuse müügirea suhtes, et sama summa saaks täieliku või osalise tagastuse korral tagasi maksta või tagasi võtta. Lisaks annab punktide nägemine müügireal kõnekeskuse kasutajatele võimaluse vastata klientide küsimustele teenitud või lunastatud punktide kohta igal real. Enne seda muudatust kalkuleeriti boonuspunktid tagastustel alati ümber, mille tulemuseks oli originaalist erinev summa, kui teenimis- või lunastusreegleid oli muudetud ning kõnekeskuse kasutajatel ei olnud ülevaadet punktide jaotumisest. Punkte saab vaadata iga kliendikaardi **Kaardikannete** alt. Funktsiooni lubamiseks lülitage sisse konfiguratsioon **Sisesta boonuspunktid müügirea kohta** vahekaardil **Kaubanduse ühisparameetrid** \> **Üldine**.

    > [!NOTE]
    > Soovitame tungivalt see funktsioon sisse lülitada, et tagastuste korral saaks kliendile tagasi anda või temalt võtta õige arvu punkte.

- Jaemüüjad saavad nüüd määrata iga boonuspunkti üleandmisperioodi. Üleandmisperioodi konfiguratsioon määrab kestuse alates teenimiskuupäevast, pärast mida on boonuspunktid klientidele saadavad. Üleandmata punkte saab vaadata **Üleandmata punktide** veerus **Kliendikaartide** lehel. Kui kliendid tagastavad kaupasid, mille eest nad teenisid püsikliendi punkte, lahutab süsteem vaikimisi esmalt üleandmata punktid ja arvestab seejärel saldo maha saadaolevatest punktidest. Saate siiski konfigureerida nii, et lahutatakse vaid saadaolevad punktid, mitte ei arvata maha üleandmata punktidest.

Lisaks saavad jaemüüjad määratleda maksimaalse püsikliendiprogrammi preemiapunktide määra ühe klinedikaardi kohta. Seda välja saab kasutada püsikliendiprogrammi pettuste vähendamiseks. Kui maksimaalne boonuspunktide summa on saavutatud, ei saa kasutaja rohkem punkte teenida. Jaemüüja võib otsustada sellised kaardid blokeerida, kuni nad on uurinud võimalikke pettuseid. Kui jaemüüja tuvastab pettuse, saab ta kliendikaardi blokeerida ja märkida kliendi blokeerituks. Selleks määrake kiirkaardi **Commerce** jaotise **Kõik kliendid** atribuudi **Blokeeri kliendi registreerimine püsikliendiprogrammis** väärtuseks **Jah**. Blokeeritud kliendile ei saa väljastada kliendikaarti ühestki teisest kanalist.

   ![Pensionireeglid ja maksimaalsed preemiapunktid](./media/Vesting-and-maximum-reward-points.png "Pensionireeglite ja maksimaalsete preemiapunktide määratlemine")

- Alluvusi kasutatakse erihindade ja allahindluste pakkumiseks, kuid mõningaid alluvusi ei soovi jaemüüjad klientidele näidata. Näiteks alluvus pealkirjaga "Palju kulutav klient", ei pruugi mõndadele klientidele meeldida. Lisaks on mõned alluvused, mida ei peaks kaupluses haldama, näiteks töövõtjate alluvused, sest te ei soovi, et kassapidajad otsustaksid, kes on töövõtjad ning pakuksid seega töövõtja-põhiseid allahindlusi. Jaemüüjad saavad nüüd valida alluvused, mis peaksid kanalites peidetud olema. Alluvused, millele on märgitud **Kanalites peita**, ei saa kassas vaadata, lisada või eemaldada. Kuid alluvusega seotud hinnad ja allahindlused rakendatakse siiski toodetele.

    ![Alluvuste peitmine](./media/Hide-affiliations.png "Alluvuste peitmine kanalites")
    
- Kõnekeskuse kasutajad saavad nüüd hõlpsamalt kliente nende kliendikaardi teabe põhjal otsida ning navigeerida kliendikaardi ja kliendikaardi kannete lehele **Klienditeeninduse** leheküljelt.

    ![Klienditeenindus](./media/Customer-service.png "Kliendi püsiklienditeabe leidmine")
    
- Kui kliendikaart on kompromiteeritud, tuleb luua uus kaart ja olemasolevad punktid uuele kaardile üle tuua. Selles väljaandes on lihtsustatud asenduskaardi voogu. Lisaks saavad kliendid kõik või osa oma boonuspunktidest sõpradele ja perele kinkida. Punktide ülekandmisel luuakse igale kliendikaardile punktide korrigeerimise kirjed. Asenduskaardi ning ülekande saldo funktsioonile pääseb ligi **Kliendikaartide** lehelt.

    ![Punktide asendamine ja ülekandmine](./media/Replace-and-transfer-points.png "Kliendikaardi asendamine või saldo ülekandmine")
    
- Jaemüüjad võivad soovida kasutada kindla kanali efektiivsust klientide registreerimiseks püsikliendi programmi. Nüüd salvestatakse kliendikaartide registreerimise allikad, et jaemüüjad saaksid nende andmete kohta aruandeid luua. Registreerimiste allikas salvestatakse automaatselt kõikide väljastatud kliendikaartide kohta MPOS/CPOS või e-Commerce'i kanalitest. Kliendikaartidele, mis on väljastatud varukontori avaldusega, saab kõnekeskuse kasutaja valida sobiva kanali.
- Varasemates väljaannetes said jaemüüjad kasutada MPOS/CPOS-i, et klientidele poes boonuspunkte lunastada. Kuid kuna nendes väljaannetes kuvati boonussaldo boonuspunktides, ei saanud kassiir vaadata kandele kohaldatavat valluta väärtuse summat. Kassapidaja pidi enne boonuspunktide maksmist punktid valuutasse teisendama. Praeguses väljaandes näeb kassapidaja pärast ridade kandega liitmist summat, mida boonuspunktid praeguses kandes katavad, hõlbustades kõikide või osade boonuspunktide kandes kasutamist. Lisaks näeb kassapidaja punkte, mis järgmise 30 päeva jooksul aeguvad, nii et nad saavad teha ülesmüüki või ristmüüki, et motiveerida klienti aeguvaid punkte sellele kandele kulutama.

    ![Boonussaldoga kaetud punktid](./media/Points-covered-by-loyalty-balance.png "Boonuspunktidega kaetud saldo kuvamine")

    ![Aeguvad punktid](./media/Expiring-points.png "Aeguvate punktide kuvamine")

- Väljaandega 8.1.3 oleme lubanud kõnekeskuse kanalis kliendikaardiga tasumise suvandi. Selle suvandi lubamiseks looge püsikliendi maksevahendi tüüp ja seostage see kõnekeskusega. 

    > [!NOTE]
    > Kuna kliendikaardi maksed on seadistatud kaardimaksetena, peate valima kaardi lehelt **Kaardi seadistus**. 

    ![Kliendikaardi seadistus](./media/LoyaltyCardSetup.png "Kliendikaardi seadistus")

    Kui see on seadistatud, saavad kliendid oma boonuspunktid lunastada kõnekeskuses. Peale selle täiustame kasutajakogemust veelgi, kuvades boonuspunktidega kaetud summat, nii et kõnekeskuse kasutajad ei pea boonussaldo nägemiseks liikuma teisele kuvale.

- Paljud jaemüüjad pakuvad boonuspunkte ainult müügikannete põhjal, kuid kliendikesksemad jaemüüjad soovivad premeerida oma kliente mis tahes suhtlustegevuse eest oma kaubamärgiga. Näiteks võivad nad pakkuda preemiaid veebiküsitluse täitmise eest, poe külastamise eest, jaemüüja meeldivaks märkimise eest Facebookis või jaemüüja kohta säutsumise eest Twitteris. Selleks saab jaemüüja määrata mis tahes arvu muid tegevusetüüpe ja määratleda nendele tegevustele vastavad teenimisreeglid. Avaldatud on ka Commerce’i skaala üksuse API „PostNonTransactionalActivityLoyaltyPoints”, mida saab kutsuda, kui tuvastatakse tegevus, mis määrab kliendile boonuspunkte. See API eeldab kliendikaardi ID-d, kanali ID-d ja muu tegevusetüübi ID-d, et leida klient, kellele tuleb boonuspunktid määrata, ja tuvastada tegevuse teenimisreegel. 

    Preemiapunktid kannetega mitteseotud tegevuste puhul koosnevad tavaliselt kahest põhietapist.

    - Arusaamine, et on toimunud tegevus, mille eest tuleb määrata preemiapunktid.
    - Asjakohaste punktide andmine.

    Esimene etapp toimub rakendusest Commerce väljaspool, näiteks kaubamärgist säutsumine või kaubamärgi Facebookis meeldivaks märkimine. Kui tegevus on tuvastatud, saavad jaemüüjad kutsuda ülalnimetatud Commerce’i skaala üksuse API ja määrata boonuspunktid reaalajas. Sellistel juhtudel pole ülevaatusetapp vajalik, kuna tegevus on toimunud ja vastavad punktid tuleb määrata. Esineb aga ka stsenaariume, mille puhul jaemüüja soovib kirjed enne punktide määramist üle vaadata. Näiteks on jaemüüja korraldanud kaupluses töötoa, mille puhul kliendid registreeruvad e-poe veebisaidil või muu sündmuste registreerimise rakenduse kaudu. Boonuspunkte teenivad aga ainult osalevad kliendid. Selliste stsenaariumide puhul võtsime versioonis 10.0 kasutusele andmeüksuse nimega **Jaemüügi püsikliendi tegevusetüübi read**. See andmeüksus võimaldab jaemüüjatel kasutada kas andmete impordi/ekspordi raamistikku (DIXF) või OData API-t registreerimaks tegevusi, mille puhul määratakse klientidele boonuspunkte. Andmeüksus talletab tegevused töölehele **Püsikliendi muude tegevuste read**, mida saab kasutada ülevaatamiseks ja muutmiseks. Kui andmed on üle vaadatud, saab IT-kasutaja tegevuseread kas käsitsi sisestada või käivitada töö nimega **Muu tegevusetüübi töötlemine püsikliendi ridade puhul**, mis sisestab kõik sisestamata tegevuseread ja määrab klientidele teenimisreeglite põhjal punktid. Ülaltoodud stsenaariumi puhul kutsub sündmuse registreerimise rakendus OData API, et saata kliendi teave rakendusse Commerce. IT-kasutaja saab siiski sisestada tegevuseread ainult nende klientide kohta, kes osalesid töötoas, ja kustutada tegevuseread teiste klientide puhul. 

    > [!NOTE]
    > Praegu sunnib süsteem kasutajaid seadistama muude tegevusetüüpide kohta numbriseeria, kuid see pole tulevastes väljaannetes vajalik etapp. Numbriseeria seadistamiseks minge jaotisse **Kaubanduse ühisparameetrid** \> **Numbriseeriad** ja valige numbriseeria suvandile **Püsikliendi muu tegevusetüübi ID**.

- Hea klienditeeninduse pakkumiseks ja kliendipäringute tõhusaks lahendamiseks peab kassapidajatel olema juurdepääs kliendi täielikule profiilile. Väljaandes 10.0 saavad kassapidajad näha kassas püsikliendi ajaloolisi üksikasju koos seostatud püsikliendiprogrammi ja järguteabega.
- Tasuta või allahindlusega tarne on üks kõrgelt motiveeriv tegur, mis paneb kliente veebist ostma. Tarnimiskampaaniate loomiseks võtsime väljaandes 10.0 kasutusele uut tüüpi kampaania nimega Saatmisläve allahindlus, kus jaemüüja saab määratleda läved, mille täitmisel kvalifitseerub klient allahindlusega või tasuta tarnele. Näiteks tuleb kõigil püsiklientidel kulutada 35 eurot kahepäevase tarne või tasuta kahepäevase tarne saamiseks. See funktsioon mõjutab uut täpsemate automaatsete kulude võimalust. Vaadake [täpsemate automaatsete kulude dokumentatsiooni](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges). Täpsemad automaatsed kulud tuleb lubada tarnimiskampaaniate toimimiseks. Need saab lubada lehe **Kaubanduse parameetrid** vahekaardil **Kliendi tellimused**, kui sisse lülitada konfiguratsioon Kasuta täpsemaid automaatseid kulusid. Kuna jaemüüja saab seadistada mitut tüüpi tasusid, nt käsitlemise või paigaldamise eest, peab ta määrama, millist tasu peetakse saatekuluks. Saatmise allahindlused kohalduvad ainult saatekulule. Tasu määramiseks saatekuluna liikuge vormile **Kulukoodid**, mille leiate jaotisest **Jaemüük ja kaubandus** \> **Jaemüügi ja kaubanduse IT** \> **Kanali seadistus** \> **Kulud** ja märkige soovitud kulude jaoks märkeruut Saatmistasu. Nüüd saate liikuda vormile **Saatmise läve allahindlus** ja määrata allahindluse.

    Nagu ka toodete allahindlused, arvestab see allahindlus kõiki olemasolevaid tavalisi allahindlusvõimalusi, näiteks lubamine jaemüüjal piirata neid allahindlusi kupongidega, nii et allahindlusi saavad ainult kupongidega kliendid. Samuti kasutavad need allahindlused hinnagruppide võimalust määrata sobilikkust neile allahindlustele. Näiteks saab jaemüüja käivitada need soodustused ainult veebikanalites ja/või teatud kliendigruppide, näiteks püsiklientide, kanalites. Kui määratud tarneviisiga tellimuseread vastavad määratletud lävele, kohaldub saatmisele allahindlus ja vähendab saatekulu seadistatud allahindluse põhjal. 

    > [!NOTE]
    > Erinevalt muudest perioodilistest allahindlustest, nagu koguse, liht-, segamise ja sobitamise ning läveallahindlused, ei loo saateallahindlus allahindlusridu, pigem redigeerib saatekulu otse ja lisab allahindluse nime kulu kirjeldusele.


[!INCLUDE[footer-include](../includes/footer-banner.md)]