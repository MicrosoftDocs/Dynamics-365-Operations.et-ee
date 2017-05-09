---
title: Eelarve plaanimise mallid Excelile
description: See teema kirjeldab, kuidas luua Microsoft Exceli malle, mida saab kasutada eelarveplaanidega.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 0e2eb6e7c130f03edbf60a185d397d94b5d61d7d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-templates-for-excel"></a>Eelarve plaanimise mallid Excelile

[!include[banner](../includes/banner.md)]


See teema kirjeldab, kuidas luua Microsoft Exceli malle, mida saab kasutada eelarveplaanidega.

Teema näitab, kuidas luua Exceli malle, mida kasutatakse eelarveplaanidega, kasutades standardset demoandmekogumit ja administraatori identimisteavet. Lisateavet eelarve plaanimise kohta vt teemast [Eelarve plaanimise ülevaade.](budget-planning-overview-configuration.md) Saate vaadata ka õppetükki [Eelarve plaanimine 101](budget-plan.md), et tutvuda baasmooduli konfigureerimise ja kasutuspõhimõtetega.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Töölehe loomine eelarveplaani dokumendi paigutusega
Eelarveplaani dokumente saab vaadata ja redigeerida üht või mitut paigutust kasutades. Igal paigutusel võib olla seostatud eelarveplaani dokumendimall, et saaksite eelarveplaani andmeid vaadata ja redigeerida Exceli töölehel. Selles teemas luuakse eelarveplaani dokumendimall olemasolevat paigutuse konfiguratsiooni kasutades. Avage **Eelarveplaanide loend** (**Eelarvestus**&gt; **Eelarveplaanid**). Klõpsake uue eelarveplaani dokumendi loomiseks valikut **Uus**. [![bpt1](./media/bpt11-1024x552.png)](./media/bpt11.png) 

Ridade lisamiseks kasutage valikut **Lisa** rida. Eelarveplaani dokumendi paigutuse konfiguratsiooni kuvamiseks klõpsake valikut **Paigutused**. 
[![bpt2](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Saate paigutuse konfiguratsiooni üle vaadata ja seda vajaduse korral korrigeerida. Selle paigutuse jaoks Exceli faili loomiseks minge jaotisse **Mall** &gt; **Loo**. Kui mall on loodud, minge jaotisse **Mall** &gt; **Kuva**, et eelarveplaani dokumendimall avada ja üle vaadata. Saate Exceli faili salvestada kohalikule kettale. [![bpt3](./media/bpt3-1024x545.png)](./media/bpt3.png) 

> [!NOTE] 
> Eelarveplaani dokumendi paigutust ei saa enam redigeerida, kui Exceli mall on sellega seostatud. Paigutuse muutmiseks kustutage seostatud Exceli malli fail ja looge see uuesti. See on vajalik selleks, et hoida paigutuse ja töölehe väljad sünkroonis. 

Exceli mall sisaldab kõiki eelarveplaani dokumendi paigutuse elemente, kui veeru **Saadaval töölehel** sätteks on valitud Tõene. Exceli mallis pole elementide kattumine lubatud. Näiteks kui paigutus sisaldab veerge Taotlus Q1, Taotlus Q2, Taotlus Q3 ja Taotlus Q4 ning taotluste koondveergu, mis kujutab kõigi neljandikveergude summat, saab Exceli mallis kasutada ainult neljandikveerge või koondveergu. Exceli fail ei saa kattuvaid veerge värskendamise ajal värskendada, kuna tabelis olevad andmed muutuvad ajakohatuks ja ebatäpseks.

[![bpt4](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> Exceliga eelarveplaani andmete vaatamisel ja redigeerimisel võimalike probleemide vältimiseks peab sama kasutaja olema sisse loginud nii Dynamics 365 for Operationsisse kui ka Microsoft Dynamics Office’i lisandmooduli andmekonnektorisse.

## <a name="add-a-header-to-budget-plan-document-template"></a>Eelarveplaani dokumendimallile päise lisamine
Päiseteabe lisamiseks valige Exceli failis ülemine rida ja sisestage tühjad read. Exceli failile päiseväljade lisamiseks klõpsake rakenduses **Andmekonnektor** valikut **Kujundus**.

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

Klõpsake vahekaardil **Kujundus**** **välju **Lisa** ja valige üksuse andmeallikaks **BudgetPlanHeader**.

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

Viige kursor Exceli failis soovitud kohta. Valitud asukohta väljasildi lisamiseks klõpsake valikut **Lisa silt**. Valitud kohta väärtusevälja lisamiseks klõpsake valikut **Lisa väärtus**. Kujundaja sulgemiseks klõpsake valikut **Valmis**.

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![bpt7](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Eelarveplaani dokumendimalli tabelisse arvutatud veeru lisamine
--------------------------------------------------------------

Seejärel lisatakse arvutatud veerud loodud eelarveplaani dokumendimallile. Veerg **Koondtaotlus**, mis koondab veerud Taotlus Q1 : Taotlus Q4, ja veerg **Korrigeerimine**, mis arvutab veeru **Koondtaotlus** eelmääratletud teguri alusel ümber.

Tabelile veergude lisamiseks klõpsake rakenduses **Andmekonnektor** valikut **Kujundus**. Veergude lisamise alustamiseks klõpsake andmeallika **BudgetPlanWorksheet** kõrval olevat valikut **Redigeeri**.

[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Valitud väljagrupis kuvatakse mallis saadaolevad veerud. Uue veeru lisamiseks klõpsake valikut **Valem**. Andke uuele veerule nimi ja kleepige valem väljale **Valem**. Veeru sisestamiseks klõpsake valikut **Värskenda**.

[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> Valemi määratlemiseks looge valem arvutustabelis ja kopeerige see aknasse **Kujundus**. Dynamics 365 for Operationsiga seotud tabelile antakse tavaliselt nimi AXTable1. Näiteks veergude Taotlus Q1 : Taotlus Q4 columns summeerimiseks arvutustabelis saate kasutada valemit AxTable1\[Taotlus Q1\]+AxTable1\[Taotlus Q2\]+AxTable1\[Taotlus Q3\]+AxTable1\[Taotlus Q4\].

Korrake neid etappe veeru **Korrigeerimine** lisamiseks. Kasutage selle veeru puhul valemit AxTable1\[Koondtaotlus\]\*$I$1. See võtab väärtuse lahtrist I1 ja korrutab väärtustega veerus **Koondtaotlus**, et arvutada korrigeerimise summad.

Salvestage ja sulgege Exceli fail. Naaske Dynamics 365 for Operationsisse ja klõpsake aknas **Paigutused** valikuid **Mall &gt; Üleslaadimine**, et laadida eelarveplaani jaoks kasutatav salvestatud Exceli mall üles. 

[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Sulgege liugaken **Paigutused**. Dokumendi kuvamiseks ja redigeerimiseks Excelis klõpsake **Eelarveplaani** dokumendis valikut **Tööleht**. Pange tähele, et selle eelarveplaani töölehe loomiseks kasutati korrigeeritud Exceli malli ja arvutatud veerge värskendatakse valemitega, mille määratlesite eelmistes etappides. 

[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Näpunäited ja vihjed eelarveplaani mallide loomiseks
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Kas eelarveplaani mallile saab lisada ka täiendavaid andmeallikaid ja neid kasutada?

Jah, saate samale või teistele Exceli malli lehtedele lisada lisaüksusi, kasutades menüüd **Kujundus**. Näiteks saate lisada andmeallika **BudgetPlanProposedProject**, et luua ja hallata pakutavate projektide loendit, töötades samal ajal Excelis eelarveplaani andmetega. Pange tähele, et suuremahuliste andmeallikate lisamine võib mõjutada Exceli töövihiku jõudlust. 

Täiendavatele andmeallikatele saate lisada soovitud filtreid, kasutades rakenduse **Andmekonnektor** valikut **Filter**.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Kas Andmekonnektori valikut Kujundus saab teiste kasutajate eest peita?

Jah, valiku **Kujundus** peitmiseks avage **Andmekonnektori** suvandid.

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

Laiendage jaotist **Andmekonnektori suvandid** ja tühjendage ruut **Luba kujundus**. See peidab valiku **Kujundus** rakendusest **Andmekonnektor**.

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Kas Andmekonnektori kogemata sulgemist andmetega töötamise ajal saab takistada?

Soovitame malli lukustada, et kasutajad ei saaks seda sulgeda. Lukustamiseks klõpsake valikut **Andmekonnektor**. Paremas ülanurgas kuvatakse ikoon. 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Klõpsake lisamenüü avamiseks noolt. Valige **Lukusta**.

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Kas eelarveplaani mallidega saab kasutada ka muid Exceli funktsioone, nagu lahtrite vormindamine, värvid, tingimusvorming ja diagrammid?

Jah, eelarveplaani mallidega töötab enamik Exceli standardvõimalusi. Soovitame kasutada värvitähistusi, et kasutajad saaksid eristada kirjutuskaitstud ja redigeeritavaid veerge. Tingimusvormingut kasutades saab esile tõsta eelarve probleemsed osad. Veergude kogusummasid saab hõlpsasti esitada Exceli standardsete valemitega, mille leiate tabeli kohalt.

Samuti saate eelarveandmete täiendavaks grupeerimiseks ja visualiseerimiseks luua ning kasutada ka liigendtabeleid ja diagramme. Klõpsake vahekaardil **Andmed** grupis **Ühendused** valikut **Värskenda kõik** ja seejärel valikut **Ühenduse atribuudid**. Klõpsake vahekaarti **Kasutus**. Märkige jaotises **Värskendamine** ruut **Värskenda andmeid faili avamisel**. 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)



