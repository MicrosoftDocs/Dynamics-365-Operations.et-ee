---
title: Koondplaanimine laoala ja laovarude jaoks, ladu ei ole kohustuslik
description: See artikkel kirjeldab, kuidas planeeritakse laoala ja laoga kaupa laovarude dimensioonina. Lao dimensioon ei ole kohustuslik.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4989a05f4647ac836b78692da7f63396dbef788
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741008"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a>Koondplaanimine laoala ja laovarude jaoks, ladu ei ole kohustuslik

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas planeeritakse laoala ja laoga kaupa laovarude dimensioonina. Lao dimensioon ei ole kohustuslik.

See koondplaneerimise stsenaarium sisaldab järgmisi tingimusi.

-   Laoala dimensioon on seadistatud kohustuslikuks ja see tuleb sisestada nõudluse kandesse. Seda sätet ei saa muuta.
-   Lao dimensioon ei ole seatud kohustuslikuks. Ladu võib olla teada, kuid seda ei kasutata koondplaneerimise arvutamisel.
-   Laoala ja lao dimensioonid seadistatakse laovarude plaanimiseks. Muidki dimensioone võib seadistada laovarude plaanimiseks. Mitme laoala režiimi funktsioonid neid siiski ei mõjuta.

Järgmine graafik näitab, kuidas koondplaneerimine jätkub. Parameetrid, mis on graafikusse kantud, ja nende asukohad, on järgnevad:
-   Ladu on seatud Käsitsi peale. Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**. Vaadake kiirkaardil **Koondplaneerimine** välja **Käsitsi**.
-   Kauba laovarud on kauba kohta määratud. Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**. Valige kaup ja seejärel klõpsake Toimingupaanil vahekaardil **Plaan** valikut **Kauba laovarud**.
-   Taastäitmise suhted on laole määratud. Klõpsake valikuid **Varud &gt; Seadistus &gt; Laovarude jaotamine &gt; Laod**. Vaadake kiirkaardil **Koondplaneerimine** väljagruppi **Pealadu**.
-   Tellimuse vaiketüübiks on määratud Tootmine, Ostutellimus või Kanban. Klõpsake suvandeid **Tooteteabe haldus &gt; Tooted &gt; Väljastatud tooted**. Valige kaup ja seejärel klõpsake Toimingupaani vahekaardil **Plaan** valikut **Tellimuse vaikesätted**. Vaadake vormi **Tellimuse vaikesätted** jaotist **Tellimuse vaiketüüp**.

![Nõude laoala ja laovarud, ladu pole.](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



## <a name="additional-resources"></a>Lisaressursid

- [Koondplaneerimine ja mitme tegevuskoha funktsiooni ülevaade](master-plan-multisite-functionality.md)
- [Koondplaanimine laovarude puhul, kohustuslik ladu](master-plan-site-warehouse-coverage-warehouse-mandatory.md)
- [Laoala ja lao katmise koondplaanimine, ladu on kohustuslik](master-plan-site-coverage-warehouse-mandatory.md)
- [Laoala ja lao katmise koondplaanimine, ladu ei ole kohustuslik](master-plan-site-coverage-warehouse-not-mandatory.md)
- [Koosluse versiooni määratlemine](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]