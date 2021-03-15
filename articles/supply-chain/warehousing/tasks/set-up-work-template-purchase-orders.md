---
title: Ostutellimuste jaoks töömalli seadistamine
description: See teema keskendub lihtsa töömalli seadistamisele, mida saab kasutada saadud kaupade paigutamiseks.
author: ShylaThompson
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9acf6db9138a009527c6662f1cbb7e5fedc8778
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976859"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a>Ostutellimuste jaoks töömalli seadistamine

[!include [banner](../../includes/banner.md)]

See teema keskendub lihtsa töömalli seadistamisele, mida saab kasutada saadud kaupade paigutamiseks. Töömallid määravad juhiste kogumi, mis esitatakse laotöötajale mobiilsel seadmel, kui kaupu vastuvõtualalt ära viiakse. Saate kasutada seda protseduuri demoettevõttes USMF nimetatud andmetega. Enne selle juhendi käivitamist looge töökausta ID. Selles näites kasutatakse töökausta ID-d nimega Sissetulev. See protseduur on mõeldud laohaldurile.

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