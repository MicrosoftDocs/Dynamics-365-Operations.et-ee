---
title: Tootmise väljundasukoht
description: See artikkel kirjeldab hierarhiat, mida kasutatakse toodangu väljastuskoha tuvastamiseks.
author: johanhoffmann
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 130db343c4d09f2b8d31bf8acad3dcceec2be32e
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067937"
---
# <a name="production-output-location"></a>Tootmise väljundasukoht

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab hierarhiat, mida kasutatakse toodangu väljastuskoha tuvastamiseks.

Tootmise väljundasukoht on asukoht, kus lõpetatud kaupu pärast tootmist kõigepealt hoitakse. Tavaliselt on see asukoht lõpetatud kaupu tootva tootmisprotsessi lähedal. Tootmise väljundasukohta kasutatakse materjali vahehoidlana, enne kui see viiakse saatmisalale, laoasukohta, tootmise sisendasukohta allavoolu tootmisprotsessi puhul jne. 

Tootmise vauikeasukoht määratakse siis, kui lõpetatud kaubad raporteeritakse tootmistellimusel või partiitellimusel. Selle väljundasukoha tuvastamiseks kasutatakse järgmist hierarhiat.

1. Tootmistellimuse või partiitellimuse päises määratletud väljundasukoha kasutamine.
2. Kui asukohta siit ei leita, kasutatakse väljundasukohta, mis on määratletud tootmisprotsessis määratletud viimase toimingu kasutatud ressursis.
3. Kui asukohta siit ei leita, kasutatakse väljundasukohta, mis on määratletud tootmisprotsessis määratletud viimase toimingu ressursi kasutatud ressursigrupis.
4. Kui asukohta siit ei leita, kasutatakse väljundasukohta, mis on määratletud tootmistellimuse jaoks määratud laos.

Vaikimisi on toodangu väljastuskoht seadistatud ainult toodetele, mis on seadistatud laohaldusprotsesse (WMS) kasutades. Kui seda tüüpi kaup raporteeritakse lõpetatuks, luuakse laotöö tüübiga **Lõpetatud toodete kõrvalepanek** või **Kaastoote ja kõrvalsaaduse kõrvalepanek**. Seda tüüpi töö kasutab tootmise väljundasukohta komplekteerimisasukohana. Kõrvalepaneku asukoht määratakse asukohakorraldustega.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]