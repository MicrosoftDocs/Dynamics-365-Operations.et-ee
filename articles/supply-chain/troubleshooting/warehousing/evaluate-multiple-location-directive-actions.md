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
ms.openlocfilehash: 2d5f7cf548eb6c18d9700c73ef084f197b78542e
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102959"
---
# <a name="multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Mitu SKU valikut ei hinda mitme asukohadirektiivi tegevusi

## <a name="symptoms"></a>Sümptomid

*Müügitellimuste* töötellimuse tüübi ja *Komplekteerimise* töötüübid ei hinda mitme asukoha direktiivi tegevust, kui on valitud **Mitu SKU-d**. Hinnatakse ainult esimese asukoha direktiivi tegevust.

## <a name="resolution"></a>Lahendus

Uus funktsioon *Hinda mitme SKU-ga asukoha direktiivide kõiki tegevusi* on lisatud versiooni 10.0.15 (vt [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Selle funktsiooniga hinnatakse kõiki mitme SKU-ga asukoha direktiivide tegevusi. Tarneahela halduse versiooni 10.0.21 puhul on see funktsioon vaikimisi sisse lülitatud.  Tarneahela halduse 10.0.25 puhul on see funktsioon kohustuslik ja seda ei saa välja lülitada. Administraatorid saavad funktsioonihalduse [lehte kasutada](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), et kontrollida funktsiooni olekut ja lubada või keelata see, kui vaja.
