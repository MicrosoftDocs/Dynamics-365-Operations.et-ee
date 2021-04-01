---
title: Osa komplekteerimise kinnitus
description: Selles teemas kirjeldatakse, kuidas seadistada ja rakendada osa komplekteerimise kinnitust mobiilselt seadmelt.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 852bd29ae18b4903906aa7fb97a06389cd7cd3bc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232859"
---
# <a name="piece-picking-confirmation"></a>Osa komplekteerimise kinnitus

[!include [banner](../includes/banner.md)]

Osade komplekteerimine võimaldab kinnitada iga varude osa mobiilsel seadmel komplekteerimis- või inventuuritöö kaudu. Komplekteerimiste puhul saate kinnitada töödeldava töö koguse kuni komplekteeritaval tööl määratud koguseni. Inventuuritöö puhul võite skannida loendatavad varud ja jälgida kogusummat.

Kui lubate osade komplekteerimise, valitakse automaatselt toote kinnitamine. Töö tüübi komplekteerimiste puhul on lubatud maksimaalne arv osi. See võimaldab määrata maksimaalse ühikute arvu, mis tuleb tööprotsessi käigus kinnitada. Maksimaalne kogus põhineb praegu töödeldaval töö ühikul. Inventuuri töötüüp ei luba maksimumi.

Võite kasutada ka skannitud vöötkoodiga seostatud kogust ja mõõtühikut. See toimib sissetulevate voogude vastuvõtmisel, sh kombineeritud litsentsiplaadiga vastuvõtmine, ostutellimuse kaup, üleviimistellimuse kaup ja koormakaup. See toimib ka osa komplekteerimisel, kui vöötkoodi skannimine lisab koguse kinnitatud ühikute koguarvule, teisendades vöötkoodil olevat mõõtühikut ja tööühikut. Kui vöötkoodil oleva mõõtühiku loendamisel saab kinnitust, et kogus on lubatud seeriagrupis loendamiseks, lisatakse kogus koguarvule.

## <a name="where-it-applies"></a>Kus see kehtib

Osa komplekteerimine toimib kogu inventuuritöö ja mis tahes tüüpi töö algse komplekteerimise puhul. Osa komplekteerimine ei rakendu, kui kaupa juhitakse seerianumbritega või kui tegemist on tootmise või kanbani komplekteerimisega litsentsiplaadi (LP) asukohast ja kaup on määratud kogumiseks.

## <a name="set-up-piece-picking"></a>Osa komplekteerimise seadistamine

1.  Avage mobiilse seadme menüüelemendis seadistusvorm töö kinnitamiseks: Laohaldus > **Laohaldus** > **Seadistus** > **Mobiilne seade** > **Mobiilse seadme menüüelemendid**. 
2. Avage mobiilse seadme menüüelemendist jaotis Töö kinnituse häälestus.

Kui töö tüüp on komplekteerimine või inventuur, saab teha järgmisi valikuid.


|           Suvand           |                                                                            Kirjeldus                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Osa komplekteerimise kinnitus | Saadaval komplekteerimise ja inventuuri töötüüpide jaoks. Toote kinnitamine valitakse automaatselt. Võimaldab iga varude üksust mobiilsel seadmel skannides kinnitada. |
|  Osade maksimaalne arv  |                   Komplekteerimistöö jaoks saadaval, kui osa komplekteerimise kinnitamine on lubatud. Määrab piirmäära ühikute arvule, mille peate kinnitama.                   |



[!INCLUDE[footer-include](../../includes/footer-banner.md)]