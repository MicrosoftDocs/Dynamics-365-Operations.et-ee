---
title: Vahelaoorderid
description: See artikkel kirjeldab vahelaoorderite kasutamist varude blokeerimiseks.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: a6bd487e602a57272ea2943441ea4b78129b3f8d
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="quarantine-orders"></a>Vahelaoorderid

[!include[banner](../includes/banner.md)]


See artikkel kirjeldab vahelaoorderite kasutamist varude blokeerimiseks. 

Vahelaoordereid saab kasutada varude blokeerimiseks. Näiteks võib olla vaja kvaliteedikontrolliks kaubad vahelattu paigutada. Karantiinis olevad kaubad edastatakse vahelattu. **Märkus:** täpsema laohalduse protsesside kasutamisel (laohalduse moodulis) kasutatakse vahelao tellimuse töötlemist ainult müügi tagastustellimuste puhul.

## <a name="quarantine-onhand-inventory-items"></a>Vabade laokaupade paigutamine vahelattu
Kui saadate kaubad vahelattu, saate luua vahelaoorderid käsitsi või seadistada süsteemi looma sissetuleva töötluse ajal vahelaoordereid automaatselt. Vahelaoorderite automaatseks loomiseks tehke valik **Vahelao haldus** vahekaardil **Varude poliitikad** lehel **Kauba mudeligrupid**. Peate määrama vastuvõtvatele ladudele ka vaikevahelao väljal **Vaheladu**. Kaubad pannakse Microsoft Dynamics 365 for Operationsis automaatselt vahelattu, kui füüsiliselt vaba kaubavaru tootmistellimusel või ostutellimusel salvestatakse. Selline liikumine toimub, kuna vahelaoorderi olekuks määratakse **Alustatud**. Kui loote vahelaoorderid käsitsi, ei pea kaupa seotud kauba mudeligrupis vahelao halduseks seadistama. Selle protsessi jaoks peate määrama vaba kaubavaru, mis tuleks vahelattu paigutada, ja kasutatava vahelao. Protsessi plaanimisel saate kasutada abivahendina vahelaoorderi olekuid.

## <a name="quarantine-order-statuses"></a>Vahelaoorderi olekud
Vahelaoorderite olek võib olla järgmine:

-   Loodud
-   Alustatud
-   Lõpetamine kinnitatud
-   Lõpetatud

### <a name="created"></a>Loodud

Kui vahelaoorder on loodud käsitsi, kuid kaup ei ole veel vahelattu pandud, siis on vahelaoorderi olek **Loodud**. Luuakse kaks laokannet. Üks kanne on väljaminekukanne, mille olek võib olla **Tellimusel**, **Füüsiliselt reserveeritud** või**Komplekteeritud**. Teine kanne on sissetulekukanne, mille olek võib vahelaos olla **Tellitud** või**Registreeritud**. Saate reserveerida, komplekteerida ja registreerida varude värskendusi tavaliste protsesside abil.

### <a name="started"></a>Alustatud

Kui vahelaoorderi oleks on **Alustatud**, edastatakse varud tavalisest laost vahelattu ja luuakse kaks laokannet. Ühe kande olek on **Maha arvatud** ja teise kande olek on **Vastu võetud**. Samal ajal luuakse kaks laokannet tagastuse käsitlemiseks. Need kanded ei ole kuupäevaga. Ühe kande olek on **Füüsiliselt reserveeritud** ja teise kande olek on **Tellitud**.

### <a name="reported-as-finished"></a>Lõpetamine kinnitatud

Kui klõpsate nuppu **Kinnita lõpetamine**, saate kinnitada alustatud vahelaoorder lõpetamise. Kaup on vahelaost väljastatud, kuid ei ole veel tavalisse lattu tagasi viidud. Tavalisse lattu tagasiviimist saab töödelda saabuva kauba töölehe kaudu, mille saab käivitada lõpetatuna kinnitamise protsessi ajal.

### <a name="ended"></a>Lõpetatud

Kui vahelaoorder lõppeb, viiakse kaup vahelaost tagasi tavalisse lattu. Kauba kande olekuks on vahelaos **Müüdud** ja tavalises laos **Ostetud**.

## <a name="quarantine-order-scrap"></a>Vahelaoorderi praak
Vahelaoorderi protsessi osana on võimalik ka varusid praakida. Praagi töötlemisel määratakse vahelao väljaminekukandega varude olekuks **Müüdud**.

<a name="see-also"></a>Vt ka
--------

[Varude blokeerimine](inventory-blocking.md)




