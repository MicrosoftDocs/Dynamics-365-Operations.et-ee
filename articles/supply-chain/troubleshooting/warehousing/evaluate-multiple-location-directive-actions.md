---
title: Mitme SKU asukohakorralduste kõigi toimingute hindamine
description: Lisatud on uus funktsioon, et hinnata mitme SKU-ga asukohadirektiivi toiminguid. Sellel lehel kuvatakse teave selle kohta, kuidas see sisse lülitada.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 45995ed6f051cdf6be2b2985ff0e2cb1decf4cf0
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476103"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Mitu SKU valikut ei hinda mitme asukohadirektiivi tegevusi

## <a name="symptoms"></a>Sümptomid

*Müügitellimuste* töötellimuse tüübi ja *Komplekteerimise* töötüübid ei hinda mitme asukoha direktiivi tegevust, kui on valitud **Mitu SKU-d**. Hinnatakse ainult esimese asukoha direktiivi tegevust.

## <a name="resolution"></a>Lahendus

Uus funktsioon *Hinda mitme SKU-ga asukoha direktiivide kõiki tegevusi* on lisatud versiooni 10.0.15 (vt [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Selle funktsiooniga hinnatakse kõiki mitme SKU-ga asukoha direktiivide tegevusi. Kui vajate seda funktsiooni, kasutage selle sisselülitamiseks [Funktsiooni haldamist](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
