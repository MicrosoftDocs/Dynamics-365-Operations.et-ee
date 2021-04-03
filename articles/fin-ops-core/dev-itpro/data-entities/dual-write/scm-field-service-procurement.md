---
title: Hanke integreerimine teenuste Supply Chain Management ja Field Service vahel
description: See teema kirjeldab, kuidas topeltkirjutusega integreerimine toetab ostutellimuse loomist ja värskendusi nii teenuses Supply Chain Management kaui ka Field Service.
author: RichardLuan
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 79a971e3de43cb0161d4ac5012f657a947bc567c
ms.sourcegitcommit: afbdc268bcdb1755d7f1bc79ad1b7fc801b2e2f5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/11/2021
ms.locfileid: "5579968"
---
# <a name="integrate-procurement-between-supply-chain-management-and-field-service"></a>Hanke integreerimine teenuste Supply Chain Management ja Field Service vahel

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management pakub töökindlat hankefunktsiooni. Dynamics 365 Field Service pakub sarnaseid funktsioone, mis toetavad teenuse protsessiga seostatud ostuprotsesse. Nende kahe rakenduse funktsioonid integreeritakse topeltkirjutuse kaudu ja tulemuseks saadavad ristfunktsionaalse kasutamise juhtumid lubatakse tabeli vastenduste, lahenduse loogika, vaadete ja vormide kaudu.

See integratsioon toetab ostutellimuse loomist ja enamasti ka mõlema rakenduse uuendusi. Samas Supply Chain Management kontrollib hinnakujundust, aadresse ja toote sissetulekut. Organisatsioonidele, mis kasutavad nii Field Service’i kui ka Supply Chain Managementi, on lubatud mitu võimast ristfunktsionaalse kasutamise juhtumit. Need kasutusjuhtumid võimaldavad hankeid käivitada ja jälgida kõigis süsteemides.

Järgmine näide näitab tabeleid mõlemas süsteemis ja kuidas need on üksteisega vastendatud. Ostutellimustele väljal Field Service viidatakse kui *kontoreale*, samas kui Supply Chain Managementi ostutellimustele viidatakse kui *hankija reale*. Integratsiooni lahendamiseks kasutab topeltkirjutus viidet *hankijaridade* linkimiseks *kontoridadega*. Lisateavet vt [Integreeritud hankija koondandmed](vendor-mapping.md).

![Hanke vastendamised](media/scm-field-service-tables.png)

## <a name="prerequisites"></a>Eeltingimused

Supply Chain Managementi integreerimiseks Field Service’iga peate installima järgmised komponendid.

- Field Service’i versioon 8.8.31.60 või uuem mitmekülgse ostutellimuse integreerimiseks
- Supply Chain Managementi versioon 10.0.14 või uuem
- Topeltkirjutus, OneFSSCM-i lahenduse käivitamiseks

## <a name="installation-guidelines"></a>Installimise juhised

### <a name="prerequisites"></a>Eeltingimused

- **Topeltkirjutus** – lisateabe saamiseks vt [topeltkirjutuse kodulehte](dual-write-home-page.md#dual-write-setup).
- **Dynamics 365 Field Service** – lisateabe saamiseks vt [Kuidas rakendus Dynamics 365 Field Service alla laadida](https://docs.microsoft.com/dynamics365/field-service/install-field-service#step-1-install-dynamics-365-field-service).

Kui need on teenuses Microsoft Dataverse lubatud, tutvustavad topeltkirjutus ja Field Service mitut lahenduse kihti, mis laiendavad keskkonda uute metaandmetega, vormide, vaadete ja loogikaga. Neid lahendusi saab lubada mis tahes järjestuses, kuigi te installite tavaliselt siin määratud järjestuses.

1. **Field Service Common** – Field Service Common installitakse, kui Field Service installitakse keskkonda.
2. **Field Service (ankur)** – Field Service (ankur) installitakse, kui Field Service installitakse keskkonda. 
3. **Supply Chain Management, laiendatud** – Supply Chain Managementi laiendatud versioon installitakse automaatselt, kui topeltkirjutus on keskkonnas lubatud. 
4. **OneFSSCM-i lahendus** – OneFSSCM installitakse automaatselt olenevalt sellest, milline lahendus (Field Service või Supply Chain Management) on viimati installitud.

    - Kui Field Service on juba keskkonda installitud ja te lubate topeltkirjutuse, mis installib Supply Chain Managementi laiendatud versiooni, installitakse ka OneFSSCM.
    - Kui Supply Chain Managementi laiendatud versioon on juba keskkonda installitud ja installite Field Service’i, installitakse ka OneFSSCM.

## <a name="initial-synchronization"></a>Esialgne sünkroonimine

Uute ostutellimuste loomiseks ja tööks olemasolevate ostutellimustega peate sünkroonima viiteandmed Supply Chain Managementi ja Dataverse’i vahel. Kasutate algset kirjutusfunktsiooni, et tuvastada tabeli seosed ja leida tabelid, mida peate antud kaardi jaoks lubama.

Peate sünkroonima järgmised tabelid.

- Tootemallid

    Kui käivitate algse kirjutamise, saate täieliku loendi vajalikest tabelitest. Siin on mõned näited neist mallidest.

    - Kõik tooted
    - Väljastatud tooted V2
    - Dataverse’is väljastatud eristatavad tooted

- Saidid
- Laod
- Hankekategooriate mallid

    Siin on mõned näited neist mallidest.

    - Hankekategooriad
    - Pro
    - Toote kategooriahierarhia
    - Tootekategooria määramised

- Hankijamallid, nt Hankija V2
- Kontaktisikute mallid, näiteks Dataverse ’i kontaktid V2
- Töötajamallid, nt Töötaja

Tabelite sünkroonimine tagab, et kõik Supply Chain Managementi dokumendid (ostutellimused ja toote sissetulekud) on Dataverse’is saadaval.

### <a name="account-and-vendor-tables"></a>Konto ja hankija tabelid

Field Service’i ostutellimused sõltuvad hankijate jälgimiseks tabelis Konto. Seetõttu kasutavad Dataverse’i ostutellimuste tabelid kontosid hankijate jälgimiseks. Selle võtmeerinevuse mahutamiseks tuleb aktiveerida neli järgmist töövoogu, et hoida kontod ja hankijad sünkroonis. 

- Hankijate loomine kontode tabelis
- Hankijate loomine hankijate tabelis
- Hankijate värskendamine kontode tabelis
- Hankijate värskendamine hankijate tabelis

Kui OneFSSCM on installitud, kuna installitud on nii Field Service kui ka Supply Chain Managementi laiendatud versioon, aktiveeritakse need töövood automaatselt. Kui Field Service pole installitud, kuid soovite integreerida ostutellimuse Dataverse’i tabelisse, peate need töövood aktiveerima. Mõlemal juhul, kui te ei soovi nullist alustada, peate võib-olla enne ostutellimuste loomist tagama, et kõik hankijad luuakse Dataverse’i kontodena. Vastasel juhul võivad ilmneda tõrked.

### <a name="initial-synchronization"></a>Esialgne sünkroonimine

Kui soovite, et olemasolevad ostutellimused ja toote sissetulekud oleks mõlemas süsteemis saadaval, peate tegema järgmiste mallide esmase sünkroonimise.

- Ostutellimuse päis V2
- CDC-i ostutellimuse rida
- CDS-i ostutellimuse rea kerge kustutamine
- Ostutellimuse sissetulek
- Ostutellimuse sissetuleku toode

## <a name="mappings-with-logic"></a>Vastendused loogikaga

Hanke integreerimine laiendab toote vastendamist järgmise loogikaga, et tagada, et veerg **Field Service’i tootetüübi** oleks Dataverse ’i toodete tabelis õigesti määratud.

- Kui suvand **Toote tüüp** on määratud valikule *Toode* ja **Toote ja kauba mudeligrupp** on määratud valikule *Tõene*, **Field Service’i tootetüüp** on määratud valikule *Varud*.
- Kui suvand **Toote tüüp** on määratud valikule *Toode* ja **Toote ja kauba mudeligrupp** on määratud valikule *Väär*, **Field Service’i tootetüüp** on määratud valikule *Mitte-varud*.
- Kui suvand **Toote tüüp** on määratud valikule *Teenus*, **Field Service’i tootetüüp** on määratud valikule *Teenus*.

Lisaks sisaldab Dataverse loogikat, mis vastendab hankijaid seotud kontodega. See loogika määrab arve hankija vaikekonto. Loomisel määrab serveripoolne lisandmooduli loogika kontoga seotud hankija vaikekonto. Hankijal on viide arvekontole, mida kasutatakse selle väärtuse seadmiseks.

## <a name="supported-scenarios"></a>Toetatud stsenaariumid

- Ostutellimusi saavad luua ja uuendada Dataverse’i kasutajad. Samas protsessi ja andmeid juhitakse rakendusega Supply Chain Management. Supply Chain Managementis ostutellimuste veergude värskenduse piirangud rakenduvad siis, kui värskendused tulevad teenusest Field Service. Näiteks ei saa te ostutellimust uuendada, kui see on lõpetatud. 
- Kui ostutellimust juhitakse Supply Chain Managementi muudatuse haldusega, saab Field Service’i kasutaja ostutellimust värskendada ainult siis, kui Supply Chain Managementi kinnituse olekuks on *Mustand*.
- Mitut veergu haldab ainult Supply Chain Management ja neid ei saa Field Service’is uuendada. Et teada saada, milliseid veerge ei saa värskendada, vaadake toote vastendamise tabelit. Lihtsustamise huvides on enamik neist veergudest Dataverse’i lehtedel määratud kirjutuskaitstuks. 

    Näiteks haldab Supply Chain Management hinnateabe veerge. Supply Chain Managemenil on kaubanduslepped, mida Field Service saab kasutada. veerud, nagu **Ühiku hind**, **Allahindlus** ja **Netosumma**, tulevad ainult Supply Chain Managementist. Kindlustamaks, et hind oleks teenusega Field Service sünkroonitud, peaksite kasutama Dataverse’is **ostutellimuse** ja **ostutellimuse toote** lehtedel **sünkroonimise** funktsiooni, kui ostutellimuse andmed on sisestatud. Lisateavet vt [Nõudmisel Dynamics 365 Supply Chain Managementi hankeandmetega sünkroonimine](#sync-procurement).

- Veerg **Kogusummad** on saadaval ainult teenuses Field Service, kuna Supply Chain Managementis pole ostutellimusel ajavälist kogusummat. Supply Chain Managementi kogusummad arvutatakse mitme parameetri põhjal, mis pole Field Service’i puhul saadaval.
- Ostutellimuse ridu, kus on määratud ainult hankekategooria või kus määratud toode on teenuse tootetüübi *Teenus* või tootetüübi Field Service kaup, saab käivitada ainult Supply Chain Managementis. Seejärel sünkroonitakse read Dataverse’i ja need on Field Service’is nähtavad.
- Kui installitud on ainult Field Service, mitte Supply Chain Management, on ostutellimusel veerg **Ladu** kohustuslik. Kui aga Supply Chain Management on installitud, on see nõue täidetud, kuna Supply Chain Management võimaldab ostutellimuste ridu, kus teatud olukordades ei ole ladu määratud.
- Toote sissetulekuid (Dataverse’i ostutellimuste sissetulekuid) haldab Supply Chain Management ja neid ei saa luua, kui Supply Chain Management on Dataverse’i installitud. Supply Chain Managementist saadud toote sissetulekud sünkroonitakse Supply Chain Managementist Dataverse’i.
- Alatarne on Supply Chain Managementis lubatud. OneFSSCM-i lahendus lisab loogika nii, et kui toote sissetuleku rida (või ostutellimuse sissetuleku toode Dataverse’is) on loodud või värskendatud, luuakse varude töölehe rida järelejääva koguse korrigeerimiseks, mis on tellimisel alatarne Dataverse’i stsenaariumite korral.

## <a name="unsupported-scenarios"></a>Ilma toeta stsenaariumid

- Field Service takistab ridade lisamist tühistatud ostutellimusele Supply Chain Managementis. Lahendusena saate muuta ostutellimuse süsteemi olekut Field Service’is ja seejärel lisada uue rea kas Field Service’ile või Supply Chain Managementile.
- Kuigi hankeread mõjutavad varude tasemeid mõlemas süsteemis, ei taga integratsioon varude joondust Supply Chain Managementi ja Field Service’i üleselt. Nii Field Service kui Supply Chain Management omavad teisi protsesse, mis värskendavad varude tasemeid. Need protsessid on väljaspool hankeulatust.

## <a name="status-management"></a>Olekuhaldus

Ostutellimuste olekud Field Service’is erinevad olekutest Supply Chain Managementis.

### <a name="field-service-purchase-order-and-purchase-order-product-statuses"></a>Field Service’i ostutellimuse ja ostutellimuse toote olekud

| Päis – süsteemi olek | Päis – kinnitamise olek | Kauba olek |
|---|---|---|
| <ul><li>Mustand</li><li>Edastatud</li><li>Cancelled</li><li>Toode saadud</li><li>Arveldatud</li></ul> | <ul><li>Null</li><li>Kinnitatud</li><li>Tagasi lükatud</li></ul> | <ul><li>Ootel</li><li>Vastuvõetud</li><li>Cancelled</li></ul> |

### <a name="supply-chain-management-purchase-order-and-purchase-order-line-statuses"></a>Supply Chain Managementi ostutellimuse ja ostutellimuse rea olekud

Rea kinnitamise olekud on aktiivsed ainult siis, kui on olemas rea töövoog.

| Päis – dokumentide olek | Päis – kinnitamise olek | Rea olek | Rea kinnitamise olek |
|---|---|---|---|
| <ul><li>Avatud tellimus (tagasitellimus)</li><li>Vastuvõetud</li><li>Arveldatud</li><li>Cancelled</li></ul> | <ul><li>Mustand</li><li>Ülevaatamisel</li><li>Kinnitatud</li><li>Tagasi lükatud</li><li>Välisel läbivaatamisel</li><li>Kinnitatud</li><li>Lõpetatud</li></ul> | <ul><li>Avatud tellimus (tagasitellimus)</li><li>Vastuvõetud</li><li>Arveldatud</li><li>Cancelled</li></ul> | <ul><li>Edastamata</li><li>Ülevaatamisel</li><li>Kinnitatud</li><li>Tagasi lükatud</li></ul> |

Olekuveergudele rakendatakse järgmisi reegleid.

- Supply Chain Managementi olekut tarneahela haldamises ei saa teenusest Field Service värskendada. Samas mõnel juhul uuendatakse Field Service’i olekut siis, kui ostutellimuse olek Supply Chain Managementis muutub.
- Kui Supply Chain Managementi ostutellimus on muudatusehalduses ja muudatusi töödeldakse, on kinnituse olekuks *Mustand* või *Ülevaatusel*. Sellisel juhul määratakse Field Service’i kinnitamise olekuks *Null*.
- Kui ostutellimuse kinnitamise olek Supply Chain Managementis on määratud olekusse *Kinnitatud*, *Välisel ülevaatamisel*, *Kinnitatud* või *Lõpetatud*, seatakse Field Service’i ostutellimuse kinnituse olekuks *Kinnitatud*.
- Kui ostutellimuse kinnitamise olek Supply Chain Managementis on määratud olekusse *Tagasi lükatud*, seatakse Field Service’i ostutellimuse kinnituse olekuks *Tagasi lükatud*.
- Kui Supply Chain Managementis muudetakse dokumendi päise olekuks *Avatud tellimus (tagastustellimus)* ja Field Service’i ostutellimuse olekuks on *Mustand* või *Tühistatud*, muudetakse Field Service’i ostutellimuse olekuks *Esitatud*.
- Kui Supply Chain Managementis muudetakse dokumendi päise olekuks *Tühistatud* ja ühtegi välja Field Service’i ostutellimuste vastuvõtmise toodet ei seostata ostutellimusega (ostutellimuse toodete kaudu), on Field Service’i süsteemi olekuks seatud *Tühistatud*.
- Kui ostutellimuse rea olek Supply Chain Managementis on *Tühistatud*, seatakse ostutellimuse toote oleku Field Service’is olekule *Tühistatud*. Kui lisaks ostutellimuse rea olek Supply Chain Managementis muudetakse olekust *Tühistatud* olekule *Tagasitellimus*, on ostutellimuse toote kauba olekuks Field Service’is *Ootel*.

## <a name="sync-with-the-supply-chain-management-procurement-data-on-demand"></a><a id="sync-procurement"></a>Supply Chain Managementi hankeandmetega nõudmisel sünkroonimine

Supply Chain Management hõlmab hankeandmeid, mis töötlevad kaubandusleppeid, allahindlusi ja muid stsenaariume, mis toetuvad Supply Chain Managementi teisestele protsessidele. Hankemootor kasutab keerukaid reegleid antud ostutellimusele parima hinna määramiseks. Kui kasutate topeltkirjutust, ei hoita neid andmeid alati sünkroonis kahe keskkonna vahel, eriti stsenaariumides, kus rida loodi või uuendati Dataverse’is ja see võib käivitada Supply Chain Managementis järelprotsessid.

## <a name="sync-the-procurement-data-from-supply-chain-management"></a>Hankeandmete sünkroonimine Supply Chain Managementist

1. Avage Dataverse’is suvand **Varud \> Ostutellimus**.
2. Uue ostutellimuse loomiseks või olemasoleva ostutellimuse rea valimiseks valige **Uus**.
3. Ostutellimusest või ostutellimuse realt.
4. Valige tegevuspaanil nupp **Sünkrooni**.

Kõik Dataverse’i ja Field Service’i veerud, mida Supply Chain Managementiga jagatakse, sünkroonitakse.

Siin on olukorrad, kus te võite kasutada funktsiooni **Sünkroonimine**.

- Kui teete Dataverse’ist samal real mitu üksteisele järgnevat muudatust, käivitage funktsioon **Sünkroonimine**.
- Kui te pole kindel, kas muudatus võib olla Dataverse’is järjestuses teine muudatus, võib olla mõtet käivitada funktsioon **Sünkroonimine**.
- Kui saate Supply Chain Managementis väärtuse värskendamise kohta tõrketeate, käivitage funktsioon **Sünkroonimine** ja proovige seejärel Dataverse’i uuesti värskendada.

## <a name="cancelling-the-posting-process"></a>Sisestamisprotsessi tühistamine

Kui toote sissetuleku sisestamisprotsess on töötlemise ajal tühistatud, võib topeltkirjutus luua toote sissetuleku rea, kuid ei loo toote sissetuleku rida Dataverse’i tarneahela halduses. Selline olukord juhtub, kuna topeltkirjutus ei toeta jaotatud kandeid.

## <a name="templates"></a>Mallid

Järgmised mallid on saadaval hankega seotud dokumentidega integreerimiseks.

| Supply Chain Management | Field Service | Kirjeldus |
|---|---|---|
| Ostutellimuse päis V2 | msdyn\_Purchaseorders | See tabel sisaldab veerge, mis tähistavad ostutellimuse päist. |
| Ostutellimuse rea üksus | msdyn\_PurchaseOrderProducts | See tabel sisaldab ridu, mis tähistavad ostutellimuse ridu. Tootenumbrit kasutatakse sünkroonimiseks. See tuvastab toote varude arvestusühikuna (SKU), sh tootedimensioonid. Lisateavet toote Dataverse ’iga integreerimise kohta vt [Ühendatud toote kasutusfunktsionaalsus](product-mapping.md). |
| Toote sissetuleku päis | msdyn\_purchaseorderreceipts | See tabel sisaldab toote sissetuleku päiseid, mis luuakse toote sissetuleku sisestamisel Supply Chain Managementis. |
| Toote sissetuleku rida | msdyn\_purchaseorderreceiptproducts | See tabel sisaldab toote sissetuleku ridu, mis luuakse toote sissetuleku sisestamisel Supply Chain Managementis. |
| Ostutellimuse rea ajutiselt kustutatud üksus | msdyn\_purchaseorderproducts | See tabel sisaldab teavet ajutiselt kustutatud ostutellimuste ridade kohta. Ostutellimuse rea saab Supply Chain Managementis ajutiselt kustutada ainult siis, kui ostutellimus on kinnitatud või vastu võetud, kui muutuse haldamine on sisse lülitatud. Rida on Supply Chain Managementi andmebaasis olemas ja märgitud kui **IsDeleted**. Kuna Dataverse ei oma ajutiselt kustutamise kontseptsiooni, siis on oluline, et see teave oleks Dataverse’iga sünkroonitud. Sel viisil saab Supply Chain Managementis ajutiselt kustutatud read automaatselt Dataverse’ist kustutada. Sel juhul asub Dataverse’i rea kustutamise loogika Supply Chain Managementi laiendatud versioonis. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/productreceiptheader-msdyn-purchaseorderreceipts.md)]

[!include [Currency](includes/productreceiptline-msdyn-purchaseorderreceiptproducts.md)]

[!include [Currency](includes/purchaseorderheadersv2-msdyn-purchaseorders.md)]

[!include [Currency](includes/purchaseorderlinesoftdeletedtable-msdyn-purchaseorderproducts.md)]

[!include [Currency](includes/purchaseorderlinetable-msdyn-purchaseorderproducts.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]