---
title: Kaubastamisolemite sortimisjärjestuse muutmine
description: See artikkel selgitab eri tootega seotud üksuste kuvamisjärjestuse juhtimisega seotud mõisteid Dynamics 365 Commerce.
author: josaw1
ms.date: 08/11/2022
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
ms.openlocfilehash: 80586597f4f60476b341e4cf1cfd90f3681e15c0
ms.sourcegitcommit: 52e31b1ef2b3ed8675de931d06090cd57e057fc2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9265832"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>Kaubastamisolemite sortimisjärjestuse muutmine


[!Include [banner](includes/banner.md)]

Jaemüüjad peavad toodete avastamist esmaseks vahendiks klientidega suhtlemisel kõigis kanalites. Klientidel on mitmeid funktsioone, mis aitavad tooteid hõlpsasti avastada. Näiteks saavad kliendid sirvida kategooriaid, otsida ja filtreerida.

See artikkel selgitab eri tootega seotud üksuste kuvamisjärjestuse juhtimisega seotud mõisteid. Samuti selgitatakse, kuidas muuta sortimisjärjestust.

## <a name="overview"></a>Ülevaade

Äris on erinevate teenusega seotud üksuste sortimine joondatud olemasolevate kliendistsenaariumidega ja ei vaja enam rakenduspartnerite laiendiid.

Äriversioonides 10.0.5 ja varasemas oli kategooriate sortimisjärjestus navigeerimishierarhias tähestikuline. Praegune kohandatud sortimisjärjestuse funktsioon võimaldab tootejuhil konfigureerida eri tootega seotud üksuste sortimisjärjestust kõigi lõppkasutaja klientide lõikes. Need kliendid hõlmavad nii peakontoreid ja kõnekeskuseid.

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
5. Puus valige Moeriietus **\>, Naised \>, Kingid**.
6. Väljale **Kuvamisjärjestus** sisestage arv.
7. Puus valige **Mood \> Naiste rõivad \> Pluusid**.

Samuti saate määratleda alamkategooriate sortimisjärjestuse.

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
> Vaikimisi on funktsioon **Luba kuvamisjärjestus tooteüksuste jaoks välja** lülitatud. Funktsioonihalduse [abil](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) saate selle sisse lülitada. Pärast funktsiooni häälestamist käivitage jaotusgraafikust **globaalne konfiguratsioon -1110** CDX-töö.
> Kui teie kategooriate kassatellimust ei uuendata, aktiveerige seade uuesti. Kategooria teave toidetakse seadme aktiveerimisel, seega võib seadmel tekkida vajadus kategooria teave ümber lükkada uuendatud kuvatellimustega. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
