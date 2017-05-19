---
title: Koondplaanimine laoala ja laovarude jaoks, ladu ei ole kohustuslik
description: Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala ja varud kattedimensioonidena. Lao dimensioon ei ole kohustuslik.
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
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 17ca8d575b4c89d50e05a492e810ad6de7610c11
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a>Koondplaanimine laoala ja laovarude jaoks, ladu ei ole kohustuslik

[!include[banner](../includes/banner.md)]


Selles teemas kirjeldatakse, kuidas plaanitakse kaupa, millel on laoala ja varud kattedimensioonidena. Lao dimensioon ei ole kohustuslik.

See koondplaneerimise stsenaarium sisaldab järgmisi tingimusi.

-   Laoala dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse. Seda sätet ei saa muuta.
-   Lao dimensioon ei ole seatud kohustuslikuks. Ladu võib olla teada, kuid seda ei kasutata koondplaneerimise arvutamisel.
-   Laoala ja lao dimensioonid seadistatakse laovarude plaanimiseks. Muidki dimensioone võib seadistada laovarude plaanimiseks. Mitme laoala režiimi funktsioonid neid siiski ei mõjuta.

Järgmine graafik näitab, kuidas koondplaneerimine jätkub. Parameetrid, mis on graafikusse kantud, ja nende asukohad, on järgnevad:
-   Ladu on seatud Käsitsi peale. Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**. Vaadake kiirkaardil **Koondplaneerimine** välja **Käsitsi**.
-   Kauba laovarud on kauba kohta määratud. Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**. Valige kaup ja seejärel klõpsake tegumiribal vahekaardil **Plaan** valikut **Kauba laovarud**.
-   Taastäitmise suhted on laole määratud. Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**. Vaadake kiirkaardil **Koondplaneerimine** väljagruppi **Pealadu**.
-   Tellimuse vaiketüübiks on määratud Tootmine, Ostutellimus või Kanban. Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**. Valige kaup ja seejärel klõpsake tegumiribal vahekaardil **Plaan** valikut **Tellimuse vaikesätted**. Vaadake vormi **Tellimuse vaikesätted** jaotist **Tellimuse vaiketüüp**.

![Nõude laoala ja laovarud, ladu pole    ](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)

 
-



<a name="see-also"></a>Vt ka
--------

[Koondplaanimine ja mitme laoala funktsioon](master-plan-multisite-functionality.md)

[Koondplaneerimine – laoala ja laovarud, ladu on kohustuslik](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[Koondplaneerimine – laovarud, ladu on kohustuslik](master-plan-site-coverage-warehouse-mandatory.md)

[Koondplaneerimine – laovarud, ladu ei ole kohustuslik](master-plan-site-coverage-warehouse-not-mandatory.md)

[Koondplaneerimine – koosluse versiooni määratlemine](master-plan-bom-version-determined.md)




