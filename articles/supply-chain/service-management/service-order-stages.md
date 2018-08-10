---
title: Teenusetellimuste etapid
description: "Hooldustellimuse etappide määratlemine ja töötajatele määramine võimaldab teil juhtida hooldustellimuse voogu ülesannetes, mida täidab teenuseorganisatsioonis mitu inimest."
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9aa90dfcfc4b30d6cb4fa7ed4e6faaf505548d41
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="service-order-stages"></a>Teenusetellimuste etapid   

[!include [banner](../includes/banner.md)]


Saate häälestada teenusetellimuse etapid, et määratleda ülesanded, mis tuleb täita, ülesannete täitmise järjekord ja töötajad, kes vastutavad ülesannete täitmise eest. Teenusetellimuse etappide määratlemine ja töötajatele määramine võimaldab teil juhtida teenusetellimuse voogu ülesannetes, mida täidab teenuseorganisatsioonis mitu inimest. Etapiseeria peab hõlmama esmast etappi.

Saate määratleda ka igas etapis lubatud toimingud. Näiteks kui tühjendate ruudu **Sisesta** kõikide etappide jaoks peale viimase, takistate hooldustellimuste sisestamist enne kõikide etappide läbimist.

## <a name="branching-in-service-order-stages"></a>Teenusetellimuse etappide harud

Hoolduse etapi häälestamisel saate luua mitu valikut ehk haru, mille vahel hoolduse järgmises etapis valida. Kõik loodavad harud on pärast esmase etapi lõpuleviimist valimiseks saadaval. Näiteks saate esimesena häälestada etapi **Plaanimine**. Loote kaks etappi nimega **Pooleli** ja **Tühista** ning seejärel valite etapi **Plaanimine** nende emaüksuseks. Määrate etapi **Plaanimine** müügitellimusse. Kui müügitellimuse plaanimisetapp jõuab lõpule, saate valida etapi **Pooleli**, kui müügitellimus on töötlemiseks valmis, või etapi **Tühista**, kui müügitellimus tühistatakse.

## <a name="see-also"></a>Vt ka

[Saate häälestada hooldustellimuse etappe.](set-up-service-order-stages.md)

[teenustellimuse etapi muutmine](change-service-order-stage.md)

  



