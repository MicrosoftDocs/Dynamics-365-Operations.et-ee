---
title: Koondplaneerimise töö tühistamine
description: See teema selgitab, kuidas tühistada aktiivne plaanimistöö, mis kasutab sisseehitatud planeerimise funktsioone.
author: ChristianRytt
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: c04e2b2c0e5d7f28ea688578b3e1d7a1e1d9f6d3
ms.sourcegitcommit: 66eae22cd99e53fe8e4c6c94945ad8061b69a442
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/11/2020
ms.locfileid: "3117444"
---
# <a name="cancel-a-master-planning-job"></a>Koondplaneerimise töö tühistamine

[!include [banner](../includes/banner.md)]

Rakenduses Microsoft Dynamics 365 Supply Chain Managementon koondplaneerimise töö tühistamiseks mitu võimalust. Näiteks võite soovida tühistada koondplaneerimise töö, kui see käivitati kogemata või kui see töötab oodatust kauem ja soovite selle lõpetada. Parim viis planeerimise töö tühistamiseks on alates **lõpetamata planeerimise protsesside** leheküljest. **Pakett-tööde** ja **pakett-tööde täiustatud** lehti tuleks kasutada ainult juhul, kui koondplaneerimise töö tühistamine lehel **lõpetamata planeerimise protsessid** ei ole lõppenud mõne minuti jooksul.

## <a name="preferred-cancel-option"></a>Eelistatud tühistamise suvand
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a>Tühista koondplaneerimise töö **lõpetamata planeerimise protsesside** lehelt
1. Avage **Koondplaneerimine > Päringud ja aruanded > Koondplaneerimine > Lõpetamata planeerimise protsessid**.
2. Valige parandusrida koos planeerimisprotsessiga, mida soovite lõpetada.
3. Klõpsake **Tühista**.

## <a name="additional-cancel-options"></a>Tühistamise lisavalikud
Neid tohib kasutada ainult juhul, kui lehel **Lõpetamata planeerimisprotsessid** tühistatud planeerimistööd ei lõpetatud mõne minuti jooksul.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Koondplaneerimise töö kustutamine **pakett-tööde** lehelt
1. Avage **Süsteemihaldus > Päringud > Pakett-tööd**.
2. Valige rida koos planeerimistööga, mida soovite lõpetada.
3. Klõpsake  **Kustuta**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Koondplaneerimise töö kustutamine **pakett-tööde täiustatud** lehelt
1. Avage **Süsteemihaldus > Päringud > Pakett-tööd**.
2. Kui töö ID-d loendis ei kuvata, klõpsake käsku **Aktiveeri täiustatud vormile**, muul juhul jätkake järgmise juhisega.
3. Avage pakett-töö. Klõpsake **töö ID** -d pakett-töö jaoks, mille ülesandeid soovite lõpetada.
4. Valige **pakett-töö**-s ülesanded, mida soovite lõpetada.
5. Klõpsake **partii ülesanded** kiirvalikul nuppu **Katkesta**.
