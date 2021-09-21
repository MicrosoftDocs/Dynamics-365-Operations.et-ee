---
title: Üks ridadest on juba koormas
description: See lehekülg selgitab, miks te võisid tõrke kätte saada, "Üks ridadest on juba koormas. Ei saa lattu väljastada," ja kuidas probleemi lahendada.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0bdfaed005b9c58f7bd5f87dd6dffe648de47261
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476170"
---
# <a name="one-of-the-lines-is-already-on-a-load"></a>Üks ridadest on juba koormas

## <a name="symptoms"></a>Sümptomid

Sissetulevate laotoimingutega töötamisel ja saatmisel võite saada järgmise tõrketeate:

> Üks ridadest on juba koormas. Ei ole võimalik lattu väljastada.

Kui loote käsitsi koormaid või kui seadistate protsessi nii, et koormad on juba enne müügitellimuse rea sisestamist loodud, on eelduseks, et järgnev väljastus tehakse käsitsi ning kasutatakse koorma protsessi ja hinnangut.

Teises võimalikus stsenaariumis proovite teha automaatset väljastamist lattu, kuid voo protsessil ei õnnestunud tööd luua. Seetõttu luuakse avatud saadetis või koorem. See avatud saadetis või koorem blokeerib seejärel järgmised katsed tellimuse automaatselt väljastamiseks, kuni te kas kustutate avatud saadetise või koorma või töötlete uue voo käsitsi uuesti.

## <a name="resolution"></a>Lahendus

Saate väljastada müügitellimuse lehelt või teha automaatse väljastamise müügitellimuse lehelt ainult juhul, kui koormat pole enne lattu väljastamist olemas. Koorem luuakse automaatselt pärast voo töötlemist.
