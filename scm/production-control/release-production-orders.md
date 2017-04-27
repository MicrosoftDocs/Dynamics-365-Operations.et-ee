---
title: "Tootmistellimuste väljastamine"
description: "Väljastatud tootmistellimus on tellimus, millele on antud tootmiseks luba. Mõistet „väljastatud” kasutatakse tootmistellimuse töötsükli sellise oleku kirjeldamiseks, kus tootmistellimus on saadaval saadaval tootmistöödel ja laoprotsessides täitmiseks."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c4ebedab6d7de62479d3bc80583afadbe780aac4
ms.lasthandoff: 03/31/2017


---

# <a name="release-production-orders"></a>Tootmistellimuste väljastamine

[!include[banner](../includes/banner.md)]


Väljastatud tootmistellimus on tellimus, millele on antud tootmiseks luba. Mõistet „väljastatud” kasutatakse tootmistellimuse töötsükli sellise oleku kirjeldamiseks, kus tootmistellimus on saadaval saadaval tootmistöödel ja laoprotsessides täitmiseks. 

<a name="characteristics-of-the-released-state"></a>Väljastatud oleku omadused
-------------------------------------

Olek **Väljastatud** on üks olek tootmistellimuse tsüklis. Tootmistellimused, mille olek on **Väljastatud** on saadaval tootmistöödel ja laoprotsessides täitmiseks. Olekul **Väljastatud** on järgmised tunnused.

-   Tootmistellimuse saab seada olekusse **Väljastatud** kas tootmistellimuselt või pakktöötluse abil. Tootmistellimuse saab ka automaatselt värskendada plaanitud tootmistellimustelt, mis on kinnitatud lehe **Kinnituse ajapiir** väljaga **Koondplaan**.
-   Olek **Väljastatud** on märguanne tööde operaatoritele, et tööde juhtimise moodulis tuleb käivitada tootmistööd.
-   Tootmisdokumendid, näiteks protsessikaardid, protsessitööd ja töökaardid pakuvad teavet tootmistööde kohta ja neid saab väljastada.
-   Füüsiliselt reserveeritud materjalide puhul luuakse laotöö materjalide komplekteerimiseks tootmistellimuse jaoks.

## <a name="releasing-jobs-to-the-shop-floor"></a>Tööde väljastamine tööde juhtimisse
Kui tootmistellimus on väljastatud, on tellimusega seotud tootmistööd nähtaval ja registreerimiseks valmis. Operaatorid saavad teha tööde registreerimisi, nagu Käivita, Peata ja Lõpetamine, kas lehel **Töökaardi terminal** või **Töökaardi seade**. Registreeritud aeg ja kogus kantakse registreerimislehtedelt automaatselt üle tootmise töölehtedele, et jälgida tarbitud aega ja kogust.

## <a name="route-cards"></a>Protsessi kaardid
Protsessikaart annab ülevaate teabest, mis on pärit protsessi ja operatsiooni seadistustest ning operatsiooni ja töö planeerimise meetoditest.

## <a name="route-jobs"></a>Protsessi tööd
Protsessitöö loetleb kõik operatsiooni tööd üksikasjalikult ning hõlmab seadistus-, protsessi-, järjekorra- ja transpordiaegu. Näiteks võib selline operatsioon nagu värvimine vajada eraldi töid, nagu seadistusaeg, käitusaeg (värvimisprotsessi jaoks) ja järjekorraaeg (kuivamiseks).

## <a name="job-cards"></a>Töökaardid
Töökaart loetleb konkreetse operatsiooni üksiktööde numbrid. Igal lehel kuvatakse üks töö. Töökaardile kaasatud tööd ja nende nende prognoositavad ajad on pärit protsessi ja operatsiooni seadistusteabest. Töökaardilt saate avada lehe **Tootmise töölehe read**, **töökaart **. Operatsiooniressursse käitavad inimesed saavad tootmisprotsessi kohta tagasisidet anda. On olemas väljad, kuhu saate sisestada tarbimisstatistika ja teabe, nt tõrgete koguse.

## <a name="warehouse-work-for-raw-material-picking"></a>Laotöö materjali komplekteerimiseks.
Töö toormaterjalide komplekteerimiseks luuakse väljastamise ajal. Töö luuakse ainult enne tellimuse väljastamist tootmistellimuse jaoks füüsiliselt reserveeritud materjalide koguse kohta. Toormaterjalide komplekteerimise jaoks laotöö loomiseks on nõutav järgmine seadistus.

-   Asukohakorraldus toormaterjalide komplekteerimiseks, mis määratleb, millisesse lao asukohta tuleb materjalid komplekteerida
-   Voomall toormaterjalide kohta, kus on konfigureeritud laotöö käivitamise poliitikad
-   Tootmise sisendasukoht, mis määratleb, kuhu materjalid pannakse





