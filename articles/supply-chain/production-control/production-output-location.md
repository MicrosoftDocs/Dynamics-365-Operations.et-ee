---
title: Tootmise väljundasukoht
description: Selles teemas kirjeldatakse hierarhiat, mida kasutatakse tootmise väljundasukoha tuvastamiseks.
author: johanhoffmann
manager: tfehr
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8fa4f7d844c178ee603778fa2f1def6bfc33db97
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209439"
---
# <a name="production-output-location"></a>Tootmise väljundasukoht

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse hierarhiat, mida kasutatakse tootmise väljundasukoha tuvastamiseks.

Tootmise väljundasukoht on asukoht, kus lõpetatud kaupu pärast tootmist kõigepealt hoitakse. Tavaliselt on see asukoht lõpetatud kaupu tootva tootmisprotsessi lähedal. Tootmise väljundasukohta kasutatakse materjali vahehoidlana, enne kui see viiakse saatmisalale, laoasukohta, tootmise sisendasukohta allavoolu tootmisprotsessi puhul jne. 

Tootmise vauikeasukoht määratakse siis, kui lõpetatud kaubad raporteeritakse tootmistellimusel või partiitellimusel. Selle väljundasukoha tuvastamiseks kasutatakse järgmist hierarhiat.

1. Tootmistellimuse või partiitellimuse päises määratletud väljundasukoha kasutamine.
2. Kui asukohta siit ei leita, kasutatakse väljundasukohta, mis on määratletud tootmisprotsessis määratletud viimase toimingu kasutatud ressursis.
3. Kui asukohta siit ei leita, kasutatakse väljundasukohta, mis on määratletud tootmisprotsessis määratletud viimase toimingu ressursi kasutatud ressursigrupis.
4. Kui asukohta siit ei leita, kasutatakse väljundasukohta, mis on määratletud tootmistellimuse jaoks määratud laos.

Tootmise vaike-väljundasukoht määratakse ainult toodetele, mis on seadistatud täpsemate laoprotsesside kasutamisega. Kui seda tüüpi kaup raporteeritakse lõpetatuks, luuakse laotöö tüübiga **Lõpetatud toodete kõrvalepanek** või **Kaastoote ja kõrvalsaaduse kõrvalepanek**. Seda tüüpi töö kasutab tootmise väljundasukohta komplekteerimisasukohana. Kõrvalepaneku asukoht määratakse asukohakorraldustega.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]