---
title: Kaubastamisolemite sortimisjärjestuse muutmine
description: Selles teemas selgitatakse mõisteid, mis on seotud erinevate kaubastamisega seotud olemite kuvamisjärjestuse juhtimisega rakenduses Microsoft Dynamics 365 for Retail.
author: ashishharchwani
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2be3c1198ac6fff851be1bead2f0995202f1f0e7
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2019
ms.locfileid: "1866157"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Kaubastamisolemite sortimisjärjestuse muutmine

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Jaemüüjad peavad toodete avastamist esmaseks vahendiks klientidega suhtlemisel kõigis jaemüügikanalites. Erinevad funktsioonid aitavad klientidel tooteid hõlpsasti avastada. Näiteks saavad nad sirvida kategooriaid, otsida ja filtreerida.

Selles teemas selgitatakse mõisteid, mis on seotud erinevate kaubastamisega seotud olemite kuvamisjärjestuse juhtimisega. Samuti selgitatakse, kuidas muuta sortimisjärjestust.

## <a name="overview"></a>Ülevaade

Erinevate kaubastamisega seotud olemite sorteerimise tuge on täiustatud. Tugi on nüüd paremini ühitatud olemasolevate kliendi stsenaariumitega, mis varem vajasid laiendusi juurutuspartneritelt.

Rakenduse Microsoft Dynamics 365 for Retail versioonides, mis on varasemad kui versioon 10.0.5, oli kategooriate sortimisjärjestus navigeerimise hierarhias tähestikuline. Uus kohandatud sortimisjärjestuse funktsioon laseb kaubastamise juhtidel konfigureerida sortimisjärjestust erinevatele kaubastamisega seotud olemitele kõigi lõppkasutaja klientide hulgas. Need kliendid hõlmavad nii peakontoreid ja kõnekeskuseid.

## <a name="configure-the-display-order-for-categories-in-the-retail-product-hierarchy"></a>Kategooriate kuvamisjärjestuse konfigureerimine jaemüügi tootehierarhias

Enne selle protseduuri lõpetamist, peate installima demoandmed oma keskkonda.

1. Avage **Jaemüük \> Tooted ja kategooriad \> Jaemüügi tootehierarhia**.
2. Klõpsake **Redigeeri kategooriahierarhiat**.
3. Klõpsake valikut **Redigeeri**.
4. Puus laiendage **KÕIK \> Tegevussport**.
5. Puus laiendage **KÕIK \> Meeskonnasport**.
6. Väljale **Kuvamisjärjestus** sisestage arv. (Arv ei saa olla negatiivne.)
7. Korrake juhiseid 4–6 iga lisatava kategooria puhul, mille järjestust soovite muuta.

Kanali navigeerimise hierarhia kuvamisjärjestus kajastub peakontoris jaemüügi tootehierarhias ja väljastatud toodetes kategooriate kaupa.

![Kohandatud jaemüügi tootehierarhia sorteeritud negatiivsete väärtustega](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Kohandatud väljastatud tooted kategooriate kaupa jaemüügi tootehierarhia põhjal](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>Kategooriate kuvamisjärjestuse konfigureerimine kanali navigeerimise hierarhias

Enne selle protseduuri lõpetamist, peate installima demoandmed oma keskkonda.

1. Avage **Jaemüük \> Tooted ja kategooriad \> Kanali navigeerimise kategooriad**.
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

Kategooriate kuvamisjärjestuse konfigureerimine kanali navigeerimise hierarhias kajastub peakontoris, kataloogis ja jaemüügi kanalites.

![Kohandatud sorteeritud kataloogi navigeerimise hierarhia](./media/ChannelNavCustomSorted.png)

![Kanali navigeerimise hierarhia põhjal kohandatud sorteeritud kataloogi navigeerimise hierarhia](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![Müügikoht kohandatud sorteeritud kategooriatega](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> Kohandatud sortimisjärjestuse funktsioon on vaikimisi välja lülitatud. Selle ja paljude teiste funktsiooni sisselülitamiseks vaadake teemat [Funktsioonide haldus](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).
