---
title: Meiliteatiste profiili seadistamine
description: See teema kirjeldab, kuidas luua rakenduses Microsoft Dynamics 365 Commerce meiliteatiste profiil.
author: bicyclingfool
ms.date: 02/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7a7d796a173a6f9dfcd62e1f73e078cac614145e
ms.sourcegitcommit: 2aca3a95d42403c7f5d80dcd5e3ee958dca5c894
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2022
ms.locfileid: "8087863"
---
# <a name="set-up-an-email-notification-profile"></a>Meiliteatise profiili seadistamine

[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas luua rakenduses Microsoft Dynamics 365 Commerce meiliteatiste profiil.

Kanalite loomisel saate seadistada meili teatise profiili. Meiliteatise profiil määratleb müügitehingu sündmused (nt loodud tellimus, tellimus pakitud ja tellige arveldatud sündmused), mille kohta saadate oma klientidele märguandeid. 

Lisateavet meili konfigureerimise kohta vt teemast [Meili konfigureerimine ja saatmine](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="create-an-email-notification-profile"></a>Meiliteatiste profiili loomine

Meiliteatiste profiili loomiseks toimige järgmiselt.

1. Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Headquartersi seadistus \> Commerce’i meiliteavituse profiil**.
1. Klõpsake toimingupaanil valikut **Uus**.
1. Sisestage väljale **Meiliteatiste profiil** profiili tuvastamiseks nimi.
1. Väljale **Kirjeldus** sisestage asjakohane kirjeldus.
1. Määrake lüliti **Aktiivne** olekusse **Jah**.

### <a name="create-an-email-template"></a>Loo e-kirja mall

Enne meiliteatise tüübi lubamist peate iga toetatava teatisetüübi jaoks looma Commerce'i peakontoris organisatsiooni meiliaadressimalli. See mall määratleb iga toetatud keele jaoks meiliteema, saatja, vaikekeele ja meilikeha.

Meilimalli loomiseks tehke järgmist.

1. Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Headquartersi seadistus \> Parameetrid \> Organisatsiooni meilimallid**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage väljale **Meili ID** ID, mis aitab selle malli tuvastada.
1. Sisestage väljale **Saatja nimi** saatja nimi.
1. Sisestage väljale **Meili kirjeldus** tähenduslik kirjeldus.
1. Sisestage väljale **Saatja meiliaadress** saatja meiliaadress.
1. Valige **Üldine** jaotises e-kirja malli jaoks vaikekeel. Vaikekeelt kasutatakse siis, kui määratud keele jaoks pole lokaliseeritud malli.
1. Laiendage jaotist **Meilisõnumi sisu** ja valige malli sisu loomiseks **Uus**. Valige iga sisuüksuse jaoks keel ja sisestage meili teema rida. Kui meil on kehatekst, veenduge, et märgitud on märkeruut **On kehatekst**.
1. Valige toimingupaanil **Meilisõnum**, et sisestada meili kehatekstile mall.

Järgmine pilt näitab mõningaid näiteid meilimalli sätetest.

![E-kirja malli sätted.](media/email-template.png)

Lisateavet meilimallide loomise kohta leiate teemast [Meilimallide loomine tehingusündmuste jaoks](email-templates-transactions.md). 

### <a name="create-an-email-event"></a>Meilisündmuse loomine

Meilisündmuse loomiseks tehke järgmist.

1. Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Headquartersi seadistus \> Commerce’i meiliteavituse profiil**.
1. Otsige loendist ja valige soovitud kirje. 
1. Valige ripploendist **Meili ID** meilimall.
1. Valige ripploendist sobiv **Meiliteatise tüüp**.
1. Märkige ruut **Aktiivne**.
1. Valige toimingupaanil nupp **Salvesta**.

Järgmine pilt näitab mõningaid näiteid sündmusest teavitamise sätetest.

![Sündmusest teavitamise sätted.](media/email-notification-profile.png)

> [!NOTE]
> Kliendi loodud teavitustüüp nõuab enne meiliteatise saatmist kohandamist.

### <a name="next-steps"></a>Järgmised sammud

Enne e-kirjade saatmist peate konfigureerima oma väljamineva e-posti teenuse ja seadistama pakett-töö. Lisateavet vt teemast [Meilisõnumi konfigureerimine ja saatmine](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="additional-resources"></a>Lisaressursid

[Meilisõnumi konfigureerimine ja saatmine](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Kanalite ülevaade](channels-overview.md)

[Kanali seadistamise eeltingimused](channels-prerequisites.md)

[Organisatsioonide ja organisatsioonihierarhiate ülevaade](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
