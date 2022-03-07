---
title: Sünkroniseeri kontsernisisesed hinnad ja allahindlused
description: See teema kirjeldab kontsernisiseste müügi- ja ostutellimuste hindade ja allahindluste sünkroniseerimist
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: a9467e8d06a44cfaab9e3c8ea3944675c3eb8fb5
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548207"
---
# <a name="synchronize-intercompany-prices-and-discounts"></a>Sünkroniseeri kontsernisisesed hinnad ja allahindlused

[!include [banner](../../includes/banner.md)]

Kontsernisiseste müügi- ja ostutellimuste allahindlused ja hinnad on alati sünkrooniseeritud. Samuti saate valida, kas sünkrooniseerida hinda ja allahindlusi algse müügitellimuse järgi või vastupidi nii, et kõigil tellimustel oleks ühtsed hinnad ja allahindlused. Seda saate teha **Kontsernisiseselt** leheküljelt, mille kaudu pääseb juurde vahekaardi **Üldine** loendilehe **Kõik kliendid** kaudu – kas **Müügist ja turundusest** või **Varumisest ja hankest**.

Väli **Hind ja allahindlus** sünkroonitakse kontsernisisese müügitellimuse rea järgi. See tähendab, et märkides ruudud **Luba hinna redigeerimine** ja **Luba allahindluse redigeerimine**, lubate kontsernisiseste müügi- ja ostutellimuste vahelisi muudatusi. Ühikuhinna, hinnaühiku või müügikulude muutmine kontsernisisesel müügitellimusel määratleb hinna kontsernisisese ostutellimuse real.

Kui kontsernisisesel müügi- või ostutellimusel on lubatud väljad **Luba hinna redigeerimine** ja **Luba allahindluse redigeerimine**, saate hinda või allahindlust kummalgi tellimusel käsitsi muuta. Vastasel juhul ei saa.

Kui kontsernisisesel müügitellimusel ei ole lubatud väljad **Luba hinna redigeerimine** ja **Luba allahindluse redigeerimine**, ei saa te kontsernisisese müügitellimuse hinda (või tasusid) ega allahindlust käsitsi muuta.

Kui kontsernisisesel ostutellimusel ei ole lubatud väljad **Luba hinna redigeerimine** ja **Luba allahindluse redigeerimine**, ei saa te kontsernisisese ostutellimuse hinda (või tasusid) ega allahindlust käsitsi muuta.

Kui kontsernisisesel müügi- ja ostutellimusel on lubatud väljad **Luba hinna redigeerimine** ja **Luba allahindluse redigeerimine**, saate hinda või allahindlust kummalgi tellimusel käsitsi muuta. See võib siiski põhjustada olukorra, kus ühe inimese tehtud uuendused alistatakse samal tellimusel teise isiku teises ettevõttes tehtud uuendustega.

> [!NOTE]
> Kui olete nii kontsernisisesel ostu- kui ka müügitellimusel märkinud välja **Hind ja allahindlus**, ei saa te hinnakujundust reguleerida.

Parim viis seda tüüpi konfliktide vältimiseks on lubada hindu ja allahindlusi muuta ainult kontsernisisestel müügitellimustel või kontsernisisestel ostutellimustel, kuid mitte mõlemal. Selleks lubatakse väljad **Luba hinna redigeerimine** ja **Luba allahindluse redigeerimine** mõlemas tellimuses.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
