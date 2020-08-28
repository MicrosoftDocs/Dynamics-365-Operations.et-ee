---
title: Asukohakorralduste loomine
description: Selles teemas kirjeldatakse asukohakorralduste loomist. Asukohakorraldused on kasutaja määratud reeglid, mis aitavad tuvastada komplekteerimise ja ladustamise asukohti varude liigutamisel.
author: Mirzaab
manager: tfehr
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-28
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: bdd99b5faefd7054023b45a91fad070aac055a26
ms.sourcegitcommit: ecad92c9cb7e9e57688e678f79f747673c921df5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2020
ms.locfileid: "3692134"
---
# <a name="create-location-directives"></a>Asukohakorralduste loomine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse asukohakorralduste loomist. Asukohakorraldused on kasutaja määratud reeglid, mis aitavad tuvastada komplekteerimise ja ladustamise asukohti varude liigutamisel. Näiteks määratleb asukohakorraldus müügitellimuse kandes koha, kus kaubad komplekteeritakse ja kus komplekteeritud kaubad ladustatakse.

> [!NOTE]
> Selles teemas kirjeldatakse mooduli **Laohaldus** funktsioone. See ei kehti mooduli [Varude haldus](../inventory/inventory-home-page.md) funktsioonide korral.

Asukohakorraldusi saate kasutada järgmiste ülesannete täitmiseks.

- Sissetulevate kaupade ladustamine.
- Kaupade komplekteerimine ja etappide määramine väljaminevate kannete puhul.
- Toormaterjali komplekteerimine ja ladustamine tootmiseks.
- Asukohtade täiendamine.

## <a name="prerequisites"></a>Eeltingimused

Enne asukohakorralduse loomist peate järgima neid samme, et veenduda, et eeltingimused oleksid täidetud.

1. Avage **Laohaldus \> Seadistus \> Ladu \> Laod**.
1. Looge ladu.
1. Seadke kiirkaardil **Ladu** suvandi **Kasuta laohaldusprotsesse** väärtuseks *Jah*.
1. Looge asukohad, asukohatüübid, -profiilid ja -vormingud. Lisateavet lugege teemast [Asukohtade konfigureerimine WMS-loaga laos](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).
1. Looge kohad, tsoonid ja tsoonigrupid. Lisateavet lugege teemadest [Lao seadistamine](https://docs.microsoft.com/dynamics365/commerce/channels-setup-warehouse) ja [Asukohtade konfigureerimine WMS-loaga laos](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).

## <a name="setup"></a>Seadistus

### <a name="create-location-directives"></a>Asukohakorralduste loomine

Asukohakorralduse loomiseks toimige järgmiselt.

1. Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.
1. Määrake loendipaanil välja **Töökäsu tüüp** väärtuseks selle laokande tüüp, mille jaoks te asukohakorraldust loote.
1. Uue asukohakorralduse loomiseks valige toimingupaanilt **Uus**.
1. Seadke uue asukohakorralduse jaoks väljad nii, nagu kirjeldatud järgmises tabelis.

    | Väli | Kirjeldus |
    |---|---|
    | Järjekorranumber | Sisestage täisarv, mis näitab asukohakorralduse paigutust järjekorras. Paigutus järjekorras määrab, millal igat asukohakorraldust valitud töökäsu tüübi puhul töödeldakse. |
    | Nimi | Sisestage asukohakorralduse nimi. | 
    | Töö tüüp | Valige tehtava töö tüüp. Väärtuste loend sõltub laokande tüübist, mille valisite väljal **Töökäsu tüüp**. Saadaval võivad olla järgmised väärtused.<ul><li>**Ladustamine** – asukohakorraldus proovib leida parimat asukohta, kuhu panna või kust leida varusid, mis tulevad süsteemi vastuvõtmise, tootmise või varude korrigeerimise kaudu. Asukohakorraldust kasutatakse ka selleks, et määrata väljaminevas voos vaheasukoht või viimase laadimisukse asukoht.</li><li>**Komplekteerimine** – asukohakorraldus püüab leida parimaid asukohti, kust varusid füüsiliselt reserveerida (töö loomine). Komplekteerimise saab lõpule viia (see tähendab, et komplekteerimise töörea võib sulgeda) isegi siis, kui töö pole lõpule viidud. Kasutaja saab lõpetada füüsilise komplekteerimise. Süsteemis on see tegevus komplekteerimise etapp. Seejärel saab kasutaja töö (näiteks ladustamise) mobiilsest seadmest tühistada ja hiljem lõpule viia. Lõpliku ladustamise lõpuleviimisel suletakse tööpäis siiski esimesena.</li><li>**Inventuur**, **Korrigeerimised**, **Kohandatud**, **Varude oleku muutus**, **Litsentsiplaadi koostamine**, **Printimine**, **Oleku muutus** ja **Paki pesastatud litsentsiplaatidesse** – neid väärtuseid ei saa kasutada üheski asukohakorralduse seadistuses.</li></ul> |
    | Koht | Valige koht, kus töö tuleb lõpule viia. |
    | Ladu | Valige laoasukoht, kus töö tuleb lõpule viia. |
    | Korralduse kood | Valige korralduse kood, et suunata asukohakorraldusi, mis on seotud töömalli ladustamisridadega, mille jaoks see kood on määratud. Lehel **Korralduse kood** saate luua uusi koode, mida saab kasutada töömalli ühendamiseks asukohakorraldusega. Sellel lehel saate ka luua seose mis tahes töömalli rea ja asukohakorralduse vahel (nt laadimisuks või vaheasukoht). Lisateavet töömalli abil korralduse koodi konfigureerimise kohta leiate teemast [Laotöö juhtimine töömallide ja asukohakorraldustega](control-warehouse-location-directives.md).<p>Kui korralduse kood on määratud, otsib süsteem töö loomise kohustuse korral asukohakorraldusi korralduse koodi, mitte järjestuse järgi. Sel moel saate määrata täpsemalt asukohamalli, mida kasutatakse töömallis kindla etapi jaoks, nt materjalide ettevalmistamise etapi jaoks.</p> |
    | Likvideerimiskood | Valige likvideerimiskood, et suunata vastuvõetud kaupade ladustamine ümber asukohta. (Lisateavet leiate teemast [Likvideerimiskoodide seadistamine](tasks/set-up-dispositions-codes.md).) See väli on saadaval ainult siis, kui välja **Töökäsu tüüp** väärtuseks on seatud *Ostutellimused*, *Tagastustellimused* või *Lõpetatud kaupade ladustamine*. |
    | Mitu SKU-d | Seadke selle suvandi väärtuseks *Jah*, et kasutada asukohas mitut varude arvestusühikut (SKU). Näiteks peab selle suvandi väärtus olema laadimisukse puhul *Jah*.<p>Kui suvandi **Mitu SKU-d** väärtuseks on seatud *Jah*, täpsustatakse ladustamisasukoht töös (ootuspäraselt). Kuid ladustamisasukoht saab käidelda mitme kauba ladustamist ainult siis, kui töö hõlmab erinevaid SKU-sid, mis tuleb komplekteerida ja ladustada, mitte siis, kui töö hõlmab ainult ühte SKU-d, mis tuleb ladustada.</p><p>Kui suvandi **Mitu SKU-d** väärtuseks on seatud *Ei*, määratakse ladustamisasukoht ainult siis, kui ladustatakse ainult üht tüüpi SKU-d.</p><p>Mõlema meetodi kasutamiseks peate määrama kaks rida, millel on sama struktuur ja seadistus, kuid seadma ühe rea puhul suvandi **Mitu SKU-d** väärtuseks *Jah* ning teise puhul *Ei*. Teisisõnu on vaja ladustamistoimingute jaoks kaht samasugust asukohakorraldust, kuigi te ei pea töö ID-s üht ja mitut SKU-d eristama. Samuti peate seadistama asukorralduse komplekteerimise jaoks, kui teil on rohkem kui ühe kaubaga tellimus.</p><p>**Märkus.** Kui määrate suvandi **Mitu SKU-d** väärtuseks *Jah* töökorralduse puhul, mille töö tüüp on *Ladustamine*, siis valib süsteem alati esimese asukohakorralduse rea, sõltumata ridades loodud muudest piirangutest.</p> |

1. Valikuline: valige toimingupaanil suvand **Redigeeri päringut**, et valida asukohad või määrata kindla asukohakorralduse valimisel rakendatavad piirangud.
1. Looge kiirkaardil **Read** üks või mitu rida, et määrata ühikud ja leida või reserveerida laos kogus.
1. Seadke igal uuel real väljad nii, nagu kirjeldatud järgmises tabelis.

    | Väli | Kirjeldus |
    |---|---|
    | Järjekorranumber | Sisestage täisarv, mis näitab asukohakorralduse paigutust järjekorras. Paigutus järjekorras määrab, millal igat asukohakorraldust valitud töö tüübi puhul töödeldakse. |
    | Alates kogusest | Määrake kogusevahemiku algus, mille puhul tuleb valida ruudustiku keskosa seeria. Määrake kogus mõõtühikus, mis on valitud väljal **Ühik**. |
    | Kuni koguseni | Määrake kogusevahemiku lõpp, mille puhul tuleb valida ruudustiku keskosa seeria. Määrake kogus mõõtühikus, mis on valitud väljal **Ühik**. |
    | Ühik | Valige kaupade jaoks mõõtühikud.<p>Saate määrata minimaalse ja maksimaalse koguse, mille puhul peaks korraldus rakenduma. Samuti saate määrata, et seda korraldust tuleks kasutada konkreetse laoühiku puhul. Välja **Ühik** kasutatakse ainult koguse hindamiseks.</p><p>Et teha kindlaks, kas asukohakorralduse rida rakendub, hindab süsteem koguseid, kasutades real määratud väärtust **Ühik**. Iga kord, kui asukohakorralduse rida kasutatakse, püüab süsteem teisendada nõudluse ühiku real määratud ühikusse. Kui ühikut ei saa teisendada, liigub süsteem edasi järgmisele reale.</p> |
    | Koguse asukoha määramine | See väli kehtib ainult siis, kui proovite kogust lattu ladustada või seda laost leida. Teisisõnu kehtib see ainult tööde puhul, mille tüüp on *Ladustamine*. Valige meetod, mida kasutatakse selle hindamiseks, kas kogus jääb väljadel **Alates kogusest** ja **Kuni koguseni** määratud vahemikku. Kui asukohakorraldus on mõeldud sissetuleva kande jaoks, valige mõni järgmistest suvanditest.<ul><li>**Litsentsiplaadi kogus** – et hinnata, kas kogus on koguse sihtvahemikus, kasutage kogust vastuvõetaval litsentsiplaadil.</li><li>**Ühikuteks jagatav kogus** – et hinnata, kas kogus on koguse sihtvahemikus, kasutage kogust, mis jagatakse kande jooksul ühikutesse. Näiteks kui saate laos vastu võtta koguse 1000 ja jagada selle 10 litsentsiplaadiks (igaühe kogus on 100), saate litsentsiplaadi koguse 100 asemel kasutada kogusena 1000 kaupa.</li><li>**Jääkkogus** – et hinnata, kas kogus on koguse sihtvahemikus, kasutage kogust, mis tuleb veel parasjagu sisseregistreeritava ostutellimuse real vastu võtta.</li><li>**Eeldatav kogus** – et hinnata, kas kogus on koguse sihtvahemikus, kasutage ostutellimuse rea kogukogust olenemata sellest, milline kogus on juba vastu võetud.</li></ul> |

1. Valikuline: saate kiirkaardil **Read** seadistada järgmisi lisavälju.

    | Väli | Kirjeldus |
    |---|---|
    | Piira ühiku alusel | Valige see märkeruut, et piirata mõõtühikuid, mida peetakse asukohakorralduste ridade puhul sobivateks valikukriteeriumideks. Kui mõõtühikud on määratud, loetakse reavaliku puhul sobivaks ainult kaubad, mille ühik ühtib vähemalt ühe ühikuga, mis on määratud ühiku seeriagrupi jaoks.<p>Näiteks kasutatakse ühikut ainult kaubaaluste puhul ja kaup on seotud ühiku seeriagrupiga, mis sisaldab *kaubaaluste* ühikut. Sel juhul loetakse kaubad asukohakorralduse jaoks sobivaks valikuks.</p><p>Siiski ei reguleeri märkeruut **Piira ühiku alusel** ühikut või ühikuid, mida rakendatakse tööridadel. Ühikupiirang rakendub ainult ühikutele, mis on saadaval ühiku seeriagrupi kaudu.</p><p>Näiteks on kaup seotud ühiku seeriagrupiga, mis sisaldab nii *kaubaaluste* kui ka *tk* ühikut. Määratletud on mõõtühik, kus 1 kaubaalus = 100 tk, ning asukohakorraldus kasutab funktsiooni **Piira ühiku alusel** ainult kaubaaluste puhul. Lisaks on määratletud töömall, mis seab tööpäise loomisele 50 tk suuruse piirangu. Sel juhul luuakse 50 tk suuruseid tööridasid.</p><p>Piirangu mõõtühiku määramiseks toimige järgmiselt</p><ol><li>Valige kiirkaardil **Read** suvand **Piira ühiku alusel**. See nupp muutub kättesaadavaks ainult pärast seda, kui valite real märkeruudu **Piira ühiku alusel** ja seejärel **Salvesta**.</li><li>Valige väljal **Ühik** mõõtühik, mille alusel soovite komplekteerimis- ja ladustamisprotsesse piirata.</li></ol> |
    | Ümarda ühikuni | Valige see suvand näitamaks, et toormaterjali komplekteerimine tuleb ümardada väljal **Piira ühiku alusel** määratud materjali käsitlemisühiku kordseni. See väli kehtib ainult toormaterjali komplekteerimise puhul ja ainult asukohakorralduste puhul, mille tüüp on *Komplekteerimine*. |
    | Pakkimiskoguse leidmine | Valige see märkeruut, kui pakkimisühiku kogus on lehel **Müügitellimus** määratud. Selle märkeruudu märkimisel valitakse ainult selle pakkimisühiku kogusega asukohad. |
    | Luba tükeldamine | Märkige see märkeruut koguse jaotamiseks mitme asukoha vahel. |
    | Viivitamatu täiendamise mall | Looge ühendus täiendamismalliga, et käivitada täiendamine kohe, kui kaupu ei eraldata. Kui jätate selle välja tühjaks, ei käivitu kauba täiendamine enne, kui kõik asukohakorralduse read on töödeldud.<p>See väli on saadaval ainult valitud töökäsu tüüpide puhul, kus täiendamine on lubatud, näiteks *Müügitellimused* ja *Toormaterjali komplekteerimine*.</p> |

1. Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus**, et valida asukoht või asukohavahemik.
1. Väljal **Järjekorranumber** kuvatakse number, mille alusel asukohakorraldust valitud töötüübi puhul töödeldakse. Saate järjestust muuta. Siiski olge asukohakorralduse tegevuste järjekorranumbrite puhul ettevaatlik, kuna asukohakorralduse tegevused käivitatakse alati selles järjestuses.
1. Sisestage väljale **Nimi** asukohakorralduse tegevuse nimi. Olge konkreetne, et oleks selge, mis tegevus see on.
1. Valikuline: valige suvand **Redigeeri päringut** lao asukohtade ja muude kriteeriumide muutmiseks.
1. Valikuline: asukohakorralduse jaoks saate seadistada järgmisi lisavälju.

    | Väli | Kirjeldus |
    |---|---|
    | Fikseeritud asukoha kasutamine | Valige, mis asukohti asukohakorraldus peaks arvestama.<ul><li>**Fikseeritud ja fikseerimata asukohad** – asukohakorraldus kaalub kõiki asukohti.</li><li>**Ainult toote fikseeritud asukohad** – asukohakorraldus kaalub ainult toodete fikseeritud asukohti.</li><li>**Ainult tootevariandi fikseeritud asukohad** – asukohakorraldus kaalub ainult tootevariantide fikseeritud asukohti.</li></ul> |
    | Luba negatiivne laovaru | Märkige see märkeruut määratud laoasukohas negatiivsete varude lubamiseks. |
    | Partii on lubatud | Märkige see märkeruut, et kasutada partiiloaga kaupade puhul partiistrateegiaid. Kui see märkeruut on märgitud ja välja **Strateegia** väärtuseks on seatud *Puudub*, liigub süsteem edasi järgmisele tegevusreale. |
    | Strateegia | Valige strateegia, mida asukohakorraldus peaks kasutama.<ul><li>**Puudub** – ühtegi strateegiat ei kasutata.</li><li>**Vastenda pakkimiskogusega** – see strateegia kontrollib, kas komplekteerimisasukohas on määratud pakkimiskogus olemas. See strateegia kehtib ainult siis, kui välja **Töö tüüp** väärtuseks on seatud *Komplekteerimine*.</li><li>**Konsolideeri** – see strateegia konsolideerib kaubad kindlas asukohas, kui sarnased kaubad on juba saadaval. See strateegia kehtib ainult siis, kui välja **Töö tüüp** väärtuseks on seatud *Ladustamine*. Tüüpilise ladustamisseadistuse puhul püüab süsteem konsolideerida esimesel tegevusereal ja üritab seejärel teisel tegevusreal ladustada ilma konsolideerimata. Kaupade konsolideerimine muudab hilisema komplekteerimise tõhusamaks.</li><li>**FEFO partii reserveerimine** – seda strateegiat kasutatakse siis, kui varusid leitakse partii aegumiskuupäeva abil ja need eraldatakse partii reserveerimiseks. Partii reserveerimisstrateegiat „esimesena aegunud, esimesena välja” (FEFO) kasutatakse ka siis, kui varusid leitakse lisaks aegumiskuupäevale ka partii „parim enne” kuupäeva põhjal. Seda strateegiat saate kasutada ainult partiiloaga kaupade puhul. See strateegia kehtib ainult siis, kui välja **Töö tüüp** väärtuseks on seatud *Komplekteerimine*. Kui valite selle strateegia, alistate rakenduvad partiinumbrite päringute sortimised.</li><li>**Täieliku LP-ni ümardamine** – see strateegia ümardab varude koguse, et see vastaks litsentsiplaadi kogusele, mis on määratud komplekteeritavatele kaupadele. Seda strateegiat saab kasutada ainult täiendamistüüpi asukohakorralduste puhul ja ainult siis, kui välja **Töö tüüp** väärtuseks on seatud *Komplekteerimine*.</li><li>**Tühi asukoht ilma sissetuleva tööta** – seda strateegiat kasutatakse tühjade asukohtade leidmiseks. Asukoht loetakse tühjaks, kui sel ei ole füüsilisi varusid ja eeldatavat sissetulevat tööd. See strateegia kehtib ainult siis, kui välja **Töö tüüp** väärtuseks on seatud *Ladustamine*.</li></ul> |

## <a name="example-of-the-use-of-location-directives"></a>Asukoha korralduste kasutamise näide

Selle näite puhul kaaluge ostutellimuse protsessi, kus asukohakorraldus peab leidma laos äsja vastuvõtudokis registreeritud laokaupade jaoks vaba ruumi. Esiteks peate leidma vaba ruumi laos, konsolideerides olemasoleva vaba kaubavaruga. Kui konsolideerimine ei ole võimalik, peate leidma tühja asukoha.

Selle stsenaariumi puhul peate määratlema kaks asukohakorralduse toimingut. Esimene tegevus järjekorras peab kasutama strateegiat **Konsolideeri** ja teine strateegiat **Tühi asukoht sissetuleva tööta**. Kui te ei määratle kolmandat toimingut ületäitmisstsenaariumi käsitlemiseks, on võimalikud kaks tulemust, kui laos ei ole enam ruumi: töö saab luua isegi siis, kui asukohti ei määratleta, või töö loomise protsess võib nurjuda. Tulemuse määrab lehe **Asukoha korralduse tõrked** seadistus, kus saate otsustada, kas valida suvand **Peata töö asukoha korralduse tõrke korral** igale töö tellimuse tüübile.

## <a name="next-step"></a>Järgmine samm

Pärast asukohakorralduste loomist saate töö loomiseks seostada iga korraldusekoodi töömalli koodiga. Lisateavet vaadake teemast [Laotöö juhtimine töömallide ja asukohadirektiividega](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/control-warehouse-location-directives).

## <a name="technical-information-for-system-admins"></a>Tehniline teave süsteemiadministraatoritele

Kui teil pole juurdepääsu lehtedele, mida kasutatakse selle ülesande täitmiseks, pöörduge oma süsteemiadministraatori poole ja edastage järgmises tabelis toodud andmed.

| Kategooria | Eeltingimus |
|---|---|
| Configuration keys | Valige suvandid **Süsteemihaldus \> Häälestus \> Litsentsi konfiguratsioon**. Laiendage litsentsivõti **Kaubandus** ning valige seejärel konfiguratsioonivõti **Lao- ja transpordihaldus**. |
