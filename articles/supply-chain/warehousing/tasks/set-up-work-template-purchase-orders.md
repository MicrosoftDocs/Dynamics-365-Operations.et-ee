---
title: Ostutellimuste jaoks töömalli häälestamine
description: See artikkel kirjeldab, kuidas seadistada lihttöömalli, mida kasutatakse vastuvõetud kaupade äraseadmisel.
author: Mirzaab
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee6bc896a979c326001e1596e4a463753005fabf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877359"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Ostutellimuste jaoks töömalli häälestamine

[!include [banner](../../includes/banner.md)]

See artikkel kirjeldab, kuidas seadistada lihttöömalli, mida kasutatakse vastuvõetud kaupade äraseadmisel. Töömallid määravad juhiste kogumi, mis esitatakse laotöötajale mobiilsel seadmel, kui kaupu vastuvõtualalt ära viiakse. Saate kasutada seda protseduuri demoettevõttes USMF nimetatud andmetega. Enne selle juhendi käivitamist looge töökausta ID. Selles näites kasutatakse töökausta ID-d nimega Sissetulev. See protseduur on mõeldud laohaldurile.

1. Avage navigeerimispaneelil **Moodulid > Laohaldus > Seadistus > Töö > Töömallid**.
2. Valige väljal **Töökäsu tüüp** suvand **Ostutellimused**.

## <a name="create-a-work-template-header"></a>Töömalli päise loomine
1. Valige suvand **Uus**.
2. Sisestage arv väljale **Järjekorranumber**. See on järjestus, milles töömalle hinnatakse. Vajaduse korral saate järjestust muuta.  
3. Sisestage väärtus välja **Töömall**. See on selle malli ainuidentifikaator.  
4. Tippige väärtus väljale **Töömalli kirjeldus**.
    - Suvandit **Kehtiv** ei märgita enne, kui olete lisanud kõik malli puhul vajaliku teabe ja klõpsanud seejärel käsku **Salvesta**.  
    - Töökäsu tüüpi **Ostutellimus** ei saa automaatselt töödelda, seega jätke valiku **Töötle automaatselt** väärtuseks **Ei**.  
5. Tippige väärtus väljale **Töökausta ID**. Töökaustade ID-de abil saate töö gruppidesse korraldada. Siin määratud väärtus on vaikeväärtus selle malli abil loodud tööde puhul.  
6. Sisestage väljale **Töö prioriteet** väärtus `1`. See näitab töö olulisust ja siin määratud väärtus on selle malli abil loodud töö puhul vaikeväärtus.  
7. Valige käsk **Salvesta**. Enne, kui saab kasutada nuppu **Päringu redigeerimine**, tuleb töömalli päis salvestada.  

## <a name="set-up-the-query-for-the-work-template"></a>Töömalli jaoks kasutatava päringu häälestamine
1. Valige **Päringu redigeerimine**. Määrame piirangu, et malli saab kasutada ainult konkreetses laos.  
2. Valige **Lisa**.
3. Tippige uue tea väljale **Väli** `warehouse`.
4. Sisestage väärtus väljale **Kriteerium**.
5. Valige nupp **OK**.
6. Valige **Jah**.

## <a name="set-work-template-details"></a>Töömalli üksikasjade häälestamine
1. Valige suvand **Uus**.
2. Tehke väljal **Töö tüüp** valik **Komplekteeri**.
3. Sisestage väljale **Tööklassi ID** sõna `purchase`. Siin määratud tööklassist saab vaikeväärtus kõigile tööridadele tüübiga Komplekteerimine, mis selle malli abil luuakse. Töötellimuse ridadelt ei saa tööklassi alistada. Tööklassidega suunatakse ja/või piiratakse töötellimuse ridade tüüp, mida laotöötaja saab mobiilses seadmes töödelda.  
4. Valige suvand **Uus**.
5. Väljal **Töö tüüp** valige **Paigal**.
6. Väljale **Tööklassi ID** sisestage väärtus. Komplekteerimise ja asetamise juhised on üks kogum. Igal komplekteerimise ja asetamise kogumil peab olema sama töö klass. Kasutage sama töö klassi, mille komplekteerimisjuhise jaoks andsite.  
7. Valige käsk **Salvesta**. Pange tähele, et märkeruut **Kehtiv** on nüüd märgitud.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]