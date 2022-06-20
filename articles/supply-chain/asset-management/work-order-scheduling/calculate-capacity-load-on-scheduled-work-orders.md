---
title: Täiskoormuse arvutamine plaanitud töökäskude kohta
description: See artikkel selgitab, kuidas arvutada varahalduses plaanitud töötellimustel võimsuse koormust.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 53b147198f6aa9e0254312e5ea48b9ae616a79a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857949"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a>Täiskoormuse arvutamine plaanitud töökäskude kohta

[!include [banner](../../includes/banner.md)]

 

Saate arvutada täiskoormuse plaanitud töökäskude kohta, et saada ülevaate ressursside töökoormuse kohta konkreetsel perioodil. Arvutused võivad olla järgmiste ressursside kohta: hooldustöötajad, töötajate grupid, tööriistad ja varad.

1. Klõpsake **Varahaldus** > **Päringud** > **Ajakava** > **Täiskoormus**.

2. Dialoogiboksis **Arvuta täiskoormus** > väljal **Kuva** valige millist koormuse tüüpi soovite arvutada: **Võimsus**, **Reserveeritud** või **Jääk**.

3. Valige **Jah** tumblernupul **Eira 0-ridu**, kui te ei soovi näha tulemusi, milles on null.

4. Valige ressursi tüübid, mille kohta soovite täiskoormust arvutada, valides **Jah** asjakohasel tumblernupul: **Töötaja**, **Hooldustöötaja grupp**, **Tööriist** ja **Vara**.

5. Valige arvutuse jaoks alguskuupäev väljal **Kuupäevast**.

6. Väljal **Intervalli tüüp** valige arvutuse intervall: **Päev**, **Nädal**, **Kuu** või **Kvartal**.

7. Väljale **Perioodi sagedus** sisestage intervallide arv, mida soovite arvutada. Kui olete valinud intervalli tüübiks näiteks **Päev** ja sisestate sellele väljale arvu "5", tehakse arvutus viie päeva kohta, alates alguskuupäevast.

8. Arvutuse alustamiseks klõpsake **OK**.

Allolev joonis näitab arvutuse tulemust koormuse tüübi **Reserveeritud** kohta, mis katab kolmenädalast perioodi.

![Joonis 1.](media/08-work-order-scheduling.png)

[!NOTE]
Kui valite oma arvutuse jaoks koormuse tüübid **Võimsus** või **Jääk**, kuvatakse sama tulemus, kui valitud perioodil pole ressursside kohta broneeringuid tehtud.

Teavet selle kohta, kuidas arvutada täiskoormus hooldusgraafiku ridade ja planeerimata töökäskude kohta, leiate teemast [Täiskoormuse arvutamine](../capacity-planning/calculate-capacity-load.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]