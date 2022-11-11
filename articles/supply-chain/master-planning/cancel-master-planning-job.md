---
title: Tühistage töö, mis loodi, kasutades taunitud koondplaneerimise mootorit.
description: See artikkel selgitab, kuidas tühistada aktiivse plaanimise tööd, mis kasutab taunitud koondplaneerimise mootorit.
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
ms.openlocfilehash: 7b71a43f407050dccb7550db7c4b6a98a596d589
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740873"
---
# <a name="cancel-a-job-that-was-created-using-the-deprecated-master-planning-engine"></a>Tühistage töö, mis loodi, kasutades taunitud koondplaneerimise mootorit.

[!include [banner](../includes/banner.md)]

Aegunud koondplaneerimise mootori abil loodud töö tühistamiseks on mitu võimalust. Näiteks võite soovida tühistada koondplaneerimise töö, kui see käivitati kogemata või kui see töötab oodatust kauem ja soovite selle lõpetada.

Parim viis planeerimise töö tühistamiseks on alates **lõpetamata planeerimise protsesside** leheküljest. **Pakett-tööde** ja **pakett-tööde täiustatud** lehti tuleks kasutada ainult juhul, kui koondplaneerimise töö tühistamine lehel **lõpetamata planeerimise protsessid** ei ole lõppenud mõne minuti jooksul.

## <a name="preferred-cancel-option"></a>Eelistatud tühistamise suvand

### <a name="cancel-master-planning-job-from-the-unfinished-planning-processes-page"></a>Lõpetamata plaanimisprotsesside lehelt koondplaneerimise töö tühistamine

1. Avage **Koondplaneerimine > Päringud ja aruanded > Koondplaneerimine > Lõpetamata planeerimise protsessid**.
2. Valige parandusrida koos planeerimisprotsessiga, mida soovite lõpetada.
3. Valige **Tühista**.

## <a name="additional-cancel-options"></a>Tühistamise lisavalikud

Neid tohib kasutada ainult juhul, kui lehel **Lõpetamata planeerimisprotsessid** tühistatud planeerimistööd ei lõpetatud mõne minuti jooksul.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Koondplaneerimise töö kustutamine **pakett-tööde** lehelt

1. Avage **Süsteemihaldus > Päringud > Pakett-tööd**.
2. Valige rida koos planeerimistööga, mida soovite lõpetada.
3. Valige **Kustuta**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Koondplaneerimise töö kustutamine **pakett-tööde täiustatud** lehelt

1. Avage **Süsteemihaldus > Päringud > Pakett-tööd**.
2. Kui töö ID-d loendis ei kuvata, klõpsake käsku **Aktiveeri täiustatud vormile**, muul juhul jätkake järgmise juhisega.
3. Avage pakett-töö. Valige pakett-töö **ID** ülesannetega, mida soovite lõpetada.
4. Valige **pakett-töö**-s ülesanded, mida soovite lõpetada.
5. Valige **Muuda olekut**, valige **Tühistamine** ja klõpsake **OK**.
6. Klõpsake **partii ülesanded** kiirvalikul nuppu **Katkesta**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]