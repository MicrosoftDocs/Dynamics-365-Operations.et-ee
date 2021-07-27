---
title: Kaubastamisolemite sortimisjärjestuse muutmine
description: Selles teemas selgitatakse mõisteid, mis on seotud erinevate kaubastamisega seotud olemite kuvamisjärjestuse juhtimisega rakenduses Dynamics 365 Commerce.
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
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: de8840b92307ba63d6d0c2cfa90536bd00696ec3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349670"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Kaubastamisolemite sortimisjärjestuse muutmine


[!include [banner](includes/banner.md)]

Jaemüüjad peavad toodete avastamist esmaseks vahendiks klientidega suhtlemisel kõigis kanalites. Erinevad funktsioonid aitavad klientidel tooteid hõlpsasti avastada. Näiteks saavad nad sirvida kategooriaid, otsida ja filtreerida.

Selles teemas selgitatakse mõisteid, mis on seotud erinevate kaubastamisega seotud olemite kuvamisjärjestuse juhtimisega. Samuti selgitatakse, kuidas muuta sortimisjärjestust.

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