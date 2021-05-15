---
title: Varude blokeerimise loomine ja haldamine
description: Selles teemas kirjeldatakse, kuidas vältida füüsilise vaba kaubavaru reserveerimist teiste väljaminevate lähtedokumentidega, kasutades varude blokeerimist.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956154"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Varude blokeerimise loomine ja haldamine

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas vältida füüsilise vaba kaubavaru reserveerimist teiste väljaminevate lähtedokumentidega, kasutades varude blokeerimist. Enne seda teemat puudutava protseduuri alustamist peab teil olema füüsilise vaba kaubavaruga kaup saadaval.

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
