---
title: Tooteomanikud
description: Teema annab teavet tooteomanike kohta. Tooteomanikud on kasutajad, kes vastutavad konkreetsete toodete eest. Neid tooteid saavad väljastada ainult grupi liikmed. Tooteomanikku saab kasutada ka kinnitamise töövoos.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 679712b2397f220e263da3df07ecd03c99bebf3f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842027"
---
# <a name="product-owners"></a>Tooteomanikud

[!include [banner](../includes/banner.md)]

Tooteomanikud on kasutajad, kes vastutavad konkreetsete toodete eest. Kui tooteomaniku grupp on määratud tootele, saavad toote väljastada ainult selle grupi liikmed. Tooteomanikku saab kasutada ka kinnitamise töövoos tehniliste muudatuste halduses.

Tooteomanikud on globaalsed sätted. Seetõttu on need kättesaadavad kõikidele juriidilistele isikutele.

## <a name="create-a-product-owner-group"></a>Tooteomaniku grupi loomine

Tooteomaniku grupi loomiseks ja sellele liikmete lisamiseks toimige järgmiselt.

1. Valige **Tehniliste muudatuste haldus \> Häälestus \> Tooteomanikud**.
2. Valige toimingupaanil nupp **Uus**.
3. Sisestage väljale **Tooteomanik** grupi nimi.
4. Väljale **Nimi** sisestage grupi kirjeldus.
5. Kiirkaardile **Liikmed** lisage töötajad, kes peaksid olema grupi liikmed.

## <a name="assign-a-product-owner-to-a-product"></a>Tootele tooteomaniku määramine

Tootele tooteomaniku määramiseks tehke järgmist.

1. Avage asjakohase toote või tooteetaloni leht **Toote üksikasjad**.
1. Kiirkaardil **Üldine** määrake väljale **Tooteomanik** asjakohase tooteomaniku rühma nimi.

Kui tooteomanik on tootele määratud, saavad sätet **Tooteomanik** redigeerida ainult tooteomaniku grupi liikmed.

Tooteomanik on nähtav ka lehel **Väljastatud tooted**.

## <a name="product-owners-and-product-releases"></a>Toote omanikud ja toote väljalasked

Selle toote saavad väljastada ainult tooteomaniku grupi kasutajad. Siiski on tegu erandiga, kui toode on tütarüksus ja selle emaüksuse väljastaja on emaüksuse omanik. Teisisõnu, kui toode on osa mõnest teise toote kooslusest, ei kontrolli süsteem koosluse iga üksuse tooteomanikku. See kontrollib ainult emaüksuse tooteomanikku.

Näiteks toode X on määratud *Disainkappide* toote omaniku grupile. Toode X on ühtlasi osa toote Y kooslusest, mis on määratud tooteomaniku grupile *Kõlaridisain*. Kui tooteomaniku grupi *Kujunduskõlarid* kasutaja väljastab toote Y ja selle koosluse, väljastatakse toode X koos tootega Y.

## <a name="product-owners-and-approvals"></a>Tooteomanikud ja kinnitused

Kuna tooteomanikud teavad, kas konkreetsetest tehnilistest muudatustest on toodetele kasu, on sageli mõistlik kaasata need tehniliste muudatuste halduses kinnitamise protsessi osana. Saate selle lähenemise rakendada, häälestades tooteomanikud osalevate pakkujatena töövoogudes, mida kasutatakse tehniliste muudatuste haldamiseks. Süsteem määrab seejärel töövoodes kinnitamise ülesanded, mis põhinevad tehniliste muudatuste taotlustes ja tehnilise muudatuste tellimustes olevatel toodetel. Lisateavet vt teemast [Tehniliste toodete muudatuste haldamine](engineering-change-management.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]