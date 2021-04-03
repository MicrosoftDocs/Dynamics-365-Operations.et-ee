---
title: Plaanitud tellimuste kinnitamine
description: Selles teemas kirjeldatakse plaaneerimise optimeerimise korral toetatud plaanitud tellimuste kinnitamist.
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 8745a461986c1f16f2b3f9fd23011701d104a30c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264014"
---
# <a name="approve-planned-orders"></a>Plaanitud tellimuste kinnitamine

[!include [banner](../../includes/banner.md)]

See kirjeldab, kuidas planeerimise optimeerimise korral värskendada plaanitud tellimuste olekut.

Pidage meeles, et plaanitud tellimuste kinnitamine on valikuline etapp plaanitud tellimuse kinnitatud tellimuseks muutmisel. Soovitatav on kinnitada muudetud plaanitud tellimused, vastasel juhul ignoreeritakse muudatusi ja need kirjutatakse üle järgmise plaanimise käitamisel.

![Plaanitud tellimuse voog](media/approved-planned-orders-1.png)

Väli **Olek** aitab teil jälgida edenemist järgmiste väärtuste abil.

- **Töötlemata:** kui koondplaneerimine loob plaanitud tellimused, on nende olek *Töötlemata*. Selle olekuga plaanitud tellimused kustutatakse järgmise plaanimise käitamisel.
- **Lõpetatud:** kui otsustate plaanitud tellimust mitte kinnitada, saate muuta oleku *Lõpetatuks*, mis näitab, et olete selle plaanitud tellimuse hindamise lõpule viinud. Pange tähele, et süsteem käsitleb olekut *Töötlemata* ja *Lõpetatud* sama moodi.
- **Kinnitatud:** kui soovite muudatusi säilitada või plaanitud tellimuse kinnitada, muutke olekuks *Kinnitatud*. Olekuga *Kinnitatud* plaanitud tellimusi käsitletakse koondplaneerimisel fikseeritult ja eeldatavalt tarnitavatena, nii et neid ei muudeta ega kustutata hilisema koondplaneerimise käivitamiste ajal. Selle saavutamiseks kopeerib planeerimisloogika koondplaneerimise ajal *kinnitatud* plaanitud tellimused vana plaani versioonist uude plaani versiooni. Pange tähele, et *Kinnitatud* plaanitud tellimusi loetakse tarnitavateks ainult konkreetse koondplaani korral.

Saate planeeritud tellimusi hallata tööruumis **Koondplaneerimine**, loendis **Plaanitud tellimus** või loendites **Plaanitud tootmistellimused**, **Plaanitud ostutellimused** ja **Plaanitud üleviimised**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]