---
title: Eelarve plaanimise andmete eraldamine
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Finance'is saadaolevaid eraldamismeetodeid ja nende kasutamist.
author: ShylaThompson
manager: AnnBe
ms.date: 03/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ceddeda5760d961568d58e7e4805955ea972c586
ms.sourcegitcommit: 8fad5a8c7ea5d0d0037669e61e2313f684bcae23
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/06/2020
ms.locfileid: "3106878"
---
# <a name="budget-planning-data-allocation"></a>Eelarve plaanimise andmete eraldamine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse Microsoft Dynamics 365 Finance'is saadaolevaid eraldamismeetodeid ja nende kasutamist.  

Saate prognoositud summade täpseks kujutamiseks eelarveplaani andmeid jaotada mitmel viisil.

## <a name="allocation-methods"></a>Eraldamismeetodid
Kolm eraldamismeetodit (Eralda perioodide lõikes, Eralda dimensioonidele ja Kasuta pearaamatu eraldamisreegleid) saavad luua eelarveplaani read, mis põhinevad sama eelarveplaani ridadel. Kolm teist meetodit (Koonda, Jaota ja Kopeeri eelarveplaanist) saavad luua eelarveplaani read muudest eelarveplaanidest. Kõigi kuue eraldamismeetodi puhul määrate teie sihtstsenaariumi. Sihtstsenaarium võib olla lähtestsenaariumiga sama või sellest erineda. Lisaks saate määrata, kas uued read lisatakse eelarveplaani või asendavad eelarveplaani praegused read.

> [!NOTE] 
> Kordumatut stsenaariumi tuleb kasutada summeerimiseks, mis erineb stsenaariumist, mida kasutati jaotuse või muude muudatuste puhul, mis tehti varem emaplaanis.  

[![Eraldusmeetod Eralda perioodide lõikes](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Eralda perioodide lõikes** – perioodi eralduskategooria abil eraldatakse eelarveplaani read lähtealuse eelarveplaani stsenaariumist perioodi vahel sihtstsenaariumis. Algsumma määratakse sihtstsenaariumis mitmele reale perioodi eraldamiskategoorias määratletud protsendi ja kuupäeva põhjal.         

[![Eraldusmeetod Dimensioonidele eraldamine](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Dimensioonidele eraldamine** – eelarveplaani read jaotatakse lähte-eelarve planeerimise stsenaariumi järgi ühele või mitmele sihtstsenaariumi reale, lähtudes protsentidest ja rahalistest mõõtmetest, mis on määratletud valitud eelarvejaotuse tähtaja jooksul.           

![Liitväärtuse diagramm](./media/aggregatechart-300x230.png)
**Liitväärtus** – eelarveplaani read liidetakse seostatud (alam) eelarveplaanides oleva lähte-eelarveplaani stsenaariumist vanema eelarveplaani sihtstsenaariumini. See meetod võimaldab eelarvesummad, mis valmistatakse ette organisatsiooni madalamal tasemel kõrgemal tasemel konsolideerimiseks.          

[![Jaotusdiagramm](./media/distributechart-300x230.png)](./media/distributechart.png)
**Jaotus** – eelarveplaani read jaotatakse lähte-eelarve planeerimise stsenaariumist vanema eelarveplaanis sihtstsenaariumi juurde seotud (alam) eelarveplaanides, lähtudes seotud plaanide organisatsiooniüksuste rahalistest mõõtmetest. See meetod võimaldab eelarvesummad, mis valmistatakse ette organisatsiooni kõrgemal tasemel veelgi lokaliseeritumaks ülevaatamiseks levitamiseks.           

[![Pearaamatu eraldusreeglid](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Kasuta pearaamatu eraldusreegleid** – eelarveplaani read jaotatakse lähte-eelarve plaanimise stsenaariumist sihtstsenaariumi järgi valitud pearaamatu eraldamise reegli alusel. 

[![Kopeeri eelarveplaanist](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Kopeeri eelarveplaanist** – nagu jaotamise eraldusmeetodi puhul, luuakse sihtpunkti eelarveplaani read, mis põhinevad seotud eelarveplaani ridadel. Selle meetodi puhul ei pea algne eelarveplaan olema emaplaan, vaid võib olla eelarveplaani hierarhias mis tahes kõrgemal tasemel. See eraldamismeetod on kasulik, kui konsolideeritud summasid eelarvestatakse algselt palju kõrgemal tasemel ning tuleb enne kõrgema taseme kinnituse saamist viia üksikasjalikuks läbivaatamiseks ja korrigeerimiseks organisatsiooni madalamale tasemele.          

## <a name="using-allocation-methods-in-a-budget-plan"></a>Eraldamismeetodite kasutamine eelarveplaanis
Eelarveplaani lehel eraldamiseks valige eraldatavad read ja seejärel klõpsake suvandit **Eralda eelarve**.

[![Nupp Eralda eelarve](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png) 

Seejärel valige eraldamismeetod. Seejärel määratakse ülejäänud väljad teie valitud meetodi alusel. Need väljad hõlmavad eelarveplaani andmete allikat ja sihtkohta ning suvandit, mis võimaldab teil korrutada allika määratud teguriga hulgikorrigeerimise lihtsustamiseks sihtsummade loomisel. Saate määrata ka suvandi **Lisa plaani**. Valige olemasoleva eelarveplaani ridade asendamiseks **Ei** või valige **Jah** olemasoleva eelarveplaani ridade säilitamiseks ja uute ridade lisamiseks eraldatud summade puhul.

## <a name="automating-allocations-during-a-workflow"></a>Eraldamiste automatiseerimine töövoos
Üks võimas funktsioon lubab eelarve plaanimise töövoo osana eraldada automaatselt. Eelarveplaani liikumisel läbi selle töövoo saavad automatiseeritud ülesanded tugineda eraldamisele määratud eelarve plaanimise etapis. 

Automaatse eraldamise seadistamiseks peate esmalt looma eraldamisgraafiku lehel **Eelarve plaanimise konfiguratsioon**. Eraldamisgraafik määratleb automaatse eraldamise käitamisel kasutatava eraldamismeetodi ja eri eraldamissuvandite väärtused (vt kirjeldusi eelmistest jaotistest). 

Seejärel loote etapi eraldamise lehel **Eelarve plaanimise konfiguratsioon**. Etapi eraldamine määrab eraldamisgraafiku eelarve plaanimise töövoogu ja etappi. 

Lõpuks lisate eelarve plaanimise etapi eraldamise automatiseeritud ülesande soovitud töövooetapis. Järgmises näites on töövoogu lisatud kaks eelarve plaanimise etapi eraldamist (punasega esile tõstetud).

[![Eelarve plaanimise etapi eraldamised](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)



