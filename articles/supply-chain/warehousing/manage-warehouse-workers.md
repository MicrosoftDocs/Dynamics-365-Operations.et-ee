---
title: Laotöötajate haldamine
description: Selles artiklis kirjeldatakse, kuidas saate kasutada laorakendust nii, et see aitab kontrollida ja jälgida ladude töötajate tehtavat tööd.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, InventLocation, WHSLaborStandards, WHSWorker, WHSWorkTable, WHSWorkTableListPage, WHSResetUserPassword
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72891
ms.assetid: feaa6f15-49d2-41f5-9b87-453463c52e4e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 18dbcf32f85bca51bf48e5ed8c64fedc99f66082
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216831"
---
# <a name="manage-warehouse-workers"></a>Laotöötajate haldamine

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse, kuidas saate kasutada laorakendust nii, et see aitab kontrollida ja jälgida ladude töötajate tehtavat tööd.

Kui kasutate funktsiooni jaotises Laohaldus, viidatakse kõikidele laotöötaja toimingutele sõnaga *töö*. Töö, nagu komplekteerimine, teisaldamine ja vabade laovarude inventuur, salvestatakse mobiilse seadmega. Enne kui laotöötaja saab tööd teha, peab ta olema jaotises Inimressursid töötajaga seostatud. Iga kontoga **Töötaja** võib olla seostatud mitu laotöö kasutajat. Need töökasutajad võivad töötada erinevates ladudes ja neil võib olla erinevatele mobiilse seadme menüüdele erinev juurdepääsutase. Laotöö kasutajatest võib mõelda kui valitud töötaja mitmest logimisnimest. Igal töö kasutajal on vaikeladu ja selle töö kasutajale saadaolevate menüü-üksused kasutavad konkreetseid töövooge. 

Uue töö kasutaja loomiseks klõpsake lehe **Töötajad** vahekaardi **Üldine** jaotises **Laod** suvandit **Töötaja**. Peate määrama kasutaja ID, kasutajanime, vaikelao ja menüü nime. See menüü laaditakse, kui kasutaja logib sisse lao mobiilsete seadmete portaali ja laseb teil määratleda, millistele menüü-üksustele kasutajal juurdepääs on. 

Iga töö kasutaja seadistuse osana saate määratleda ka konkreetsed protsessi töövood. Näiteks saate kasutada välja **On tsüklilise inventuuri ülevaataja** määramaks, kas kasutaja saab korrigeerimisi töödela inventuuri ajal inventuuri lahknemiste tsükli kaupa läbimisel või kas need korrigeerimised tuleb enne teise isiku poolt üle vaadata.

## <a name="defining-labor-standards"></a>Tööstandardite määratlemine
Leht **Tööstandardid** võimaldab teil määratleda arvutamismeetodid, mida süsteem kasutab kindlat tüüpi töö jaoks vajaminema hinnangulise aja arvutamiseks. Selle määratluse saab seada üldisele või konkreetsele tasemele. Näiteks saate määratleda aja, mis on vajalik müügitellimuse komplekteerimise töötlemiseks kaalu järgi kindla üksuse määratlusele, kui kasutatakse kindlat komplekteerimisprotsessi. Samal ajal saate salvestada aja muu arvutamisviisi alusel komplekteeritud vaba kaubavaruga asetamistoimingu puhul. 

Enda määratletud tööstandardite lubamiseks peate valima suvandi **Luba tööstandardid** igale laole, kus tööstandardeid kasutatakse.

## <a name="monitoring-and-controlling-warehouse-work"></a>Laotöö seire ja kontrollimine
Leht **Kogu töö** võimaldab teil kogu plaanitud, töös olevat ja lõpetatud tööd jälgida ja säilitada. Sellel lehel saate värskendada erinevaid protsesse, nagu laotöö kasutaja määramised ja töö prioriteet. Samuti saate süveneda töö päise ja töö ridadega seotud üksikasjadesse, et mõista eeldatavast või lõpetatud tööprotsessidest. 

Kui lubate suvandi **Tööstandardid**, näete töö arvutatud hinnangulist aega. Kui tööd tehakse, kuvatakse iga töötoimingu puhul ka tegelik aeg. Nii saate võrrelda hinnangulist ajaarvutust tegeliku ajaga estimated. 

Lisaks saate kasutada hinnangulist aega töö loomisel töö automaatse jagamise reeglites. Nii saate laadida taskaalustatud töö hinnagulise ülesannete täitmiseks kuluva aja alusel. 

Tööüksuste töötlemiseks kasutatav aja analüüs aitab täiustada laotöötaja tõhusust. Analüüsi aitavad teostada järgmised saadaolevad aruanded.

-   **Töö kasutaja alusel** – see aruanne näitab töötaja tootlikkust eeldatud aja ja tegeliku aja võrdluse alusel.
-   **Töö tehingu tüübi alusel** – kasutage seda aruannet kindlate laoprotsesside puudujääkide uurimiseks. Näiteks märkate, et üleviimistellimuste komplekteerimised võtavad sel nädalal kauem aega kui eelmisel nädalal. Seda teavet saate kasutada edasiseks uurimiseks.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]