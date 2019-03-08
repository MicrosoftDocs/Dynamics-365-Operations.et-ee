---
title: Müügitellimuste lähetamine ladustamiseta
description: Selles juhendis selgitatakse, kuidas värskendada müügitellimust, kui tooted on kliendile tarnitud.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae70e09dbc4da90b7d1802d076384eae2d00da0e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "312964"
---
# <a name="ship-sales-orders-without-warehousing"></a>Müügitellimuste lähetamine ladustamiseta

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles juhendis selgitatakse, kuidas värskendada müügitellimust, kui tooted on kliendile tarnitud. Juhend kehtib täitmisvoo puhul, mis pole seadistatud laohalduse jaoks (ei põhi- ega täpsema lao puhul) ega nõua seetõttu toote komplekteerimise registreerimist enne tarnimist. Saate seda protseduuri käitada oma andmete või demoettevõtte USMF andmetega. Mõlemal juhul tuleb enne selle ülesande alustamist luua müügitellimus varundatud tootele, mille kogus on suurem kui 1. Sisestamise tõrke vältimiseks peab kontrollima, et toote saadaolev kogus tellimusel valitud asukohas ja laos vastab tellitud kogusele.


## <a name="post-packing-slip-for-an-order"></a>Tellimuse saatelehe sisestamine
1. Avage Müük ja turundus > Müügitellimused > Kõik müügitellimused.
2. Leidke ja valige loendist selle ülesande jaoks loodud tellimus.
3. Klõpsake loendis valitud real olevat linki.
4. Klõpsake toimingupaanil valikut Komplekteerimine ja pakkimine.
5. Klõpsake valikut Saatelehe sisestamine.
6. Laiendage või ahendage jaotist Parameetrid.
7. Valige väljal Kogus väärtus Kõik.
    * Muud suvandiud on Tarni kohe ja Komplekteeritud. Kui tellimuserida tuleb tarnida osaliselt ja tellimuserea väli Tarni kohe sisaldab kogust, valige suvand Tarni kohe. Kui teie organisatsiooni täitmisvoog sisaldab komplekteerimist eraldi protsessina, mida hallatakse ja registreeritakse komplekteerimisloendiga, valige suvand Komplekteeritud.  
    * Kontrollige, kas suvandi Sisestamine sätteks on valitud Jah.  
8. Määrake suvandi Saatelehe printimine sätteks Jah.
    * Vahekaart Ülevaade sisaldab loendit selles sisestuses loodavate saatelehtede loendit. Kui tarnite üksikut tellimust, luuakse tavaliselt üks saateleht. Kui aga selle tellimuse read tarnitakse erinevatest kohtadest, jaotatakse sisestus automaatselt vastavaks arvuks dokumentideks. See on kohustuslik tingimus, mida ei saa muuta. Samamoodi jaotatakse sisestus mitmeks dokumendiks, kui tellimuse read tuleb tarnida erinevatele tarneaadressidele ja tarnepoliitika on seadistatud jaotust nõudma.  
9. Valige vahekaardil Read tarnitava tellimuserea jaoks rida.
10. Sisestage väljale Värskendus algsest kogusest väiksem arv.
11. Klõpsake nuppu OK.
12. Klõpsake nuppu Jah.
13. Sulgege leht.
14. Klõpsake toimingupaanil valikut Suvandid.
15. Klõpsake suvandit Muuda vaadet.
16. Klõpsake suvandit Päisevaade.
    * Kui kõik tellimuse read on täielikult tarnitud, muutub tellimuse olek väärtuselt Avatud väärtusele Tarnitud.  
    * Selles näites on tellimuserida tarnitud osaliselt. Seetõttu jääb tellimuse olekuks Avatud.     
    * Välja Dokumendi olek väärtuseks määratakse Saateleht, kuna vähemalt üks tellimuserida on tarnitud.  
17. Klõpsake toimingupaanil valikut Üldine.
18. Klõpsake suvandit Rea kogus.
19. Sulgege leht.
20. Klõpsake toimingupaanil valikut Komplekteerimine ja pakkimine.
21. Klõpsake suvandit Saateleht.
    * Leht Saatelehe tööleht sisaldab kõiki teie tellimuse jaoks loodud saatelehedokumente. Saate iga dokumendi üksikasjad soovi korral üle vaadata ja välja printida.  

