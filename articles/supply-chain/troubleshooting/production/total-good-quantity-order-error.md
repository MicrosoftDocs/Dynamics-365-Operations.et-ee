---
title: Kaupade üldkoguse tõrge tellimuse lõpetamisel
description: Kui proovite tootmistellimust lõpetada ja lõpetatuna esitada, võite saada toodete üldkoguse tõrke. See lehekülg selgitab, miks ja kuidas probleemi lahendada.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5f0c2c2ca64ada9d72c0ebd04e7de561aaa52039
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476110"
---
# <a name="total-good-quantity-error-when-trying-to-end-a-production-order"></a>Kaupade üldkoguse tõrge tootmistellimuse lõpetamisel

## <a name="symptoms"></a>Sümptomid

Kui proovite sisestada tootmistellimuse lõpetatuna kinnitamise töölehte, kuvatakse järgmine tõrketeade:

> Õige lõpetatuna kinnitatud tootmise kogus tootmisele kokku on %1. Tagasiside viimasele operatsioonile on kokku 0,00.

## <a name="cause"></a>Põhjus

See probleem ilmneb juhul, kui viimases toimingus sisestatud kogused olid valed. Näiteks kui tootmist alustatakse, kuid kogust, mis tuleb käivitada, ei eraldata, sisestatakse protsessikaardi tööleht ridadeta. Olukorra kinnitamiseks avage tootmistellimus ja seejärel valige toiminguribal **Kuvamine** vahekaardil suvand **Marsruudi kaart**.

## <a name="resolution"></a>Lahendus

Selle probleemi saate lahendada, kui sisestate täiendavad töölehed operatsioonide jaoks, mille jaoks töölehed pole õigesti sisestatud. Taaskäivitage tootmistellimus uuesti ja valige täiendavate töölehtede sisestamine. See tegevus ei käivita tootmistellimust, kuid see sisestab töölehed. Protsessi kaart peaks seejärel näitama sisestatud koguseid ja teil peaks olema võimalik tootmistellimused edukalt lõpetada.
