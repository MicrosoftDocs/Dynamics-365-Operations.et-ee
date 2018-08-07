---
title: "Pearaamatupidaja tööruumile finantsdimensioonide lisamine"
description: "Selles teemas selgitatakse, kuidas lisada pearaamatupidaja tööruumi finantsdimensioonid, et neid saaks kasutada pearaamatu ja eelarvearuannetes."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5faefe5da8c3a64987a38ebef92eb87049ebe874
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a>Pearaamatupidaja tööruumile finantsdimensioonide lisamine

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas lisada pearaamatupidaja tööruumi finantsdimensioone, et neid saaks kasutada pearaamatu- ja eelarvearuannetes. Pearaamatupidaja tööruumis on vahekaart **Ülevaade** ja vahekaart **Finants**. Nendel vahekaartidel kuvatavad aruanded põhinevad kahel mõõdikul: LedgerActivityMeasure ja BudgetActivityMeasure. Rakenduses Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juuli 2017) on nende mõõdikute ja DimensionCombinationEntity üksuse vahel seoste kogum. Seega saate valida dimensioonid.

1. Uuendage rakenduse Finance and Operations lehel **Üksuse pood** mõõdikud **LedgerActivityMeasure** ja **BudgetActivityMeasure**.
2. Avage rakenduses Microsoft Visual Studio rakenduste sirvija ja otsige rakendust **LedgerCFO**.
3. Jaotises **Ressursid** avage rakendus **LedgerCFOWorkspacePBIX**.
4. Kui ressurss avaneb Microsoft Power BI töölaual, siis valige käsk **Too andmed**, seejärel valige käsk **SQL serveri andmebaas** ja siis klõpsake nuppu **Ühenda**.
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

