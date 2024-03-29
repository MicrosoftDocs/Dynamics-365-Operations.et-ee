---
title: Koondplaanimine laoala ja laovarude jaoks, ladu on kohustuslik
description: See artikkel kirjeldab, kuidas planeeritakse laoala ja laoga kaupa laovarude dimensioonina. Lao dimensioon on kohustuslik.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adcb2d41ff70714b6bc9c28f3e23ce95f5292f2e
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740055"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a>Koondplaanimine laoala ja laovarude jaoks, ladu on kohustuslik

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas planeeritakse laoala ja laoga kaupa laovarude dimensioonina. Lao dimensioon on kohustuslik.

See koondplaneerimise stsenaarium sisaldab järgmisi tingimusi.

-   Laoala dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse.
-   Lao dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse.
-   Laoala ja lao dimensioonid seadistatakse laovarude plaanimiseks. Muidki dimensioone võib seadistada laovarude plaanimiseks. Mitme laoala režiimi funktsioonid neid siiski ei mõjuta.

Järgmine graafik näitab, kuidas koondplaneerimine jätkub. Parameetrid, mis on graafikusse kantud, ja nende asukohad, on järgnevad:
-   Ladu on seatud **Käsitsi** peale. Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**. Vaadake kiirkaardil **Koondplaneerimine** välja **Käsitsi**.
-   Kauba laovarud on kauba kohta määratud. Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**. Valige kaup ja seejärel klõpsake Toimingupaanil vahekaardil **Plaan** valikut **Kauba laovarud**.
-   Taastäitmise suhted on laole määratud. Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**. Vaadake kiirkaardil **Koondplaneerimine** väljagruppi **Pealadu**.
-   Tellimuse vaiketüübiks on määratud Tootmine, Ostutellimus või Kanban. Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**. Valige kaup ja seejärel klõpsake Toimingupaani vahekaardil **Plaan** valikut **Tellimuse vaikesätted**. Vaadake vormi **Tellimuse vaikesätted** jaotist **Tellimuse vaiketüüp**.

![Nõude laoala ja laovarud, ladu kohustuslik.](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



## <a name="additional-resources"></a>Lisaressursid

- [Koondplaneerimine ja mitme tegevuskoha funktsiooni ülevaade](master-plan-multisite-functionality.md)
- [Koondplaanimine laovarude puhul, kohustuslik ladu](master-plan-site-coverage-warehouse-mandatory.md)
- [Koondplaanimine laovarude puhul, ladu ei ole kohustuslik](master-plan-site-coverage-warehouse-not-mandatory.md)
- [Laoala ja lao katmise koondplaanimine, ladu ei ole kohustuslik](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)
- [Koosluse versiooni määratlemine](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]