---
title: Koondplaanimine laoala ja laovarude jaoks, ladu on kohustuslik
description: Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala ja varud kattedimensioonidena. Lao dimensioon on kohustuslik.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: a0931d88f84544160803e42466575c02f47588a4
ms.lasthandoff: 03/31/2017


---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a>Koondplaanimine laoala ja laovarude jaoks, ladu on kohustuslik

[!include[banner](../includes/banner.md)]


Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala ja varud kattedimensioonidena. Lao dimensioon on kohustuslik.

See koondplaneerimise stsenaarium sisaldab järgmisi tingimusi.

-   Laoala dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse.
-   Lao dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse.
-   Laoala ja lao dimensioonid seadistatakse laovarude plaanimiseks. Muidki dimensioone võib seadistada laovarude plaanimiseks. Mitme laoala režiimi funktsioonid neid siiski ei mõjuta.

Järgmine graafik näitab, kuidas koondplaneerimine jätkub. Parameetrid, mis on graafikusse kantud, ja nende asukohad, on järgnevad:
-   Ladu on seatud **Käsitsi** peale. Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**. Vaadake kiirkaardil **Koondplaneerimine** välja **Käsitsi**.
-   Kauba laovarud on kauba kohta määratud. Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**. Valige kaup ja seejärel klõpsake tegumiribal vahekaardil **Plaan** valikut **Kauba laovarud**.
-   Taastäitmise suhted on laole määratud. Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**. Vaadake kiirkaardil **Koondplaneerimine** väljagruppi **Pealadu**.
-   Tellimuse vaiketüübiks on määratud Tootmine, Ostutellimus või Kanban. Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**. Valige kaup ja seejärel klõpsake tegumiribal vahekaardil **Plaan** valikut **Tellimuse vaikesätted**. Vaadake vormi **Tellimuse vaikesätted** jaotist **Tellimuse vaiketüüp**.

![Nõude laoala ja laovarud, ladu kohustuslik](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="see-also"></a>Vt ka
--------

[Koondplaanimine ja mitme laoala funktsioon](master-plan-multisite-functionality.md)

[Koondplaneerimine – laovarud, ladu on kohustuslik](master-plan-site-coverage-warehouse-mandatory.md)

[Koondplaneerimine – laovarud, ladu ei ole kohustuslik](master-plan-site-coverage-warehouse-not-mandatory.md)

[Koondplaneerimine – laoala ja laovarud, ladu ei ole kohustuslik](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[Koondplaneerimine – koosluse versiooni määratlemine](master-plan-bom-version-determined.md)



