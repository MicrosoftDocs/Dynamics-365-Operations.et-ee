---
title: Ülevaade lahknevuste lahendamisest arvete koondsummade võrdlemise ajal
description: Arve koondsummade võrdlemist saab kasutada tagamiseks, et arve koondsummad ei erineks eeldatavatest summadest rohkem kui lubatud hälbe võrra.
author: abruer
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4a20368385ec43547ee3d29770bd83cdec47e4a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189495"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching-overview"></a>Ülevaade lahknevuste lahendamisest arvete koondsummade võrdlemise ajal

[!include [banner](../includes/banner.md)]

Arvete võrdlemise kinnitamise üks tüüp on arvete kogusummade võrdlemine. Selleks, et määrata, et süsteem peaks arvete kogusummasid võrdlema, määrake lehe **Ostureskontro parameetrid** vahekaardil **Arve kinnitamine** suvandi **Arvesummade võrdlemine** väärtuseks **Jah**. 

Arve koondsummade vastavusseviimist saab kasutada tagamiseks, et arve koondsummad ei erineks eeldatavatest summadest rohkem kui lubatud hälbe võrra. Lehel **Arve kogusummade vastendamise üksikasjad** võrreldakse kuute kogusummat. Kui mõni kogusumma erineb oodatud vastavast ostutellimuse kogusummast, märgitakse võrdluslahknevus. 

Kogusummade võrdluslahknevusega arve ülevaatamiseks klõpsake tööruumis **Hankija arved** paanil **Ootel arved**. Seejärel klõpsake toimingupaani vahekaardil **Ülevaade** suvandit **Vastanduvad üksikasjad**. Kui tuvastatakse võrdluslahknevus, ilmuvad arve summa juurde hoistusikoonid. Saate kogusummade kohta üksikasju vaadata, vaadates arve kogusummade võrdlemise üksikasju. 

Pärast lahknevuse tuvastamist peate vajaduse korral võtma ühendust hankijaga, kui arvate, et arvel olev teave pole täpne. Olenevalt tulemuseks olevast kokkuleppest hankijaga saate teha ühe järgnevatest toimingutest.

-   Aktsepteerima hinnaerinevust ja sisestama arve, millel on vastenduste lahknevus. Süsteem võib olla seadistatud teilt kinnitust küsima, enne kui saab sisestada, kas võrdluslahknevusi on. Sel juhul peate kinnitama võrdluslahknevuse ja saate valikuliselt sisestada kinnituse kommentaari. Seejärel saate valida, kas soovite arve sisestada.
-   Tegema arve summa ümber eeldatavale summale ja sisestama arve.
-   Taotlema hankijalt täiskrediiti ja uut parandatud arvet.

Lisateabe saamiseks vt [Erandite uurimine või lahendamine](tasks/research-resolve-exceptions.md).


