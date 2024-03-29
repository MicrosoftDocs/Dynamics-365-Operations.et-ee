---
title: Eelarve plaanimise põhjendusdokumendid
description: Põhjendusdokumendid pakuvad eelarvetaotlejatele teatud eelarve vajalikkust põhjendavaid selgitusi.
author: panolte
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: kfend
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 03780b36cb3a6a609350c61792f0c98f2c08244d
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711767"
---
# <a name="budget-planning-justification-documents"></a>Eelarve plaanimise põhjendusdokumendid

[!include [banner](../includes/banner.md)]

Põhjendusdokumendid pakuvad eelarvetaotlejatele teatud eelarve vajalikkust põhjendavaid selgitusi. 

Eelarvehaldur loob Microsoft Wordis eelarveplaani malli ja määrab selle praegusse eelarve plaanimise protsessi. Seejärel saavad eelarve omanikud malli avada ja andmed Wordis automaatselt sisestada oma eelarvetaotluse põhjal. Pärast seda on võimalik lisada täiendavat teksti või andmeid ning seejärel isikupärastatud põhjendusdokument salvestada ja manustada eelarveplaanile.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Microsoft Dynamics Office’i lisandmooduli seadistamine Microsoft Wordi jaoks

1.  Avage uus Microsoft Wordi dokument.
2.  Klõpsake lindil valikut **Sisesta** ja siis valikut **Pood**.
3.  Otsige Microsoft Dynamics Office’i lisandmoodulit ja klõpsake nuppu **Lisa**.
4.  Klõpsake Wordi paremal paanil valikut **Lisa serveriteave**.
5.  Tippige või kleepige serveri URL ja klõpsake **OK**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Põhjenduse malli määratlemine Microsoft Wordis

1.  Klõpsake Microsoft Dynamics Office’i lisandmoodulis pärast sisselogimist nuppu **Kujundus**.
2.  Päiseteabe jaoks kasutage nuppu **Lisa välju**.
3.  Valige atribuudi BudgetPlanJustification üksuse andmeallikas ja klõpsake nuppu **Edasi**. **Märkus.** See üksus on nõutav kõigi põhjendusdokumentide puhul. Kasutada saab muid üksusi, kuid üleslaadimine tagasi Microsoft Dynamics 365 Finance'i ebaõnnestub, kui seda üksust ei kaasata.
4.  Lisage Wordi dokumenti atribuutide BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter ja DocumentNumber sildid ning väärtused. **Märkus.** Vajaduse korral saate standardsiltide asemel kasutada oma kohandatud silte.
5.  Päisejaotisega lõpetamiseks klõpsake nuppu **Valmis**.
6.  Eelarveplaani summade reatasemel üksikasjade saamiseks klõpsake valikut **Lisa tabel**.
7.  Valige jälle atribuudi BudgetPlanJustification üksuse andmeallikas ja klõpsake nuppu **Edasi**.
8.  Lisage väljad atribuutide EffectiveDate, ScenarioName, AccountDisplayValue ja AccountingCurrencyExpenseAmount jaoks. **Märkus.** Kui üksikutele eelarveplaani ridadele lisamiseks on kommentaarid saadaval, saab need siin tabelisse lisada.
9.  Lisage muud lõppkasutajale pakutavad lisajuhised ning tehke dokumendile vajalikud vormindus- ja laadimuudatused.
10. Enne jätkamist salvestage dokument kohalikku arvutisse ja sulgege fail.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Eelarve plaanimise protsessi seadistamine põhjendusmalli kasutamiseks

1.  Minge jaotisse **Eelarvestus** &gt; **Seadistus** &gt; **Eelarve plaanimine** &gt; **Põhjendusdokumendi mallid**.
2.  Klõpsake nuppu **Uus** ja sirvige vastloodud Microsoft Wordi dokumendini.
3.  Sisestage malli kuvatav nimi ja kirjeldus. Klõpsake **OK**.
4.  Minge jaotisse **Eelarvestus** &gt; **Seadistus** &gt; **Eelarve** **plaanimine** &gt; **Eelarve plaanimise protsess**.
5.  Valige protsess, kus malli tuleb kasutada, ja klõpsake nuppu **Redigeeri**.
6.  Valige väljal **Põhjendusdokumendi mall** sobiv mall ja salvestage.

##### <a name="edit-and-save-personalized-justification-documents"></a>Isikupärastatud põhjendusdokumentide redigeerimine ja salvestamine

1.  Looge uus eelarveplaan või avage olemasolev eelarveplaan.
2.  Valige ripploendist **Põhjendus** suvand **Uue põhjenduse loomine**.
3.  Pärast üksikasjade sisestamist valige rippmenüüst **Põhjendus** isikupärastatud dokumendi üleslaadimine.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
