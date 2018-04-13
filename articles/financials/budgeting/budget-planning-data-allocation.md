---
title: Eelarve plaanimise andmete eraldamine
description: Selles artiklis kirjeldatakse erinevaid rakenduses Microsoft Dynamics 365 for Finance and Operations saadaolevaid eraldamismeetodeid ja kuidas neid kasutada.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: b5f262318b4defb941f1216d0bfe06961f62bad4
ms.contentlocale: et-ee
ms.lasthandoff: 03/26/2018

---

# <a name="budget-planning-data-allocation"></a>Eelarve plaanimise andmete eraldamine

[!INCLUDE [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse erinevaid rakenduses Microsoft Dynamics 365 for Finance and Operations saadaolevaid eraldamismeetodeid ja kuidas neid kasutada.  

Saate prognoositud summade täpseks kujutamiseks eelarveplaani andmeid jaotada mitmel viisil.

## <a name="allocation-methods"></a>Eraldamismeetodid
Kolm eraldamismeetodit (Eralda perioodide lõikes, Eralda dimensioonidele ja Kasuta pearaamatu eraldamisreegleid) saavad luua eelarveplaani read, mis põhinevad sama eelarveplaani ridadel. Kolm teist meetodit (Koonda, Jaota ja Kopeeri eelarveplaanist) saavad luua eelarveplaani read muudest eelarveplaanidest. Kõigi kuue eraldamismeetodi puhul määrate teie sihtstsenaariumi. Sihtstsenaarium võib olla lähtestsenaariumiga sama või sellest erineda. Lisaks saate määrata, kas uued read lisatakse eelarveplaani või asendavad eelarveplaani praegused read.

[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Eralda perioodide lõikes** – perioodi eraldamiskategooriat kasutatakse eelarveplaani ridade eraldamiseks algsest eelarveplaani stsenaariumist sihtstsenaariumi perioodide lõikes. Algsumma määratakse sihtstsenaariumis mitmele reale perioodi eraldamiskategoorias määratletud protsendi ja kuupäeva põhjal.         

[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Eralda dimensioonidele** – eelarveplaani read eraldatakse algsest eelarve plaanimise stsenaariumist sihtstsenaariumi ühele või enamale reale valitud eelarve eraldustingimuses määratletud protsentide ja finantsdimensioonide põhjal.           

![AggregateChart](./media/aggregatechart-300x230.png)
**Koonda** – eelarveplaani read koondatakse seostatud (tütar-) eelarveplaanide algsest eelarveplaani stsenaariumist eelarve emaplaani sihtstsenaariumisse. See meetod võimaldab eelarvesummad, mis valmistatakse ette organisatsiooni madalamal tasemel kõrgemal tasemel konsolideerimiseks.          

[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Jaota** – eelarveplaani read jaotatakse eelarve emaplaani algsest eelarve plaanimise stsenaariumist seostatud (tütar-) eelarveplaanide sihtstsenaariumisse seotud plaanide organisatsiooniüksuste finantsdimensioonide põhjal. See meetod võimaldab eelarvesummad, mis valmistatakse ette organisatsiooni kõrgemal tasemel veelgi lokaliseeritumaks ülevaatamiseks levitamiseks.           

[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Kasuta pearaamatu eraldamisreegleid** – eelarveplaani read jaotatakse algse eelarve plaanimise stsenaariumist sihtstsenaariumisse valitud pearaamatu eraldamisreegli põhjal. 

[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Kopeeri eelarveplaanist** – nagu eraldamismeetodi jaotamise puhul, luuakse eelarveplaani read sihtkohas seotud eelarveplaani ridade põhjal. Selle meetodi puhul ei pea algne eelarveplaan olema emaplaan, vaid võib olla eelarveplaani hierarhias mis tahes kõrgemal tasemel. See eraldamismeetod on kasulik, kui konsolideeritud summasid eelarvestatakse algselt palju kõrgemal tasemel ning tuleb enne kõrgema taseme kinnituse saamist viia üksikasjalikuks läbivaatamiseks ja korrigeerimiseks organisatsiooni madalamale tasemele.          

## <a name="using-allocation-methods-in-a-budget-plan"></a>Eraldamismeetodite kasutamine eelarveplaanis
Eelarveplaani lehel eraldamiseks valige eraldatavad read ja seejärel klõpsake suvandit **Eralda eelarve**.

[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png) 

Seejärel valige eraldamismeetod. Seejärel määratakse ülejäänud väljad teie valitud meetodi alusel. Need väljad hõlmavad eelarveplaani andmete allikat ja sihtkohta ning suvandit, mis võimaldab teil korrutada allika määratud teguriga hulgikorrigeerimise lihtsustamiseks sihtsummade loomisel. Saate määrata ka suvandi **Lisa plaani**. Valige olemasoleva eelarveplaani ridade asendamiseks **Ei** või valige **Jah** olemasoleva eelarveplaani ridade säilitamiseks ja uute ridade lisamiseks eraldatud summade puhul.

## <a name="automating-allocations-during-a-workflow"></a>Eraldamiste automatiseerimine töövoos
Üks võimas funktsioon lubab eelarve plaanimise töövoo osana eraldada automaatselt. Eelarveplaani liikumisel läbi selle töövoo saavad automatiseeritud ülesanded tugineda eraldamisele määratud eelarve plaanimise etapis. 

Automaatse eraldamise seadistamiseks peate esmalt looma eraldamisgraafiku lehel **Eelarve plaanimise konfiguratsioon**. Eraldamisgraafik määratleb automaatse eraldamise käitamisel kasutatava eraldamismeetodi ja eri eraldamissuvandite väärtused (vt kirjeldusi eelmistest jaotistest). 

Seejärel loote etapi eraldamise lehel **Eelarve plaanimise konfiguratsioon**. Etapi eraldamine määrab eraldamisgraafiku eelarve plaanimise töövoogu ja etappi. 

Lõpuks lisate eelarve plaanimise etapi eraldamise automatiseeritud ülesande soovitud töövooetapis. Järgmises näites on töövoogu lisatud kaks eelarve plaanimise etapi eraldamist (punasega esile tõstetud).

[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)




