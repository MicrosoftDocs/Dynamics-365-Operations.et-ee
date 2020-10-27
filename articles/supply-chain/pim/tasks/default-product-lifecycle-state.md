---
title: Toote elutsükli vaikeoleku loomine
description: See protseduur näitab, kuidas luua toote elutsükli vaikeolekut ja kuidas seostada vaikeolekut väljastatud toodetega.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8766208f0dff0cf24db7335ef00c42749811f8fd
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985433"
---
# <a name="create-a-default-product-lifecycle-state"></a>Toote elutsükli vaikeoleku loomine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas luua toote elutsükli vaikeolekut ja kuidas seostada vaikeolekut väljastatud toodetega.


## <a name="create-a-default-lifecycle-state"></a>Elutsükli vaikeoleku loomine
1. Avage Tooteteabe haldus > Häälestus > Toote elutsükli olek.
2. Klõpsake valikut Uus.
3. Tippige väärtus väljale Olek.
4. Väljal Vaikesäte juriidilisele isikule väljastamisel valige Jah.
5. Sisestage väljale Kirjeldus soovitud väärtus.
6. Valige Ei väljal On planeerimiseks aktiivne.

> [!NOTE]
> Kui uut väljastatud toodet ei ole vaja koondplaneerimisse kaasta, valige Ei. Kui see tuleks koondplaneerimisse kaasata, säilitage juhtelemendi vaikeväärtus Jah.  

## <a name="create-a-new-released-product"></a>Uue väljastatud toote loomine
1. Sulgege leht.
2. Avage Tooteteabe haldus > Tooted > Väljastatud tooted.
3. Klõpsake valikut Uus.
4. Sisestage väärtus väljale Toote number.
5. Sisestage väärtus väljale Toote nimi.
6. Sisestage väärtus väljale Otsingunimi.
7. Sisestage või valige väärtus väljal Kauba mudeligrupp.
8. Sisestage või valige väärtus väljal Kaubagrupp.
9. Sisestage või valige väärtus väljal Laoala dimensioonigrupp.
10. Sisestage või valige väärtus väljal Jälgimisdimensioonigrupp.
11. Klõpsake nuppu OK.

> [!NOTE]
> Toote elutsükli vaikeolek on globaalne määratlus.  

## <a name="change-the-product-to-an-active-state"></a>Toote aktiivsesse olekusse määramine
1. Väljal Toote elutsükli olek sisestage või valige väärtus.

> [!NOTE]
> Oletame, et aktiivne olek on seadistatud, mis tähendab, et saate nüüd aktiivse oleku valida ja lubada toodet kasutada koondplaneerimisel ja koosluse taseme arvutamisel. See on loogiline ainult juhul, kui kõik ühtse planeerimise jaoks vajalikud toodete üksikasjad on määratud.  

