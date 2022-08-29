---
title: Müügitellimuste lähetamine ladustamiseta
description: See artikkel selgitab, kuidas värskendada müügitellimust, kui tooteid kliendile saadetakse.
author: Henrikan
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2bb4115a486fbfe7287c9b183224699de4dfd456
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335521"
---
# <a name="ship-sales-orders-without-warehousing"></a>Müügitellimuste lähetamine ladustamiseta

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas värskendada müügitellimust, kui tooteid kliendile saadetakse. Juhend kehtib täitmisvoole, mis ei ole seadistatud laohalduse jaoks (ei ole baas- ega laohaldusprotsessid (WMS)) ega nõua seetõttu toote komplekteerimist enne saatmist registreerida. Saate seda protseduuri käitada oma andmete või demoettevõtte USMF andmetega. Mõlemal juhul tuleb enne selle ülesande alustamist luua müügitellimus varundatud tootele, mille kogus on suurem kui 1. Sisestamise tõrke vältimiseks peab kontrollima, et toote saadaolev kogus tellimusel valitud asukohas ja laos vastab tellitud kogusele.

## <a name="post-packing-slip-for-an-order"></a>Tellimuse saatelehe sisestamine
1. Avage navigeerimispaanil **Moodulid > Müük ja turundus > Müügitellimused > Kõik müügitellimused**.
2. Leidke ja valige loendist selle ülesande jaoks loodud tellimus.
3. Klõpsake tegevuspaneelil valikut **Komplekteerimine ja pakkimine.**
4. Vali **Sisesta saateleht**.
5. Laiendage või ahendage jaotist **Parameetrid**.
6. Valige väljal **Kogus** suvand **Kõik**.
    - Muud suvandid on **Tarni kohe** ja **Komplekteeritud**. Kui tellimuserida tuleb tarnida osaliselt ja tellimuserea väli **Tarni kohe** sisaldab kogust, valige suvand **Tarni kohe**. Kui teie organisatsiooni täitmisvoog sisaldab komplekteerimist eraldi protsessina, mida hallatakse ja registreeritakse komplekteerimisloendiga, valige suvand **Komplekteeritud**.  
    - Kontrollige, kas suvandi **Sisestamine** sätteks on valitud **Jah**.  
7. Määrake suvandi **Saatelehe printimine** sätteks **Jah**. Vahekaart **Ülevaade** sisaldab loendit selles sisestuses loodavate saatelehtede loendit. Kui tarnite üksikut tellimust, luuakse tavaliselt üks saateleht. Kui aga selle tellimuse read tarnitakse erinevatest kohtadest, jaotatakse sisestus automaatselt vastavaks arvuks dokumentideks. See on kohustuslik tingimus, mida ei saa muuta. Samamoodi jaotatakse sisestus mitmeks dokumendiks, kui tellimuse read tuleb tarnida erinevatele tarneaadressidele ja tarnepoliitika on seadistatud jaotust nõudma.  
8. Valige vahekaardil **Read** tarnitava tellimuserea jaoks rida.
9. Sisestage väljale **Värskendus** algsest kogusest väiksem arv.
10. Valige nupp **OK**.
11. Valige **Jah**.
12. Sulgege leht.
13. Toimingupaanil valige **Suvandid**.
14. Valige **Muuda vaadet**.
15. Valige **Päise vaade**.
    - Kui kõik tellimuse read on täielikult tarnitud, muutub tellimuse olek väärtuselt Avatud väärtusele Tarnitud.  
    - Selles näites on tellimuserida tarnitud osaliselt. Seetõttu jääb tellimuse olek avatuks.     
    - Välja **Dokumendi olek** väärtuseks määratakse Saateleht, kuna vähemalt üks tellimuserida on tarnitud.  
16. Valige toimingupaanil **Üldine**.
17. Valige **Rea kogus**.
18. Sulgege leht.
19. Klõpsake tegevuspaneelil valikut **Komplekteerimine ja pakkimine.**
20. Vali **Saateleht**. Leht **Saatelehe tööleht** sisaldab kõiki teie tellimuse jaoks loodud saatelehedokumente. Saate iga dokumendi üksikasjad soovi korral üle vaadata ja välja printida.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]