---
title: Eelarve planeerimise Exceli Mallid
description: Selles teemas kirjeldatakse, kuidas luua Microsoft Exceli malle, mida saab kasutada koos eelarve.
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

# <a name="budget-planning-templates-for-excel"></a>Eelarve planeerimise Exceli Mallid

Selles teemas kirjeldatakse, kuidas luua Microsoft Exceli malle, mida saab kasutada koos eelarve.

See teema näitab, kuidas luua Exceli Mallid, mida kasutatakse eelarve plaane standard demo andmekogumi ja Admin kasutaja kasutajanimi. Eelarve planeerimise kohta lisateabe saamiseks vaadake [eelarve ülevaade.](budget-planning-overview-configuration.md) Samuti saate jälgida selle [eelarve planeerimise 101](budget-plan.md) juhendaja õppida põhi mooduli konfiguratsiooni ja kasutamise põhimõtted.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Loo töölehe abil eelarve kava dokumendi paigutus
Eelarve kava dokumente saab vaadata ja üks või mitu paigutust abil redigeerida. Iga paigutus võib olla seotud eelarve kava dokumendi mall, vaadata ja redigeerida eelarve kava andmed Exceli töölehel. Selle teema dokumendimall eelarve plaan loob paigutus olemasoleva konfiguratsiooni abil. Avatud on **eelarvekavad lisanud** (**eelarve koostamise**&gt;**eelarve**). Klõpsake **uus** uus eelarve kava dokumendi loomiseks. [![bpt1](./media/bpt11-1024x552.png)](./media/bpt11.png) 

Kasutamine ning **lisa** line võimalus lisada read. Klõpsake **paigutusega** saate vaadata eelarve kava dokumendi paigutus konfiguratsiooni. 
[![bpt2](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Saate vaadata paigutuse konfiguratsioon ja kohandada seda vastavalt vajadusele. Mine **malli**&gt;**Loo** luua Exceli faili selle paigutus. Pärast malli loomist, minge **malli**&gt;**View** avada ja vaadata dokumendimall eelarve plaan. Exceli faili saate salvestada oma kõvakettale. [![bpt3](./media/bpt3-1024x545.png)](./media/bpt3.png) 

> [!NOTE] 
> Eelarve kava dokumendi paigutust ei saa redigeerida pärast Exceli malli on sellega seotud. Paigutuse muutmiseks seotud Exceli malli faili kustutada ja uueneda see. See on vajalik hoida väljade paigutuse ja töölehe sünkroonitud. 

Exceli mall sisaldab kõiki elemente alates eelarve kava dokumendi paigutuse, kus on **saadaval töölehel** veerus True. Exceli mall tohivad kattuvaid elemente. Näiteks kui paigutus taotluse Q1, taotluse Q2, Q3 taotluse ja taotluse Q4 veerud ja kokku taotluse veeru, mis esindab kõigi 4 kvartali veergude summa, kvartali veergude või veerg on kasutada Exceli malli. Exceli faili ei saa kattuvate veergude värskendamise ajal värskendada, kuna tabeli andmed võiks olla vananenud ja ebatäpsed.

[![bpt4](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> Võimalike probleemide vaatamiseks ja redigeerimiseks Excelis eelarve andmete vältimiseks tuleks nii Dynamics 365 sama kasutaja logitakse ja andmeliidese Microsoft Dynamics Office Add-in.

## <a name="add-a-header-to-budget-plan-document-template"></a>Päise lisamiseks eelarve kava dokumendimall
Päise teabe lisamiseks valige kõige ülemine rida Exceli faili ja lisada tühi rida. Klõpsake **disain** ja selle **andmeliidese** Exceli faili päis väljade lisamiseks.

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

Aastal ning **disain** jaotises ** ** klõpsake **lisa** väljad ja valige seejärel **BudgetPlanHeader** üksus andmeallika.

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

Kursoriga soovitud asukohta Exceli faili. Klõpsake **lisa silt** välja sildi lisamiseks valitud asukohta. Valige **lisa** välja väärtuse lisamiseks valitud koht. Klõpsake **teha** sulgeda kujundaja.

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![bpt7](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Arvutatud veeru lisamiseks tabeli eelarve kava dokumendi mall
--------------------------------------------------------------

Loodud eelarve kava dokumendimalli lisatakse järgmine, arvutatud veerud. A **kokku taotluse** veeru, mis võtab kokku taotluse Q1: taotluse Q4 veerud, ja on **kohandamine** veerg, mis arvutab ümber ning **kokku taotluse** veeru eelmääratletud teguriga.

Klõpsake **disain** ja selle **andmeliidese** veergude lisamiseks tabel. Klõpsake **muuta** kõrval **BudgetPlanWorksheet** andmeallika veergude lisamise alustamiseks.

[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Valitud väljarühma kuvatakse veerud, mis on saadaval malli. Klõpsake **valem** lisada uue veeru. Uue veeru nimi ja seejärel kleepige arvesse valem on **valem** välja. Klõpsake **Update** veeru lisamiseks.

[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> Määratlege valem, valemi koostada tabeli ja seejärel kopeerida selle **disain** akna. Dynamics 365 toimingute seotud tabeli tavaliselt on nimi "AXTable1". Näiteks kokkuvõttes taotleda Q1: taotleda Q4 veerge arvutustabelis, valem = AxTable1\[taotleda Q1\]+ AxTable1\[taotleda Q2\]+ AxTable1\[taotleda Q3\]+ AxTable1\[taotleda Q4\].

Korrake neid samme, et lisada selle **kohandamine** veeru. Kasutage valemit = AxTable1\[kokku taotluse\]\*$$ 1 selle veeru I. See võtab väärtus lahtris I1 ja väärtusi korrutada ning **kokku taotluse** veeru arvutamiseks korrigeerimise summad.

Salvestage ja sulgege Excel faili. Tagasi Dynamics 365 toimingute jaoks ning **paigutusega**, klõpsake **malli &gt;laadida** laadida salvestatud Exceli malli kasutatakse eelarve kava. 

[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Tihe ning **paigutusega** liugurit. Aastal **eelarve kava** dokument, klõpsake **töölehe** vaadata ja redigeerida Exceli dokument. Pange tähele, et selle eelarve kava töölehe loomiseks kasutatud kohandatud Exceli mall ja arvutatud veergude uuendatakse valemid, mis määratleti eelmise sammu. 

[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Tips & tricks jaoks eelarve kava mallide loomine
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Saate lisada ja kasutada täiendavatele andmeallikatele eelarve kava malli?

Jah, saab kasutada ka **disain** menüü täiendavate üksuste lisamiseks sama või muudel lehtedel Exceli malli. Näiteks saate lisada ka **BudgetPlanProposedProject** andmeallika saate luua ja hallata projektide loetelu samal ajal, millal töötamine eelarve kava Exceli. Pange tähele, et andmete allikad sh võib mõjutada jõudlust Exceli töövihiku. 

Kasutage selle **Filter** failis on **andmeliidese** soovitud filtrid lisamiseks täiendavatele andmeallikatele.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Peita teiste kasutajate andmeliidese suvandi kujundus?

Jah, avada selle **andmeliidese** suvandite peitmiseks on **disain** võimalus teistelt kasutajatelt.

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

Laiendada **konnektori suvandid** ja selge on **lubade kasutada disaini programmi** ruut. See varjata ning **disain** valik selle **andmeliidese**.

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Saate takistada kasutajatel kogemata sulgemine andmeliidese kasutades andmeid?

Soovitame malli, et kasutajad sulgemist puldiga. Lukk, klõpsake selle **andmeliidese**, üleval paremas nurgas kuvatakse nool. 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Noolekestele Peamenüü. Valige **lukk**.

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Kasutada muud Exceli funktsioonid, nagu rakendatavat, värvid, tingimusvormingut ja diagrammid minu eelarve kava malle?

Jah, enamik standard Exceli funktsioonid töötavad eelarve kava Mallid. Soovitame kasutada värvikoodid kasutajatele kirjutuskaitstud ja redigeeritavad veergude eristamiseks. Tingimusvormingu saab rõhutada eelarve piirkondadesse. Veergude summade saab esitada lihtsalt standard Exceli valemite tabeli abil.

Saate luua ja kasutada pivot tabelite ja diagrammide täiendavaid ühendustele ning eelarve andmete visualiseeringuid. Kohta ning **andmeid** vahekaardil, on **ühendused** nuppu **Värskenda kõik**, ja seejärel klõpsake **ühenduse atribuudid**. Klõpsake selle **kasutamise** vahekaart. All **värskendada**, valige selle **Värskenda andmed faili avamisel** ruut. 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)


