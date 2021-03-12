---
title: Meiliteatiste profiili seadistamine
description: See teema kirjeldab, kuidas luua rakenduses Microsoft Dynamics 365 Commerce meiliteatiste profiil.
author: samjarawan
manager: annbe
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9378fb200a239433f2023bb90f72840dace1c0eb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000820"
---
# <a name="set-up-an-email-notification-profile"></a>Meiliteatiste profiili seadistamine


[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas luua rakenduses Microsoft Dynamics 365 Commerce meiliteatiste profiil.

## <a name="overview"></a>Ülevaade

Enne kanalite loomist tuleb seadistada profiili, et tagada meiliteatiste saatmine erinevate sündmuste korral, nt tellimuse loomine, tellimuse tarne olek ja makse tõrge.

Lisateavet meili konfigureerimise kohta vt teemast [Meili konfigureerimine ja saatmine](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="create-an-email-notification-profile"></a>Meiliteatiste profiili loomine

Meiliteatiste profiili loomiseks toimige järgmiselt.

1. Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Headquartersi seadistus \> Commerce’i meiliteavituse profiil**.
1. Klõpsake toimingupaanil valikut **Uus**.
1. Sisestage väljale **Meiliteatiste profiil** profiili tuvastamiseks nimi.
1. Väljale **Kirjeldus** sisestage asjakohane kirjeldus.
1. Määrake lüliti **Aktiivne** olekusse **Jah**.

### <a name="create-an-email-template"></a>Loo e-kirja mall

Enne kui meiliteavitusi luua saab, peate looma organisatsiooni meilimalli, mis sisaldab saatja meili andmeid ja meilimalli.

Meilimalli loomiseks tehke järgmist.

1. Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Headquartersi seadistus \> Parameetrid \> Organisatsiooni meilimallid**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage väljale **Meili ID** ID, mis aitab selle malli tuvastada.
1. Sisestage väljale **Saatja nimi** saatja nimi.
1. Sisestage väljale **Meili kirjeldus** tähenduslik kirjeldus.
1. Sisestage väljale **Saatja meiliaadress** saatja meiliaadress.
1. Täitke jaotises **Üldine** kõik vajalikud valikulised andmed (nagu näiteks meili prioriteetsus).
1. Laiendage jaotist **Meilisõnumi sisu** ja valige malli sisu loomiseks **Uus**. Valige iga sisuüksuse jaoks keel ja sisestage meili teema rida. Kui meil on kehatekst, veenduge, et märgitud on märkeruut **On kehatekst**.
1. Valige toimingupaanil **Meilisõnum**, et sisestada meili kehatekstile mall.

Järgmine pilt näitab mõningaid näiteid meilimalli sätetest.

![E-kirja malli sätted.](media/email-template.png)

### <a name="create-an-email-event"></a>Meilisündmuse loomine

Meilisündmuse loomiseks tehke järgmist.

1. Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Headquartersi seadistus \> Commerce’i meiliteavituse profiil**.
1. Otsige loendist ja valige soovitud kirje. 
1. Valige ripploendist **Meili ID** meilimall.
1. Valige ripploendist sobiv **Meiliteatise tüüp**.
1. Märkige ruut **Aktiivne**.
1. Valige toimingupaanil nupp **Salvesta**.

Järgmine pilt näitab mõningaid näiteid sündmusest teavitamise sätetest.

![Sündmusest teavitamise sätted](media/email-notification-profile.png)

### <a name="next-steps"></a>Järgmised etapid

Enne e-kirjade saatmist peate konfigureerima oma väljamineva e-posti teenuse ja seadistama pakett-töö. Lisateavet vt teemast [Meilisõnumi konfigureerimine ja saatmine](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).


## <a name="additional-resources"></a>Lisaressursid

[Meilisõnumi konfigureerimine ja saatmine](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Kanalite ülevaade](channels-overview.md)

[Kanali seadistamise eeltingimused](channels-prerequisites.md)

[Organisatsioonide ja organisatsioonihierarhiate ülevaade](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
