---
title: Pearaamatupidaja tööruumile finantsdimensioonide lisamine
description: Selles teemas selgitatakse, kuidas lisada pearaamatupidaja tööruumi finantsdimensioonid, et neid saaks kasutada pearaamatu ja eelarvearuannetes.
author: aprilolson
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: b42fc4f0e299dc785ef465efc54286effccfb92b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823832"
---
# <a name="add-financial-dimensions-to-the-cfo-workspace"></a>Pearaamatupidaja tööruumile finantsdimensioonide lisamine

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas lisada pearaamatupidaja tööruumi finantsdimensioone, et neid saaks kasutada pearaamatu- ja eelarvearuannetes. Pearaamatupidaja tööruumis on vahekaart **Ülevaade** ja vahekaart **Finants**. Nendel vahekaartidel kuvatavad aruanded põhinevad kahel mõõdikul: LedgerActivityMeasure ja BudgetActivityMeasure. Nende mõõtude ja üksuse DimensionCombinationEntity vahel on seos. Seega saate valida dimensioonid.

1. Uuendage lehel **Üksuse pood** mõõdikud **LedgerActivityMeasure** ja **BudgetActivityMeasure**.
2. Avage rakenduses Microsoft Visual Studio rakenduste sirvija ja otsige rakendust **LedgerCFO**.
3. Jaotises **Ressursid** avage rakendus **LedgerCFOWorkspacePBIX**.
4. Kui ressurss avaneb Microsoft Power BI desktop, siis valige käsk **Too andmed**, seejärel valige suvand **SQL serveri andmebaas** ja seejärel suvand **Ühenda**.
5. Sisestage serveri nimi ja seejärel sisestage andmebaasi väljale **AxDW**. Valige käsk **DirectQuery** ja seejärel valige käsk **OK**.
6. Otsige ja valige tulemiloendist **LedgerActivityMeasure\_DimensionCombination** ja seejärel valige käsk **Laadi**.

    > [!TIP]
    > Loendis **Väljad** pange tabelile nimeks **Finantsdimensioonid**, et seda oleks lihtsam tuvastada.

7. Valige jaotis **Seoste haldamine** ja seejärel valige käsk **Uus**.
8. Valige esimesel väljal väärtus **Pearaamatu toimingud** ja seejärel valige väärtus **LedgerDimension**.
9. Teisel väljal valige väärtus **LedgerActivityMeasure\_DimensionCombination** (või **Finantsdimensioonid**, kui panite tabelile selle nime). Valige päis **DimensionCombinationRECID**.
10. Väljal **Kardinaalsus** valige väärtus **Mitu ühele**.
11. Määrake välja **Ristfiltri suund** väärtuseks **Üks**.
12. Valige käsud **Muuda seos aktiivseks** ja **Eelda viiteterviklust**, klõpsake nuppu **OK** ja seejärel nuppu **Sule**.

    [![Seose loomine](./media/Create-relationship.png)](./media/Create-relationship.png)

13. Loendis **Väljad** peaksite nägema tabelit ja saadaolevaid finantsdimensioone. Lohistage soovitud finantsdimensioonid aruandetaseme filtrite juurde.
14. Salvestage muudatused.
15. Paremklõpsake rakendusobjektide puul (AOT) projekti ja seejärel nuppu **Sünkrooni**.
16. Looge projekt ja seejärel avage tulemuste vaatamiseks rakendus.

    [![Valmis tööruum](./media/workspace.png)](./media/workspace.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]