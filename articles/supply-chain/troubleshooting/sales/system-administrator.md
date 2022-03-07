---
title: Süsteemiadministraatorid ei saa tellimuste ootelolekuid tühjendada, sest nad pole autoriseeritud
description: Süsteemiadministraatorid ei saa tellimuste ootelolekuid tühjendada, sest nad pole autoriseeritud.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026456"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a>Süsteemiadministraatorid ei saa tellimuste ootelolekuid tühjendada, sest nad pole autoriseeritud

KB number: 4614642

## <a name="symptoms"></a>Sümptomid

Süsteemiadministraatorid ei saa müügitellimuste ootel olemist tühjendada, kui neil pole tellimuse ootele määratud konkreetset rolli.

## <a name="resolution"></a>Eraldusvõime

Juurdepääs teatud toimingutele, näiteks müügitellimuste kinnipidamiste kustutamine, on tingitud äripoliitika seadistamisest. Süsteemiadministraatoritel pole tavaliselt lubatud seda tüüpi toiminguid sooritada. 

Sageli reguleerib juurdepääsu konkreetsele toimingule äripoliitika ning seda ülesannet saavad täita ainult organisatsiooni konkreetsed isikud. Näited hõlmavad kinnitusi, mis on töövoo kinnituste tulemus ja töövoo konfiguratsioonist tulenevad konkreetsed ülesanded.

Kuigi ühtegi töövoogu ei ole tellimuste ootel olekuga seostatud, on põhimõte sarnane. Asjakohane roll määrab organisatsioonis konkreetse inimeste grupi, kellel on õigus tellimuse ootel olemised kustutada. Seda õigust ei tuleks tingimata anda kõikidele administraatoritele, kuna see lähenemine rikub määratletud äripoliitikat.
