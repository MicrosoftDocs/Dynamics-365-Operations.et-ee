---
title: Täiskoormuse arvutamine plaanitud töökäskude kohta
description: Selles teemas tutvustatakse, kuidas arvutada täiskoormust plaanitud töökäskude kohta varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b817909ac0950b773cba775be2502b5796c6d8d6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426396"
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

![Joonis 1](media/08-work-order-scheduling.png)

[!NOTE]
Kui valite oma arvutuse jaoks koormuse tüübid **Võimsus** või **Jääk**, kuvatakse sama tulemus, kui valitud perioodil pole ressursside kohta broneeringuid tehtud.

Teavet selle kohta, kuidas arvutada täiskoormus hooldusgraafiku ridade ja planeerimata töökäskude kohta, leiate teemast [Täiskoormuse arvutamine](../capacity-planning/calculate-capacity-load.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]