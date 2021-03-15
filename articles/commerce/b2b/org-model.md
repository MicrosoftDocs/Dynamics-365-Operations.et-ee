---
title: B2B organisatsioonidele organisatsiooni modelleerimise hierarhiate loomine.
description: Selles teemas kirjeldatakse, kuidas luua organisatsioonilised modelleerimishierarhiad ettevõtetevahelistele (B2B) organisatsioonidele.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 450efd595a1cc1b72b2e62afbdd4518bcca59cb0
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035895"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a>B2B organisatsioonidele organisatsiooni modelleerimise hierarhiate loomine.

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas luua organisatsioonilised modelleerimishierarhiad ettevõtetevahelistele (B2B) organisatsioonidele rakenduses Microsoft Dynamics 365 Commerce.

Äripartneri organisatsioone esindavad Commerce'i peakontoris klient ja kliendi hierarhia üksused. Äripartneri organisatsioon ja selle kasutajad on esindatud klientidena ning kliendihierarhiaid kasutatakse nende klientide üksteisega seostamiseks.

Kui äripartneri taotlus B2B e-kaubanduse saidiga liitumiseks kinnitatakse, sooritatakse järgmised toimingud.

- Süsteemis luuakse kaks uut kliendikirjet: kliendikirje **Tüüp Organisatsioon** äripartneri organisatsioonile ja kliendikirje **Tüüp Isik** taotlejale (see on äripartneri kasutaja, kes taotluse esitas).
- Uus kliendi hierarhia kirje luuakse jaotisesse **Klient \> Kliendi hierarhia**. Kirjel on järgmised päise atribuudid.

    - **Kliendi hierarhia ID** - kliendi hierarhia kordumatu ID. See ID kasutab numbriseeriat, mis on määratletud Commerce'i peakontori ühisparameetrites Commerce'i peakontoris.
    - **Nimi** - äripartneri organisatsiooni nimi, nagu on määratletud liitumistaotluses.
    - **Eesmärk** - see atribuut on seadistatud eelmääratletud väärtusele **B2B organisatsioon**.
    - **Organisatsioon** - äripartneri kliendi ID.

Siin on kliendi hierarhia kirje üksikasjad.

- Taotleja kliendikirje on seotud kliendi hierarhiaga.
- Administraatori roll on seotud taotlejaga.

Kui administraator lisab äripartneri organisatsioonile B2B-saidil veel kasutajaid, luuakse Commerce'i peakontoris igale loodud kasutajale uus kliendikirje. See kliendikirje lisatakse ka äripartneri vastavale kliendi hierarhia kirjele ja sellel on roll "Kasutaja".

> [!NOTE]
> Enamasti peaksid hierarhia kõigi kliendikirjete vastavad atribuudi väärtused ühtima. Näiteks, kuna kõik äripartneri kasutajad peaksid saama toodetele sarnaseid hindu, peavad nende hinnagrupp ja seotud konfiguratsioonid ühtima. Süsteem ei jõusta siiski seda ühtsust. Seetõttu vastutavad asjakohased Commerce'i peakontori kasutajad selle eest, et atribuudi väärtused ja konfiguratsioonid ühtiksid kõigi antud hierarhia klientidega.

Commerce peakontori kasutajad saavad hierarhia kõikide kliendikirjete atribuudi väärtusi vaadata kõrvuti vaates. Valige soovitud kliendikirje atribuudid, valides rippmenüüst vahekaardi nimed. Kasutajad saavad selle vaate kaudu otse atribuudi väärtusi vaadata ja redigeerida. Teise võimalusena, kui soovite kõik administraatori kliendikirje väärtused rakendada ka kõigile kasutaja kliendikirjetele, valige kliendi hierarhia üksikasjade all valik **Alistamine**.

## <a name="additional-resources"></a>Lisaressursid

[B2B e-kaubanduse saidi seadistamine](set-up-b2b-site.md)

[Äripartnerist kasutajate haldamine B2B e-kaubanduse saitidel](manage-b2b-users.md)

[Kliendikonto makseviisi konfigureerimine B2B e-kaubanduse saitide jaoks](payment-method.md)

[Toote koguse piirangute määramine B2B e-kaubanduse saitide jaoks](quantity-limits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]