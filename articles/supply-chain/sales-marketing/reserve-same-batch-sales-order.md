---
title: "Sama partii reserveerimine müügitellimuse jaoks"
description: "Selles artiklis selgitatakse, kuidas seadistada toodet lubama varude reserveerimist üksiku varude partii suhtes."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8e0f8f85609e7c3095f13738d43cdf5734018eaa
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="reserve-the-same-batch-for-a-sales-order"></a>Sama partii reserveerimine müügitellimuse jaoks

[!include[banner](../includes/banner.md)]


Selles artiklis selgitatakse, kuidas seadistada toodet lubama varude reserveerimist üksiku varude partii suhtes.

Sama partii reserveerimisel saate reserveerida müügitellimuse rea varusid ühe varupartii suhtes. Näiteks võib tapeeti telliv klient soovida, et kogu tellimus täidetaks samast partiist, et vältida rullidevahelist erinevust. Toote seadistamiseks nii, et kasutataks sama partii reserveerimist, peavad järgmised sätted olema tootele määratavas kauba mudeligrupis, jälgimisdimensioonide grupis ja laoala dimensioonigrupis aktiivsed.

-   **Kauba mudeligrupid** – kauba mudeligrupil peavad olema varude poliitikate väljagrupis **Reserveerimine** valitud väljad **Sama partii valimine** ja **Konsolideeri vajadus**.
-   **Jälgimisdimensioonide grupid** – jälgimisdimensiooni grupil peab olema partiinumbri puhul valitud väli **Laovarude planeerimine dimensioonide kaupa**.
-   **Laodimensioonide grupid** – laodimensiooni grupil peab olema väljadele **Laoala** ja **Ladu** valitud väli **Laovarude planeerimine dimensioonide kaupa**.

Kui reserveerite sama partii valikuga müügitellimuse real olevale tootele varusid, püüab Finance and Operations reserveerida tellitud kogust ühest varude partiist. Arvestatakse ka konkreetse partii atribuudi nõudeid. Kui kogust ei saa ühest partiist täita, kuvatakse leht **Sama partii reserveerimise konflikt**. See leht kirjeldab probleeme ja ka tegevusi, mida saate reserveerimise jätkamiseks teha. Järgmised tingimused võivad partii reserveerimist takistada.

-   Partii likvideerimiskoodil on müügi väljal **Blokeeri reserveering** lipp **Blokeeritud**.
-   Partii on aegumiskuupäeva ja kehtivate kliendi müümispäevade alusel aegunud. Kaupa saab siiski reserveerimisel arvestada, kui kauba mudeligrupp on selle kauba puhul arvestatakse „esimesena aegunud esimesena välja” (FEFO) kuupäeva ja kui komplekteerimise kriteeriumina on valitud parim-enne kuupäev.
-   Partiil pole jäänud järele piisavalt kõlblikkusaja päevi, tuginedes aegumiskuupäevale ja parim-enne kuupäevale, millele on liidetud kliendi müümispäevad.





