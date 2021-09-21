---
title: Koondplaneerimine plaanib üle saadaoleva võimsuse
description: Koondplaneerimise käigus ei arvestata võimsuse piiranguid ja planeeritakse rohkem kui saadaolev võimsus
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 48b3d179bb923ff6f6cc5b6be291408b3eb34d98
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476134"
---
# <a name="master-planning-is-scheduling-more-than-the-available-capacity"></a>Koondplaneerimine plaanib üle saadaoleva võimsuse

## <a name="symptoms"></a>Sümptomid

Koondplaneerimise käigus ei arvestata võimsuse piiranguid ja planeeritakse rohkem kui saadaolev võimsus.

Kui kasutate operatsiooni planeerimist, kus on piiratud võimsus ja kui protsess määrab nii ressursirühma kui ka üksikute ressursside jaoks nõuete kombinatsiooni, on väike võimalus üle broneerida, kuna algoritm kontrollib võimsuse konflikte. See ülebroneerimine võib ilmneda, kui kasutate koondplaneerimise käivitamiseks abilisi. See on kõige tõenäolisem juhul, kui on palju töid, millel on suhteliselt lühike käitusaeg.

## <a name="resolution"></a>Lahendus

Kui on oluline, et operatsiooni planeerimisel ei esineks ülebroneerimist, saate koondplaneerimise planeerimisosa muuta ühekordseks, lülitades sisse **Täpne piiratud võimsus operatsiooni planeerimiseks** valiku **Koondplaneerimise parameetrite** lehel. See valik pole vaikimisi saadaval. Peate selle lehele käsitsi lisama, kasutades isikupärastamise funktsioone. Selle suvandi kasutamisel toimub planeerimine aeglasemalt, kuna puudub paralleelne töötlemine.
