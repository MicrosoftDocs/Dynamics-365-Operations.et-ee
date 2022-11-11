---
title: Koondplaanimine laovarude puhul, kohustuslik ladu
description: See artikkel kirjeldab, kuidas planeeritakse laoala laovarude dimensiooniga kaupa. Ladu on kohustuslik dimensioon.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df58017c25737cc946d09bf86ff7ad8bd33f4176
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741036"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a>Koondplaanimine laovarude puhul, kohustuslik ladu

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas planeeritakse laoala laovarude dimensiooniga kaupa. Ladu on kohustuslik dimensioon.

See koondplaneerimise stsenaarium sisaldab järgmisi tingimusi.

-   Laoala dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse. Seda sätet ei saa muuta.
-   Lao dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse.
-   Saidi dimensioon on seadistatud laovarude planeerimiseks. Ka teised dimensioonid võivad olla seatud laovarude planeerimiseks. Mitmesaidiline funktsioon siiski neid ei mõjuta.
-   Lao dimensioon ei ole seadistatud laovarude planeerimiseks. Seega on tarne ja nõudlus ning võibolla ka teised laovarude planeerimisega dimensioonid koondatud saitide kaupa.

Järgmine graafik näitab, kuidas koondplaneerimine jätkub. Parameetrid, mis on graafikusse kantud, ja nende asukohad, on järgnevad:
-   Kauba laovarud on kauba kohta määratud. Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**. Valige kaup ja klõpsake siis valikuid **Plaan &gt; Kauba laovarud**.
-   Taastäitmise suhted on laole määratud. Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**. Vaadake vahekaardil **Koondplaneerimine** väljagruppi **Pealadu**.
-   Tellimuse vaiketüübiks on määratud Tootmine, Ostutellimus või Kanban. Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**. Valige kaup ja klõpsake siis valikuid **Plaan &gt; Tellimuse vaikesätted**. Vaadake vormi **Tellimuse vaikesätted** jaotist **Tellimuse vaiketüüp**.

![Nõue laoala varude laole kohustuslik.](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



## <a name="additional-resources"></a>Lisaressursid

- [Koondplaneerimine ja mitme tegevuskoha funktsiooni ülevaade](master-plan-multisite-functionality.md)
- [Laoala ja lao katmise koondplaanimine, ladu on kohustuslik](master-plan-site-warehouse-coverage-warehouse-mandatory.md)
- [Koondplaanimine laovarude puhul, kohustuslik ladu](master-plan-site-coverage-warehouse-mandatory.md)
- [Laoala ja lao katmise koondplaanimine, ladu ei ole kohustuslik](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)
- [Koosluse versiooni määratlemine](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]