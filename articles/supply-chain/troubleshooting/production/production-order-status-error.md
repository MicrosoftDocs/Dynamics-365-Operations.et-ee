---
title: Tõrge oleku muutmisel olekult lõpetatuna kinnitatud olekule lõpp
description: Tootmistellimuse oleku muutmisel lõpetatud olekust, kinnitatud olekuks, võite saada vea. See lehekülg selgitab probleemi lahendamist.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 744637f5cccffe44b85f77c1a9df2034012fac40
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476126"
---
# <a name="error-when-changing-status-of-production-order-from-reported-as-finished-to-end"></a>Viga tootmistellimuse oleku muutmisel valmimisest teatatud lõpetatuks

## <a name="symptoms"></a>Sümptomid

Kui tootmistellimuse olek muudetakse täielikult lõpetatuks, kuvatakse järgmine tõrketeade: "Värskenda konflikti.

> Värskenduse konflikt. Standardkulu ei kattu pärast uuendamist finantsilise laovaru väärtusega.

> Funktsioonis InventCostMovement.checkVariance ilmnes kriitiline tõrge.

## <a name="cause"></a>Põhjus

See probleem ilmneb, sest aluseks olevaid andmeid muudeti teise protsessiga. Protsess proovib värskendada andmeid kuni viis korda. Kui konflikt on pärast viit katset endiselt olemas, kuvatakse üks allpool loetletud tõrketeadetest.

## <a name="resolution"></a>Lahendus

Selline käitumine on nii kavandatud. Probleemi leevendamiseks naaske partii juurde. See peaks lõpetama töötamise.

Kui partii töö järjepidevalt nurjub pärast selle jätkamist, veenduge, et pearaamatu vaikevaluuta ümardamise täpsus oleks vastavuses InventSum tabeli väärtustele rakendatud ümardamisega. Kui ümardamise täpsust on muudetud mittevastavaks väärtuseks, peate selle ilmselt muutma tagasi vastavale väärtusele. Otsige **ModifiedDateTime**. Sellisel juhul näitab väärtus tavaliselt, et ümardamise täpsust on viimati muudetud.
