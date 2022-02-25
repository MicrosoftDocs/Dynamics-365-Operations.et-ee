---
title: Meiliteatiste profiili seadistamine
description: See teema kirjeldab, kuidas luua rakenduses Microsoft Dynamics 365 Commerce meiliteatiste profiil.
author: bicyclingfool
ms.date: 02/11/2022
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
ms.openlocfilehash: 9f7adffd67e8198d16e4f7ed4fc4aadf59071b1d
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109627"
---
# <a name="set-up-an-email-notification-profile"></a>Meiliteatise profiili seadistamine

[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas luua rakenduses Microsoft Dynamics 365 Commerce meiliteatiste profiil.

Kanalite loomisel saate seadistada meili teatise profiili. Meiliteatise profiil määratleb müügikande sündmused (nt loodud tellimus, tellimuse pakitud ja arveldatud sündmused), mille kohta saadate teatised oma klientidele. 

Lisateavet meili konfigureerimise kohta vt teemast [Meili konfigureerimine ja saatmine](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="create-an-email-notification-profile"></a>Meiliteatiste profiili loomine

Meiliteatiste profiili loomiseks toimige järgmiselt.

1. Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Headquartersi seadistus \> Commerce’i meiliteavituse profiil**.
1. Klõpsake toimingupaanil valikut **Uus**.
1. Sisestage väljale **Meiliteatiste profiil** profiili tuvastamiseks nimi.
1. Väljale **Kirjeldus** sisestage asjakohane kirjeldus.
1. Määrake lüliti **Aktiivne** olekusse **Jah**.

### <a name="create-an-email-template"></a>Loo e-kirja mall

Enne meiliteatise tüübi lubamist peate igas toetatavas teavitustüübis Commerce Headquarters looma organisatsiooni meilimalli. Mall määratleb iga toetatud keele jaoks meili teema, saatja, vaikekeele ja meili keha.

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

Lisateavet meilimallide loomise kohta vt teemast Kandesündmuste [jaoks meilimallide loomine](email-templates-transactions.md). 

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
> Kliendi loodud teatise tüüp nõuab kohandust, mis tuleb rakendada enne meiliteatise saatmist.

### <a name="schedule-a-recurring-email-notification-process-job"></a>Korduva meiliteatise protsessi töö plaanimine

Meiliteatiste saatmiseks peab teil olema käitatud **jaemüügitellimuse meiliteatise** töö.

Jaemüügitellimuse meiliteatise **töö töötlemise häälestamiseks** Commerce Headquartersis, kui te pole seda juba teinud, järgige neid samme.

1. Minge jaemüügi ja **rakenduse Commerce \> Retail ja Commerce IT meili ja \> teatiste saatmine meiliteatise \> saatmiseks**.
1. Jaemüügitellimuse **meiliteatise töötlemise dialoogiboksis** valige **kordumine**.
1. Valige dialoogiboksis **Kordumise** määratlemine suvand **Lõppkuupäev puudub**.
1. Valige jaotises **Kordumismuster** **väärtus Minutes** (Minutid) ja seejärel määrake välja **Arv väärtuseks** **1**. Need sätted tagavad meiliteatiste töötlemise võimalikult kiiresti.
1. Valige **OK**, et naasta jaemüügitellimuse **meiliteatise töötlemise dialoogiboksi**.
1. Tööseadistuse **lõpetamiseks valige OK**.

### <a name="next-steps"></a>Järgmised sammud

Enne e-kirjade saatmist peate konfigureerima oma väljamineva e-posti teenuse ja seadistama pakett-töö. Lisateavet vt teemast [Meilisõnumi konfigureerimine ja saatmine](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).

## <a name="additional-resources"></a>Lisaressursid

[Meilisõnumi konfigureerimine ja saatmine](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[Kanalite ülevaade](channels-overview.md)

[Kanali seadistamise eeltingimused](channels-prerequisites.md)

[Organisatsioonide ja organisatsioonihierarhiate ülevaade](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
