---
title: Koondplaanimine laovarude puhul, kohustuslik ladu
description: Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala kattedimensioonidena. Ladu on kohustuslik dimensioon.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f61c142fff73fdeeca573cca3f54e654511af1e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "328328"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a>Koondplaanimine laovarude puhul, kohustuslik ladu

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala kattedimensioonidena. Ladu on kohustuslik dimensioon.

See koondplaneerimise stsenaarium sisaldab järgmisi tingimusi.

-   Laoala dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse. Seda sätet ei saa muuta.
-   Lao dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse.
-   Saidi dimensioon on seadistatud laovarude planeerimiseks. Ka teised dimensioonid võivad olla seatud laovarude planeerimiseks. Mitmesaidiline funktsioon siiski neid ei mõjuta.
-   Lao dimensioon ei ole seadistatud laovarude planeerimiseks. Seega on tarne ja nõudlus ning võibolla ka teised laovarude planeerimisega dimensioonid koondatud saitide kaupa.

Järgmine graafik näitab, kuidas koondplaneerimine jätkub. Parameetrid, mis on graafikusse kantud, ja nende asukohad, on järgnevad:
-   Kauba laovarud on kauba kohta määratud. Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**. Valige kaup ja klõpsake siis valikuid **Plaan &gt; Kauba laovarud**.
-   Taastäitmise suhted on laole määratud. Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**. Vaadake vahekaardil **Koondplaneerimine** väljagruppi **Pealadu**.
-   Tellimuse vaiketüübiks on määratud Tootmine, Ostutellimus või Kanban. Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**. Valige kaup ja klõpsake siis valikuid **Plaan &gt; Tellimuse vaikesätted**. Vaadake vormi **Tellimuse vaikesätted** jaotist **Tellimuse vaiketüüp**.

![Nõue laoala varude laole kohustuslik](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a>Lisaressursid
--------

[Koondplaneerimine ja mitme laoala režiim](master-plan-multisite-functionality.md)

[Koondplaneerimine – laoala ja laovarud, ladu on kohustuslik](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Koondplaanimine – laovarud, ladu on kohustuslik](master-plan-site-coverage-warehouse-mandatory.md)

[Koondplaneerimine – laoala ja laovarud, ladu ei ole kohustuslik](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Koondplaneerimine – koosluse versiooni määratlemine](master-plan-bom-version-determined.md)



