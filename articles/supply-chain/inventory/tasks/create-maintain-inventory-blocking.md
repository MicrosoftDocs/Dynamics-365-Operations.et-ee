---
title: Varude blokeerimise loomine ja haldamine
description: See artikkel kirjeldab, kuidas kasutada varude blokeerimist, et vältida füüsilise vaba kaubavaru reserveerimist muude väljaminevate lähtedokumentidega.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba95b689bedfc76598dfa81548a074f4fb7c833a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859339"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Varude blokeerimise loomine ja haldamine

[!include [banner](../../includes/banner.md)]

See artikkel kirjeldab, kuidas kasutada varude blokeerimist, et vältida füüsilise vaba kaubavaru reserveerimist muude väljaminevate lähtedokumentidega. Enne selle artikli protseduuride käivitamist peab teil olema kaup, mille jaoks on füüsiline vaba kaubavaru saadaval.

## <a name="block-inventory"></a>Blokeeri varud

Varude blokeerimise kirje loomiseks selliselt, et inventar on blokeeritud, järgige neid samme.

1. Avage **Varude haldus \> Perioodilised ülesanded \> Inventari blokeerimine**.
1. Valige toimingupaanil nupp **Uus**.
1. Määrake uue blokeerimiskirje päises **kaubakoodi** väli kaubale, mida soovite blokeerida, ja sisestage kirjeldus.
1. Sisestage blokeeritavate kaupade arv kiirkaardi **Üldine** väljale **Kogus**.
1. Kiirkaardil **Varude dimensioonid** määrake sait ja ladu, kus asuvad kaubad, mida soovite blokeerida.
1. Valige toimingupaanil nupp **Salvesta**.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Varude blokeerimise tingimuste värskendamine

Varude blokeerimise kirje uuendamiseks järgige neid samme.

1. Avage **Varude haldus \> Perioodilised ülesanded \> Inventari blokeerimine**.
1. Valige loendipaanil asjakohane blokeerimiskirje.
1. Redigeerige kandeid nii, nagu vaja. Näiteks võite muuta välja **Oodatav kuupäev** väärtust näitamaks, millal blokeeritud inventar jälle reserveerimiseks vabaks antakse. Kui on valitud suvand **Oodatud sissetulekud**, kuvatakse kuupäev eeldataval kandel. (Välja **Eeldatud sissetulekud** suvand valitakse vaikimisi blokeeriva kirje käsitsi loomisel.)
1. Valige toimingupaanil nupp **Salvesta**.

## <a name="unblock-inventory"></a>Varude blokeeringu eemaldamine

Varude blokeerimise kirje eemaldamiseks selliselt, et inventar ei oleks enam blokeeritud, järgige neid samme.

1. Avage **Varude haldus \> Perioodilised ülesanded \> Inventari blokeerimine**.
1. Valige loendipaanil asjakohane blokeerimiskirje.
1. Valige tegumiribal suvand **Kustuta**.
1. Teil pakutakse tegevus kinnitada. Jätkamiseks valige **Jah**.
1. Sulgege leht.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
