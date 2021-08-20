---
title: Müügitellimuste lähetamine ladustamiseta
description: Selles teemas selgitatakse, kuidas värskendada müügitellimust, kui tooted on kliendile tarnitud.
author: omulvad
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0760ff5810bb832e25d6a2d473b3cda703872a05de4936191f91664406fe18c8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767312"
---
# <a name="ship-sales-orders-without-warehousing"></a>Müügitellimuste lähetamine ladustamiseta

[!include [banner](../../includes/banner.md)]

Selles teemas selgitatakse, kuidas värskendada müügitellimust, kui tooted on kliendile tarnitud. Juhend kehtib täitmisvoo puhul, mis pole seadistatud laohalduse jaoks (ei põhi- ega täpsema lao puhul) ega nõua seetõttu toote komplekteerimise registreerimist enne tarnimist. Saate seda protseduuri käitada oma andmete või demoettevõtte USMF andmetega. Mõlemal juhul tuleb enne selle ülesande alustamist luua müügitellimus varundatud tootele, mille kogus on suurem kui 1. Sisestamise tõrke vältimiseks peab kontrollima, et toote saadaolev kogus tellimusel valitud asukohas ja laos vastab tellitud kogusele.

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
    - Selles näites on tellimuserida tarnitud osaliselt. Seetõttu jääb tellimuse olekuks Avatud.     
    - Välja **Dokumendi olek** väärtuseks määratakse Saateleht, kuna vähemalt üks tellimuserida on tarnitud.  
16. Valige toimingupaanil **Üldine**.
17. Valige **Rea kogus**.
18. Sulgege leht.
19. Klõpsake tegevuspaneelil valikut **Komplekteerimine ja pakkimine.**
20. Vali **Saateleht**. Leht **Saatelehe tööleht** sisaldab kõiki teie tellimuse jaoks loodud saatelehedokumente. Saate iga dokumendi üksikasjad soovi korral üle vaadata ja välja printida.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]