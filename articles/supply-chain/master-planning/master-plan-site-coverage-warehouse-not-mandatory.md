---
title: Koondplaanimine laoala varudele, ladu ei ole kohustuslik
description: Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala kattedimensioonidena.
author: ChristianRytt
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 484b178f3ac43f727fd6acb5deb40b7907c931ec
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579612"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a>Koondplaanimine laoala varudele, ladu ei ole kohustuslik

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala kattedimensioonidena.

See koondplaneerimise stsenaarium sisaldab järgmisi tingimusi.

-   Laoala dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse.
-   Lao dimensioon ei ole seatud kohustuslikuks. Ladu võib olla teada, kuid seda ei kasutata koondplaneerimise arvutamisel.
-   Saidi dimensioon on seadistatud laovarude planeerimiseks.
-   Lao dimensioon ei ole seadistatud laovarude planeerimiseks. Seega on tarne ja nõudlus ning võibolla ka teised laovarude planeerimisega dimensioonid koondatud saitide kaupa.

Järgmine graafik näitab, kuidas koondplaneerimine jätkub. Parameetrid, mis on graafikusse kantud, ja nende asukohad, on järgnevad:
-   Kauba laovarud on kauba kohta määratud. Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**. Valige kaup ja klõpsake siis valikuid **Plaan &gt; Kauba laovarud**.
-   Taastäitmise suhted on laole määratud. Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**. Vaadake vahekaardil **Koondplaneerimine** väljagruppi **Pealadu**.
-   Tellimuse vaiketüübiks on määratud Tootmine, Ostutellimus või Kanban. Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**. Valige kaup ja klõpsake siis valikuid **Plaan &gt; Tellimuse vaikesätted**. Vaadake vormi **Tellimuse vaikesätted** välja **Tellimuse vaiketüüp**.

![Nõue laoala varude laole pole kohustuslik.](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



## <a name="additional-resources"></a>Lisaressursid

[Koondplaneerimine ja mitme tegevuskoha funktsiooni ülevaade](master-plan-multisite-functionality.md)

[Laoala ja lao katmise koondplaanimine, ladu on kohustuslik](master-plan-site-coverage-warehouse-mandatory.md)

[Koondplaanimine laovarude puhul, kohustuslik ladu](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Koondplaanimine laovarude puhul, ladu ei ole kohustuslik](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Koosluse versiooni määratlemine](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]