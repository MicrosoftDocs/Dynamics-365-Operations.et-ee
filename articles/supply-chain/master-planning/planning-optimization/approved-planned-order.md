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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: b7975088be898ccecceb1f7be009cecff107f6e6
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759684"
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
