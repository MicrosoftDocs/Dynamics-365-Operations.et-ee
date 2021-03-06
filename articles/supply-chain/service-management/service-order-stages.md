---
title: Teenusetellimuste etapid
description: Hooldustellimuse etappide määratlemine ja töötajatele määramine võimaldab teil juhtida hooldustellimuse voogu ülesannetes, mida täidab teenuseorganisatsioonis mitu inimest.
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c46d4bb43c8f59a0ef55963ac9b453491a6112b0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817505"
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

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]