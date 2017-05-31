---
title: "Finantsdimensioonid ja põhikontod paremalt vasakule keeles"
description: "See teema kirjeldab mõningaid juurutamisotsuseid, mida tuleb arvestada, kui kasutate rakenduses Microsoft Dynamics 365 for Operations paremalt vasakule keelt, ja peate seadistama finantsdimensioonid ja põhikontod."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b1f196d2a13bba49647dd4f008cd39b7417940f1
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="financial-dimensions-and-main-accounts-in-a-right-to-left-language"></a>Finantsdimensioonid ja põhikontod paremalt vasakule keeles

[!include[banner](../includes/banner.md)]


See teema kirjeldab mõningaid juurutamisotsuseid, mida tuleb arvestada, kui kasutate rakenduses Microsoft Dynamics 365 for Operations paremalt vasakule keelt, ja peate seadistama finantsdimensioonid ja põhikontod.

Finantsdimensioonid ja põhikontod on juurutamise plaanimisfaasi põhikomponendid. Pärast finantsdimensioonide ja põhikontode loomist süsteemis kasutatakse neid lehtedel **Konto struktuuride konfigureerimine**, **Täpsemad konto struktuurid** ja **Finantsdimensiooni konfiguratsioon rakenduste integreerimiseks**. Nendel lehtedel määratletud tellimust kasutatakse andmete sisestamise ja tarbimise süsteemis. Mõnes süsteemis kohas ilmuvad finantsdimensioonid ja põhikontod eraldi väljadel. Teistes kohtades, nagu töölehed, finantsdimensioonid ja põhikontod, ilmuvad need ühe stringina.

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Parimad tavad finantsdimensioonide ja põhikontode seadistamiseks paremalt vasakul süsteemis

-   Kui valite kontoplaanide jaoks eraldaja, valige üks eraldaja suvanditest: kaks sidekriipsu (--), kaks pulka (||), kaks punkti (..) või kaks allkriipsu (\_\_).
-   Finantsdimensiooni ja põhikonto väärtuste loomisel kasutage ainult numbreid ja paremalt vasakule keele märke.
-   Vältige valitud kontoplaani eraldaja kasutamist finantsdimensiooni ja põhikonto väärtustes.

Neid parimaid tavasid järgides saate tagada kasutaja määratletud tellimuse pideva tähistamise kogu süsteemis.




