---
title: Vahelaoorderid
description: See teema kirjeldab vahelaoorderite kasutamist varude blokeerimiseks.
author: perlynne
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a44909a7880b0cd53e39ccbadf8b79ae5c9dafc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834213"
---
# <a name="quarantine-orders"></a>Vahelaoorderid

[!include [banner](../includes/banner.md)]

See teema kirjeldab vahelaoorderite kasutamist varude blokeerimiseks.

Vahelaoordereid saab kasutada varude blokeerimiseks. Näiteks võib olla vaja kvaliteedikontrolliks kaubad vahelattu paigutada. Karantiinis olevad kaubad edastatakse vahelattu. **Märkus:** täpsema laohalduse protsesside kasutamisel (laohalduse moodulis) kasutatakse vahelao tellimuse töötlemist ainult müügi tagastustellimuste puhul.

## <a name="quarantine-on-hand-inventory-items"></a>Vabade laokaupade paigutamine vahelattu
Kui saadate kaubad vahelattu, saate luua vahelaoorderid käsitsi või seadistada süsteemi looma sissetuleva töötluse ajal vahelaoordereid automaatselt. Vahelaoorderite automaatseks loomiseks tehke valik **Vahelao haldus** vahekaardil **Varude poliitikad** lehel **Kauba mudeligrupid**. Peate määrama vastuvõtvatele ladudele ka vaikevahelao väljal **Vaheladu**. Kaubad pannakse Supply Chain Managementis automaatselt vahelattu, kui füüsiliselt vaba kaubavaru tootmistellimusel või ostutellimusel salvestatakse. Selline liikumine toimub, kuna vahelaoorderi olekuks määratakse **Alustatud**. Kui loote vahelaoorderid käsitsi, ei pea kaupa seotud kauba mudeligrupis vahelao halduseks seadistama. Selle protsessi jaoks peate määrama vaba kaubavaru, mis tuleks vahelattu paigutada, ja kasutatava vahelao. Protsessi plaanimisel saate kasutada abivahendina vahelaoorderi olekuid.

## <a name="quarantine-order-statuses"></a>Vahelaoorderi olekud
Vahelaoorderite olek võib olla järgmine:

-   Loodud
-   Alustatud
-   Lõpetamine kinnitatud
-   Lõpetatud

### <a name="created"></a>Loodud

Kui vahelaoorder on loodud käsitsi, kuid kaup ei ole veel vahelattu pandud, siis on vahelaoorderi olek **Loodud**. Luuakse kaks laokannet. Üks kanne on väljaminekukanne, mille olek võib olla **Tellimusel**, **Füüsiliselt reserveeritud** või **Komplekteeritud**. Teine kanne on sissetulekukanne, mille olek võib vahelaos olla **Tellitud** või **Registreeritud**. Saate reserveerida, komplekteerida ja registreerida varude värskendusi tavaliste protsesside abil.

### <a name="started"></a>Alustatud

Kui vahelaoorderi oleks on **Alustatud**, edastatakse varud tavalisest laost vahelattu ja luuakse kaks laokannet. Ühe kande olek on **Maha arvatud** ja teise kande olek on **Vastu võetud**. Samal ajal luuakse kaks laokannet tagastuse käsitlemiseks. Need kanded ei ole kuupäevaga. Ühe kande olek on **Füüsiliselt reserveeritud** ja teise kande olek on **Tellitud**.

### <a name="reported-as-finished"></a>Lõpetamine kinnitatud

Kui klõpsate nuppu **Kinnita lõpetamine**, saate kinnitada alustatud vahelaoorder lõpetamise. Kaup on vahelaost väljastatud, kuid ei ole veel tavalisse lattu tagasi viidud. Tavalisse lattu tagasiviimist saab töödelda saabuva kauba töölehe kaudu, mille saab käivitada lõpetatuna kinnitamise protsessi ajal.

### <a name="ended"></a>Lõpetatud

Kui vahelaoorder lõppeb, viiakse kaup vahelaost tagasi tavalisse lattu. Kauba kande olekuks on vahelaos **Müüdud** ja tavalises laos **Ostetud**.

## <a name="quarantine-order-scrap"></a>Vahelaoorderi praak
Vahelaoorderi protsessi osana on võimalik ka varusid praakida. Praagi töötlemisel määratakse vahelao väljaminekukandega varude olekuks **Müüdud**.

<a name="additional-resources"></a>Lisaressursid
--------

[Varude blokeerimine](inventory-blocking.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]