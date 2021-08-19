---
title: Te ei saa prognoositud ühiku kulusid värskendada, kui impordite prognoositud nõudluse kirjeid
description: Kui kasutate andmeüksuseid nõudluse prognoosi kirjete importimiseks, ei uuendata olemasolevate kirjete omahinda nii, et see vastaks imporditud andmetele.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: de471da861785f283eeaa78f97b5d1e1a6b023d71de6fff72ae39edd6bb124cc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765366"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a>Te ei saa prognoositud ühiku kulusid värskendada, kui impordite prognoositud nõudluse kirjeid

KB number: 4614109

## <a name="symptoms"></a>Sümptomid

Kui kasutate andmeüksuseid nõudluse prognoosi kirjete importimiseks, ei uuendata olemasolevate kirjete **Prognoositud omahinda** nii, et see vastaks imporditud andmetele.

## <a name="cause"></a>Põhjus

**Prognoositudd ühikuhind** on kirjutuskaitstud väli. Väärtus põhineb toote ühikuhinnal ja seda ei saa importimise kaudu otse määrata.

## <a name="resolution"></a>Eraldusvõime

Kuna väli on kirjutuskaitstud, ei saa te selle jaoks väärtusi importida. Väärtus arvutatakse vastavalt olemasolevale äriloogikale.
