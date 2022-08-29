---
title: Varude blokeerimine
description: Selles artiklis antakse ülevaade varude blokeerimisest, mis kuulub Supply Chain Managementi kvaliteedikontrolli protsessi hulka. Varude blokeerimist saab kasutada kaupade töötlemise või tarbimise vältimiseks.
author: yufeihuang
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 83b5417dc24af85f09e6713f2b12fdc358f61d54
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334681"
---
# <a name="inventory-blocking"></a>Varude blokeerimine

[!include [banner](../includes/banner.md)]

Selles artiklis antakse ülevaade varude blokeerimisest, mis kuulub Supply Chain Managementi kvaliteedikontrolli protsessi hulka. Varude blokeerimist saab kasutada kaupade töötlemise või tarbimise vältimiseks.

Laokaupade blokeerimiseks on järgmised võimalused.

- Käsitsi
- Kvaliteettellimust luues
- Kvaliteettellimust loovat protsessi kasutades
- Varude oleku blokeerimine

## <a name="blocking-items-manually"></a>Kaupade käsitsi blokeerimine

Saate blokeerida kaubakoguse, luues lehel **Varude blokeerimine** kande. Käsitsi saab blokeerida ainult neid kaupu, mis on saadaval vaba kaubavaruna. Käsitsi blokeeritud koguste puhul peate otsustama, kas plaanimistegevused sisaldavad eeldatava vaba kaubavaruna eeldatavaid sissetulekuid. Eeldatavad sissetulekud on blokeeritud kaubad, mille puhul eeldatakse, et need on pärast kontrolli lõpule viimist vabade kaubavarudena saadaval. Saate eeldatavat kuupäeva muuta. Vaikimisi on suvand **Eeldatavad sissetulekud** valitud kaupade puhul, mis on blokeeritud kvaliteettellimuse kaudu. Saate koguse käsitsi blokeerimise tühistada, kustutades kande lehelt **Varude blokeerimine**.

## <a name="blocking-items-by-creating-a-quality-order"></a>Kaupade blokeerimine kvaliteettellimust luues

Saate määrata kaubad, mida tuleb kontrollida, luues kvaliteettellimuse lehel **Kvaliteettellimused**. Kvaliteettellimuse loomisel blokeeritakse kogus, mille kauba kohta määrate. Kvaliteettellimusega seostatud valimiplaan juhib ainult nende kaupade kogust, mida tuleb kontrollida, mitte blokeeritud kaupade kogust. Kvaliteettellimusele sisestatud kogus on blokeeritud kogus olenemata kogusest, mille valimiplaan määrab kontrolli saamiseks. kogus blokeeritud kogus.

> [!NOTE]
> Nii partii aegumiskuupäeva kui ka varude oleku blokeerimise funktsioonide kasutamine pole koondplaneerimises toetatud. See võib põhjustada kaubavaru topeltvälistust, mis võib tekkida koondplaneerimise käigus. Soovitame teil aegunud partiide blokeerimisel toetuda varude oleku asemel partii likvideerimise koodidele.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Kaupade blokeerimine protsessiga, mis loob kvaliteettellimuse

Kui kvaliteediprotsess määrab, et kaupa tuleb kontrollida, blokeeritakse kauba kogus automaatselt. Seega, kui kvaliteeditellimus luuakse automaatselt, kontrollib kvaliteeditellimusega seotud kaupade valimi kava nii blokeeritud kaupade kui ka kontrollitavate koguste hulka. Kui lehel **Kauba valim** on valitud suvand **Täielik blokeerimine**, blokeeritakse kontrollimisel näiteks kogu ostutellimuse täielik kogus olenemata kaubavalimi kogusest.

### <a name="example"></a>Näide

Järgmises näites luuakse kvaliteettellimus ostutellimuse saatelehe sisestamisel. Lehel **Kvaliteediseosed** määrasite, et ostutellimuse saatelehe sisestamine on protsess, mis aktiveerib kvaliteettellimuse.

|Häälestamine |Kasutaja tegevus |Tulemus |
|----|---|---|
| Kvaliteediseos määrab, et ostutellimuse saatelehe sisestamisel tuleb luua kvaliteettellimus. Kvaliteettellimuse kauba valimi seadistus määrab, et kontrollida tuleb 10 protsenti ostutellimuse rea kogusest. Ning kuna kauba valimi seadistuses on valitud suvand **Täielik blokeerimine**, tuleb ostutellimuse rea täielik kogus kontrollimisel blokeerida olenemata kontrollimiseks saadetud kogusest. | Saateleht on sisestatud. | Kvaliteettellimus on loodud. Kümme protsenti kauba ostutellimuse kogusest on saadetud kontrolli. Ostutellimuse rea täielik kogus on blokeeritud. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Kaupade blokeerimine varude oleku blokeerimine

Saate määrata, millised varude olekud on blokeerivad olekud, kasutades lehe **Varude olekud parameetrit** **Varude blokeerimine**.  Varude olekuid ei saa kasutada blokeerivate olekutena tootmistellimuste, müügitellimuste, üleviimistellimuste, väljaminevate kannete ega projekti integreerimise puhul. Väljamineva töö jaoks kasutage saadaoleva varude olekuga kaupu. Kui kaupade olek on **Katki** ja neile kaupadele tehakse koondplaneerimine, loetakse need kaubad puuduvateks ning varusid täiendatakse automaatselt.

## <a name="take-care-when-blocking-items-that-use-both-inventory-status-blocking-and-quality-order-blocking"></a>Olge hoolikad kaupade blokeerimisel, mis kasutavad nii varude oleku blokeerimist kui ka kvaliteettellimuse blokeerimist

Saate luua kvaliteettellimuse, mis on seotud varudega, millel on lubatud olek **varude blokeerimine**. Sel juhul loob kvaliteettellimus lisaks varude oleku poolt loodud kirjele ka täiendava varude blokeerimise kirje. Kuna kvaliteettellimuse varude blokeerimisel on lubatud parameeter **Eeldatavad laekumised**, loob see täiendava *Tellitud varud* kande, mis on samuti blokeeritud varude oleku poolt. See kombinatsioon võib põhjustada raskusi loodud varude kannete tähenduse mõistmisel, sest on näha, nagu ületaks blokeeritud kogukogus kogu vaba kaubavaru. Uurime kandeid näite põhjal, mis sisaldab kauba A0001 10 ühiku laekumise kui kvaliteettellimus loodi 1 ühiku näidiseks. Käitumine sõltub ka sellest, kas suvand **Reserveeri tellitud kaubad** on lubatud **varud ja laohalduse parameetrid** lehel.

>[!NOTE]
>Kui kasutate koos varude oleku blokeerimist ja kvaliteettellimusi, soovitame tungivalt, et suvand **Reserveeri tellitud kaubad** oleks lubatud.

### <a name="example-with-reserve-ordered-items-enabled"></a>Näide, kus "Reserveeri tellitud kaubad" on lubatud

Kui **Reserveeri tellitud kaubad** on lubatud, on kõikide varude blokeerimise kannete olek kas *Füüsiliselt reserveeritud* või *Reserveeritud-tellitud*.

| Laokande viide | Sissetulek | Väljasta | Kogus | Laoala | Ladu | Lao olek | Koht | Litsentsiplaat | Kommentaar |
|---|---|---|---|---|---|---|---|---|---|
| Ostutellimus | Ostetud | | 10 tk | 2 | 24 | Blokeerimine | RECV | receiptLp1 | | 
| Varude blokeerimine | | Füüsiliselt reserveeritud | -9 tk | 2 | 24 | Blokeerimine | | | Varude oleku blokeerimise loodud kanne |
| Varude blokeerimine | | Füüsiliselt reserveeritud | -1 tk | 2 | 24 | Blokeerimine | RECV | receiptLp1 | Kvaliteettellimuse valimi blokeerimise loodud kanne |
| Varude blokeerimine | Tellitud | | 1 tk | 2 | 24 | Blokeerimine | RECV | receiptLp1 | Kvaliteettellimuse valimi blokeerimise eeldatavad laekumised |
| Varude blokeerimine | | Reserveeritud tellitud | 1 tk | 2 | 24 | Blokeerimine | | | Varude oleku blokeerimise loodud kanne

### <a name="example-with-reserve-ordered-items-disabled"></a>Näide, kus "Reserveeri tellitud kaubad" ei ole lubatud

Kui **Reserveeri tellitud kaubad** on keelatud, ei saa eeldatavaid laekumisi reserveerida, kuna nende olek on *Tellitud*, seega jääb mõni blokeerimine olekusse *Tellimisel*.

| Laokande viide | Sissetulek | Väljasta | Kogus | Laoala | Ladu | Varude olek | Koht | Numbrimärk | Kommentaar |
|---|---|---|---|---|---|---|---|---|---|
| Ostutellimus | Ostetud | | 10 tk | 2 | 24 | Blokeerimine | RECV | receiptLp1 | |
| Varude blokeerimine | | Füüsiliselt reserveeritud | -9 tk | 2 | 24 | Blokeerimine | | | Varude oleku blokeerimise loodud kanne |
| Varude blokeerimine | | Füüsiliselt reserveeritud | -1 tk | 2 | 24 | Blokeerimine | RECV | receiptLp1 | Kvaliteettellimuse valimi blokeerimise loodud kanne |
| Varude blokeerimine | Tellitud | | 1 tk | 2 | 24 | Blokeerimine | RECV | receiptLp1 | Kvaliteettellimuse valimi blokeerimise eeldatavad laekumised |
| Varude blokeerimine | | Tellimusel | 1 tk | 2 | 24 | Blokeerimine | RECV | receiptLp1 | Varude oleku blokeerimise loodud kanne

Pange tähele kahe juhtumi vahelist erinevust kande olekus ja dimensioonides. Seetõttu soovitame lubada suvandi **Reserveeri tellitud kaubad**.

## <a name="disable-expected-receipts-from-quality-orders-that-sample-blocked-inventory"></a>Keelake oodatud kviitungid kvaliteettellimustest, mille valim on blokeeritud varudes

Varude kannete lihtsustamiseks kvaliteettellimuste korral, mille varude oleku tagajärjeks on blokeeritud varud, annab süsteem funktsiooni, mis keelab sellistelt kvaliteettellimustelt oodatavad sissetulekud. Kuna varude oleku blokeerimine blokeerib eeldatava sissetuleku kohe, siis selle muudatuse tõttu vaba kaubavaru ei vähendata.

Selle funktsiooni kasutamiseks peab see olema teie süsteemi jaoks sisse lülitatud. Tarneahela halduse versiooni 10.0.29 puhul lülitatakse funktsioon vaikimisi sisse. Administraatorid saavad selle funktsiooni sisse või välja lülitada, *otsides* keelake eeldatud sissetulekud kvaliteettellimustest, mis blokeerisid lao näidised funktsioonihalduse [tööruumis](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="additional-resources"></a>Lisaressursid

[Varude blokeerimise loomine ja haldamine](tasks/create-maintain-inventory-blocking.md)

[Kvaliteedijuhtimise protsessid](quality-management-processes.md)

[Kaupade kvaliteedi kontrollimine](tasks/inspect-quality-goods.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]