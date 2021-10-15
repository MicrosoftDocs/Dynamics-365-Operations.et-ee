---
title: Vahelaoorderid
description: See teema kirjeldab garantiitellimuste kasutamist varude blokeerimiseks.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5cf0ec8f9f4d862724cb8ab72b48771ed68eaf39
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568779"
---
# <a name="quarantine-orders"></a>Vahelaoorderid

[!include [banner](../includes/banner.md)]

See teema kirjeldab garantiitellimuste kasutamist varude blokeerimiseks.

Garantiitellimused lasevad teil varud blokeerida. Näiteks võib olla vaja kvaliteedikontrolliks kaubad vahelattu paigutada. Karantiinis olevad kaubad edastatakse vahelattu.

> [!NOTE]
> Edasijõudnud laohalduse protsesside kasutamisel (laohalduse moodulis) kasutatakse garantiitellimuse töötlemist ainult müügi tagastustellimuste puhul.

## <a name="quarantine-on-hand-inventory-items"></a>Vabade laokaupade paigutamine vahelattu

Kaupade garantiisse saatmisel saate kas käsitsi luua garantiitellimused või seadistada süsteemi neid sissetuleva töötluse ajal automaatselt looma.

Süsteemi automaatseks garantiitellimuste loomiseks järgige neid samme.

1. Avage **Varude haldus \> Seadistus \> Varud \> Kauba mudeligrupid**.
1. Valige loendist olemasolev mudelgrupp või looge uus mudelgrupp.
1. Valige kiirkaardil **Varude poliitikad** märkeruut **Garantiihaldus**.
1. Sulgege leht.
1. Peate määrama vastuvõtvatele ladudele ka vaikegarantiilao väljal **Garantiiladu**.

Kui laos vastuvõetuna registreeritud kaup kuulub mudelirühma, kus on valitud märkeruut **Garantii haldus**, genereerib süsteem selle jaoks garantiitellimuse. Garantiitellimus annab töötajatele korralduse viia toode garantiilattu.

Kui loote garantiitellimusi käsitsi **Garantiitellimused** lehel, ei pea kaup olema seotud kauba mudelirühmas garantii haldamiseks seadistatud. Selle protsessi jaoks peate määrama vaba kaubavaru, mis tuleks vahelattu paigutada, ja kasutatava vahelao. Protsessi plaanimisel saate kasutada abivahendina vahelaoorderi olekuid.

## <a name="quarantine-order-statuses"></a>Vahelaoorderi olekud

Vahelaoorderite olek võib olla järgmine:

- Loodud
- Alustatud
- Lõpetamine kinnitatud
- Lõpetatud

### <a name="created"></a>Loodud

Kui vahelaoorder on loodud käsitsi, kuid kaup ei ole veel vahelattu pandud, siis on vahelaoorderi olek **Loodud**. Luuakse kaks laokannet. Üks kanne on väljaminekukanne, mille olek võib olla **Tellimusel**, **Füüsiliselt reserveeritud** või **Komplekteeritud**. Teine kanne on sissetulekukanne, mille olek võib vahelaos olla **Tellitud** või **Registreeritud**. Saate reserveerida, komplekteerida ja registreerida varude värskendusi tavaliste protsesside abil.

### <a name="started"></a>Alustatud

Kui vahelaoorderi oleks on **Alustatud**, edastatakse varud tavalisest laost vahelattu ja luuakse kaks laokannet. Ühe kande olek on **Maha arvatud** ja teise kande olek on **Vastu võetud**. Samal ajal luuakse kaks laokannet tagastuse käsitlemiseks. Need kanded ei ole kuupäevaga. Ühe kande olek on **Füüsiliselt reserveeritud** ja teise kande olek on **Tellitud**.

### <a name="reported-as-finished"></a>Lõpetamine kinnitatud

Alustatud garantiitellimuse lõpetatuks märkimiseks avage tellimus ja tehke tegevuspaanil valik **Märgi lõpetatuks**. Kaup on garantiist väljastatud, kuid ei ole veel tavalisse lattu tagasi viidud. Tagasi tavapärasesse lattu liikumist saab töödelda kauba saabumise päeviku kaudu, mida saab vormistada aruande käigus kui valmis protsessi.

### <a name="ended"></a>Lõpetatud

Kui vahelaoorder lõppeb, viiakse kaup vahelaost tagasi tavalisse lattu. Kauba kande olekuks on vahelaos *Müüdud* ja tavalises laos *Ostetud*.

## <a name="quarantine-order-scrap"></a>Vahelaoorderi praak

Vahelaoorderi protsessi osana on võimalik ka varusid praakida. Praagi töötlemisel määratakse garantiilao väljaminekukandega varude olekuks *Müüdud*.

## <a name="additional-resources"></a>Lisaressursid

- [Varude blokeerimine](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
