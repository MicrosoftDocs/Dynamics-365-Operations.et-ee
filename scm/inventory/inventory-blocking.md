---
title: Varude blokeerimine
description: "See artikkel annab ülevaate varude blokeerimisest, mis kuulub Microsoft Dynamics AX-i kvaliteedikontrolli protsessi hulka. Varude blokeerimist saab kasutada kaupade töötlemise või tarbimise vältimiseks."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 0d7e37de63e6c63b5d7942a84de60ef8f3984cde
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-blocking"></a>Varude blokeerimine

[!include[banner](../includes/banner.md)]


See artikkel annab ülevaate varude blokeerimisest, mis kuulub Microsoft Dynamics AX-i kvaliteedikontrolli protsessi hulka. Varude blokeerimist saab kasutada kaupade töötlemise või tarbimise vältimiseks.

Laokaupade blokeerimiseks on järgmised võimalused.
-   Käsitsi
-   Kvaliteettellimust luues
-   Kvaliteettellimust loovat protsessi kasutades
-   Varude oleku blokeerimine

## <a name="blocking-items-manually"></a>Kaupade käsitsi blokeerimine
Saate blokeerida kaubakoguse, luues lehel **Varude blokeerimine** kande. Käsitsi saab blokeerida ainult neid kaupu, mis on saadaval vaba kaubavaruna. Käsitsi blokeeritud koguste puhul peate otsustama, kas plaanimistegevused sisaldavad eeldatava vaba kaubavaruna eeldatavaid sissetulekuid. Eeldatavad sissetulekud on blokeeritud kaubad, mille puhul eeldatakse, et need on pärast kontrolli lõpule viimist vabade kaubavarudena saadaval. Saate eeldatavat kuupäeva muuta. Vaikimisi on suvand **Eeldatavad sissetulekud** valitud kaupade puhul, mis on blokeeritud kvaliteettellimuse kaudu. Saate koguse käsitsi blokeerimise tühistada, kustutades kande lehelt **Varude blokeerimine**.

## <a name="blocking-items-by-creating-a-quality-order"></a>Kaupade blokeerimine kvaliteettellimust luues
Saate määrata kaubad, mida tuleb kontrollida, luues kvaliteettellimuse lehel **Kvaliteettellimused**. Kvaliteettellimuse loomisel blokeeritakse kogus, mille kauba kohta määrate. Kvaliteettellimusega seostatud valimiplaan juhib ainult nende kaupade kogust, mida tuleb kontrollida, mitte blokeeritud kaupade kogust. Kvaliteettellimusele sisestatud kogus on blokeeritud kogus olenemata kogusest, mille valimiplaan määrab kontrolli saamiseks. kogus blokeeritud kogus.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Kaupade blokeerimine protsessiga, mis loob kvaliteettellimuse
Kui kvaliteediprotsess määrab, et kaupa tuleb kontrollida, blokeeritakse kauba kogus automaatselt. Seega kui kvaliteettellimus luuakse automaatselt, juhib kvaliteettellimusega seostatud kauba valimiplaan nii blokeeritud kaupade kogust kui ka kontrollitavate kaupade kogust. Kui lehel **Kauba valim** on valitud suvand **Täielik blokeerimine**, blokeeritakse kontrollimisel näiteks kogu ostutellimuse täielik kogus olenemata kaubavalimi kogusest.
### <a name="example"></a>Näide

Järgmises näites luuakse kvaliteettellimus ostutellimuse saatelehe sisestamisel. Lehel **Kvaliteediseosed** määrasite, et ostutellimuse saatelehe sisestamine on protsess, mis aktiveerib kvaliteettellimuse.

|Häälestamine                                                                     |Kasutaja tegevus                 |Tulemus             |
|--------------------------------------------------------------------------|----------------------------|-------------------|
| Kvaliteediseos määrab, et ostutellimuse saatelehe sisestamisel tuleb luua kvaliteettellimus. Kvaliteettellimuse kauba valimi seadistus määrab, et kontrollida tuleb 10 protsenti ostutellimuse rea kogusest. Ning kuna kauba valimi seadistuses on valitud suvand **Täielik blokeerimine**, tuleb ostutellimuse rea täielik kogus kontrollimisel blokeerida olenemata kontrollimiseks saadetud kogusest. | Saateleht on sisestatud. | Kvaliteettellimus on loodud. Kümme protsenti kauba ostutellimuse kogusest on saadetud kontrolli. Ostutellimuse rea täielik kogus on blokeeritud. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Kaupade blokeerimine varude oleku blokeerimine
Saate määrata, millised varude olekud on blokeerivad olekud, kasutades lehe **Varude olekud parameetrit** **Varude blokeerimine**.  Varude olekuid ei saa kasutada blokeerivate olekutena tootmistellimuste, müügitellimuste, üleviimistellimuste, väljaminevate kannete ega projekti integreerimise puhul. Väljamineva töö jaoks kasutage saadaoleva varude olekuga kaupu. Kui kaupade olek on **Katki** ja neile kaupadele tehakse koondplaneerimine, loetakse need kaubad puuduvateks ning varusid täiendatakse automaatselt.



<a name="see-also"></a>Vt ka
--------

[Varude blokeerimise loomine ja haldamine (tegevuse juhis)](https://ax.help.dynamics.com/en/wiki/create-and-maintain-an-inventory-blocking/)

[Kvaliteedijuhtimise protsessid](quality-management-processes.md)

[Kaupade kvaliteedi kontrollimine (tegevuse juhis)](https://ax.help.dynamics.com/en/wiki/inspect-the-quality-of-goods/)



