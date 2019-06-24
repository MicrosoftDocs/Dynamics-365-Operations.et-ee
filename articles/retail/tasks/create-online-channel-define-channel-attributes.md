---
title: Võrgukanali loomine ja kanaliatribuutide määratlemine
description: See protseduur juhendab uue võrgukanali loomisel ja selle lisamisel organisatsiooni hierarhiasse.
author: jashanno
manager: AnnBe
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4547731d7e3bc56b1ba5e0a35ff4746c6c0e9863
ms.sourcegitcommit: 901ec3b360303bb8b4d9a9dcfecc6d75d7f844a0
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/05/2019
ms.locfileid: "1618292"
---
# <a name="create-online-channel-and-define-channel-attributes"></a>Võrgukanali loomine ja kanaliatribuutide määratlemine

[!include[task guide banner](../includes/task-guide-banner.md)]

See protseduur juhendab uue võrgukanali loomisel ja selle lisamisel organisatsiooni hierarhiasse. Organisatsiooni hierarhia tuleb luua enne uue võrgukanali loomist. Protseduur kasutab demoettevõtte USRT andmeid.


## <a name="create-a-new-online-channel"></a>Uue võrgukanali loomine
1. Avage Jaemüük ja kaubandus > Kanalid > Veebipoed.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Nimi.
4. Sisestage või valige väärtus väljal Ladu.
5. Tehke valik väljal Salvesta ajavöönd.
6. Valige või sisestage väärtus väljal Default customer (Vaikimisi klient).
7. Valige või sisestage väärtus väljal Kliendi aadressiraamat.
8. Valige või sisestage väärtus väljal Terms of payment (Makse tingimused).
9. Valige või sisestage väärtus väljal Makseviis.
10. Sisestage või valige väärtus väljal Email notification profile (E-posti teatise profiil).
11. Laiendage jaotist Financial dimensions (Finantsdimensioonid).
12. Sisestage või valige välja Äriüksus väärtus.
    * Samuti saate määrata teiste vaikedimensioonide väärtused.  
13. Klõpsake nuppu Salvesta.

## <a name="add-the-online-channel-to-organization-hierarchy"></a>Võrgukanali lisamine organisatsiooni hierarhiasse
1. Sulgege leht.
2. Avage Organisatsiooni haldus > Organisatsioonid > Organisatsiooni hierarhiad.
3. Otsige loendist ja valige soovitud kirje.
4. Klõpsake käsku Kuva.
5. Klõpsake nuppu Redigeeri.
    * Saate valida ükskõik, millise hierarhiasõlme, millesse soovite uue kanali lisada.  
6. Klõpsake nuppu Sisesta.
7. Klõpsake valikut Jaemüügikanal.
8. Klõpsake nuppu OK.
9. Rippdialoogi avamiseks klõpsake käsku Avalda.
10. Sisestage kuupäev ja kellaaeg väljale Jõustumiskuupäev.
11. Klõpsake Avalda.

## <a name="configure-orders-for-near-realtime-notification"></a>Tellimuste konfigureerimine peaaegu reaalajas teatiste jaoks
1. Valige suvandid Retail > Peakontori seadistamine > Parameetrid > Retaili parameetrid.
2. Määrake reaalajas kasutamise teenus e-kaubanduse tellimuste loomiseks väärtusele Jah.
3. Kävitage jaotusgraafik 1070 muudatuste sünkroonimiseks kanali andmebaasiga. 


