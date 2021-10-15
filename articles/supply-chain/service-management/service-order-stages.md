---
title: Teenusetellimuste etapid
description: Hooldustellimuse etappide määratlemine ja töötajatele määramine võimaldab teil juhtida hooldustellimuse voogu ülesannetes, mida täidab teenuseorganisatsioonis mitu inimest.
author: kamaybac
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
ms.openlocfilehash: 0a43cbe0cf5993a305ff500f34f0da5d3763084c
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576324"
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