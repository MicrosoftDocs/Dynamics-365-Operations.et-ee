---
title: "Sama partii reserveerimine müügitellimuse jaoks"
description: "Selles artiklis selgitatakse, kuidas seadistada toodet lubama varude reserveerimist üksiku varude partii suhtes."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 2f82d8bf65dcb421420eabbfe9f4c4ef0332b1cc
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="reserve-the-same-batch-for-a-sales-order"></a>Sama partii reserveerimine müügitellimuse jaoks

[!include[banner](../includes/banner.md)]


Selles artiklis selgitatakse, kuidas seadistada toodet lubama varude reserveerimist üksiku varude partii suhtes.

Sama partii reserveerimisel saate reserveerida müügitellimuse rea varusid ühe varupartii suhtes. Näiteks võib tapeeti telliv klient soovida, et kogu tellimus täidetaks samast partiist, et vältida rullidevahelist erinevust. Toote seadistamiseks nii, et kasutataks sama partii reserveerimist, peavad järgmised sätted olema tootele määratavas kauba mudeligrupis, jälgimisdimensioonide grupis ja laoala dimensioonigrupis aktiivsed.

-   **Kauba mudeligrupid** – kauba mudeligrupil peavad olema varude poliitikate väljagrupis **Reserveerimine** valitud väljad **Sama partii valimine** ja **Konsolideeri vajadus**.
-   **Jälgimisdimensioonide grupid** – jälgimisdimensiooni grupil peab olema partiinumbri puhul valitud väli **Laovarude planeerimine dimensioonide kaupa**.
-   **Laodimensioonide grupid** – laodimensiooni grupil peab olema väljadele **Laoala** ja **Ladu** valitud väli **Laovarude planeerimine dimensioonide kaupa**.

Kui reserveerite sama partii valikuga müügitellimuse real olevale tootele varusid, püüab Microsoft Dynamics 365 for Operations reserveerida tellitud kogust ühest varude partiist. Arvestatakse ka konkreetse partii atribuudi nõudeid. Kui kogust ei saa ühest partiist täita, kuvatakse leht **Sama partii reserveerimise konflikt**. See leht kirjeldab probleeme ja ka tegevusi, mida saate reserveerimise jätkamiseks teha. Järgmised tingimused võivad partii reserveerimist takistada.

-   Partii likvideerimiskoodil on müügi väljal **Blokeeri reserveering** lipp **Blokeeritud**.
-   Partii on aegumiskuupäeva ja kehtivate kliendi müümispäevade alusel aegunud. Kaupa saab siiski reserveerimisel arvestada, kui kauba mudeligrupp on selle kauba puhul arvestatakse „esimesena aegunud esimesena välja” (FEFO) kuupäeva ja kui komplekteerimise kriteeriumina on valitud parim-enne kuupäev.
-   Partiil pole jäänud järele piisavalt kõlblikkusaja päevi, tuginedes aegumiskuupäevale ja parim-enne kuupäevale, millele on liidetud kliendi müümispäevad.





