---
title: Kaubastamisolemite sortimisjärjestuse muutmine
description: See artikkel selgitab eri tootega seotud üksuste kuvamisjärjestuse juhtimisega seotud mõisteid Dynamics 365 Commerce.
author: josaw1
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4e7a7bd42b0ef72ae6bc3f52a8857602b6282907
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847650"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Kaubastamisolemite sortimisjärjestuse muutmine


[!Include [banner](includes/banner.md)]

Jaemüüjad peavad toodete avastamist esmaseks vahendiks klientidega suhtlemisel kõigis kanalites. Erinevad funktsioonid aitavad klientidel tooteid hõlpsasti avastada. Näiteks saavad nad sirvida kategooriaid, otsida ja filtreerida.

See artikkel selgitab eri tootega seotud üksuste kuvamisjärjestuse juhtimisega seotud mõisteid. Samuti selgitatakse, kuidas muuta sortimisjärjestust.

## <a name="overview"></a>Ülevaade

Erinevate kaubastamisega seotud olemite sorteerimise tuge on täiustatud. Tugi on nüüd paremini ühitatud olemasolevate kliendi stsenaariumitega, mis varem vajasid laiendusi juurutuspartneritelt.

Rakenduse Retail versioonides, mis on varasemad kui versioon 10.0.5, oli kategooriate sortimisjärjestus navigeerimise hierarhias tähestikuline. Uus kohandatud sortimisjärjestuse funktsioon laseb kaubastamise juhtidel konfigureerida sortimisjärjestust erinevatele kaubastamisega seotud olemitele kõigi lõppkasutaja klientide hulgas. Need kliendid hõlmavad nii peakontoreid ja kõnekeskuseid.

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a>Kategooriate kuvamisjärjestuse konfigureerimine tootehierarhias

Enne selle protseduuri lõpetamist, peate installima demoandmed oma keskkonda.

1. Avage **Jaemüük ja kaubandus \> Tooted ja kategooriad \> Kaubanduse tootehierarhia**.
2. Klõpsake **Redigeeri kategooriahierarhiat**.
3. Klõpsake valikut **Redigeeri**.
4. Puus laiendage **KÕIK \> Tegevussport**.
5. Puus laiendage **KÕIK \> Meeskonnasport**.
6. Väljale **Kuvamisjärjestus** sisestage arv. (Arv ei saa olla negatiivne.)
7. Korrake juhiseid 4–6 iga lisatava kategooria puhul, mille järjestust soovite muuta.

Kanali navigeerimise hierarhia kuvamisjärjestus kajastub peakontoris kaubanduse tootehierarhias ja väljastatud toodetes kategooriate kaupa.

![Kohandatud tootehierarhia sorteerimine negatiivsete väärtustega.](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Väljastatud tooted kategooriate kaupa tootehierarhia põhjal kohandatult sorteeritud.](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>Kategooriate kuvamisjärjestuse konfigureerimine kanali navigeerimise hierarhias

Enne selle protseduuri lõpetamist, peate installima demoandmed oma keskkonda.

1. Avage **Jaemüük ja kaubandus \> Tooted ja kategooriad \> Kanali navigeerimise kategooriad**.
2. Valige loendis hierarhia **Moe navigeerimine**.
3. Klõpsake **Redigeeri kategooriahierarhiat**.
4. Klõpsake valikut **Redigeeri**.
5. Puus valige **Mood \> Naiste rõivad \> Naiste kingad**.
6. Väljale **Kuvamisjärjestus** sisestage arv.
7. Puus valige **Mood \> Naiste rõivad \> Pluusid**.

    Samuti saate määratleda sortimisjärjestuse alamkategooriaid.

8. Puus valige **Mood \> Meeste rõivad \> Vabaaja särgid**.
9. Väljale **Kuvamisjärjestus** sisestage arv.
10. Puus valige **Mood \> Meeste rõivad \> Mantlid & jakid**.
11. Väljale **Kuvamisjärjestus** sisestage arv.
12. Korrake tegevust iga lisatava kategooria puhul, mille järjestust soovite muuta.

Kategooriate kuvamisjärjestuse konfigureerimine kanali navigeerimise hierarhias kajastub peakontoris, kataloogis ja kanalites.

![Kohandatud sorteeritud kataloogi navigeerimise hierarhia.](./media/ChannelNavCustomSorted.png)

![Kanali navigeerimise hierarhia põhjal kohandatud sorteeritud kataloogi navigeerimise hierarhia.](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![Müügikoht koos kohandatud sorteeritud kategooriatega.](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> Kohandatud sortimisjärjestuse funktsioon on vaikimisi välja lülitatud. Selle ja paljude teiste funktsiooni sisselülitamiseks vaadake teemat [Funktsioonide haldus](/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]