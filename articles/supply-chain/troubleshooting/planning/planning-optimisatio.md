---
title: Plaanitud ostutellimus luuakse ostu olemasolul negatiivsete päevade jooksul
description: Kui laovarude kood on miinimum/maksimum, loob Planning Optimization plaanitud ostutellimuse, kui ost on negatiivsete päevade jooksul olemas.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026445"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a>Plaanitud ostutellimus luuakse ostu olemasolul negatiivsete päevade jooksul

KB number: 4614298

## <a name="symptoms"></a>Sümptomid

Kui laovarude kood on *miinimum/maksimum*, loob Planning Optimization plaanitud ostutellimuse, kui ost on negatiivsete päevade jooksul olemas.

## <a name="resolution"></a>Eraldusvõime

Planning Optimization ei toeta negatiivseid päevi. Kuid see tagab alati, et plaanitud tellimusi ei planeerita täitmisaja jooksul praeguse kuupäevaga võrreldes. Näiteks ostu täitmisaeg on 10 päeva ning ostutellimus peaks saabuma kaheksa päeva jooksul tänasest. Sel juhul kasutatakse ostutellimust pakkumisena nõudlusele, mis on viis päeva alates tänasest.

Seetõttu on soovitatav täitmisajad korrigeerida nii, et see hõlmaks kõiki (või peaaegu kõiki) oma stsenaariume.
