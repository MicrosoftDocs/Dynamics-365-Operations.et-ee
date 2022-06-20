---
title: Koondplaneerimise töö tühistamine
description: See artikkel selgitab, kuidas tühistada aktiivset planeerimistööd, mis kasutab sisseehitatud plaanimise funktsioone.
author: t-benebo
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6a9667be9921fdde7e1ca5de68c7f51d48905ac8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860779"
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
5. Klõpsake nuppu **Muuda olekut**, valige **Tühistamine** ja klõpsake nuppu **OK**.
6. Klõpsake **partii ülesanded** kiirvalikul nuppu **Katkesta**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]