---
title: Eelarve loomine kandekontodelt ja summakontodelt
description: "Selles artiklis antakse ülevaade koondkontode alusel eelarvete loomise protsessist. Lisaks selgitatakse, kuidas koondkontode jaoks eelarve juhtimine sisse lülitada, kui eelarve juhtimine on nõutav."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fd6dc5173fd37f0257c98c1a41f3e6ce40b5b680
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a>Eelarve loomine kandekontodelt ja summakontodelt

[!include[banner](../includes/banner.md)]


Selles artiklis antakse ülevaade koondkontode alusel eelarvete loomise protsessist. Lisaks selgitatakse, kuidas koondkontode jaoks eelarve juhtimine sisse lülitada, kui eelarve juhtimine on nõutav.

Nii eelarveplaani kui ka eelarveregistri kande dokumendid võimaldavad eelarve koostamist põhikontodel, mille põhikonto tüübiks on **Kogusumma**. Tegelikud summad saab sisestada ainult ülekande põhikontodele. 

Perioodilise protsessi **Eelarveplaani loomine pearaamatust** puhul saate vahekaardil **Allikas** määrata kriteeriumina põhikonto tüübi **Kogusumma**. Sellisel juhul kaasatakse iga kogusumma põhikonto sihteelarveplaani ja summa on võrdne valitud põhikontode vahemiku kogusummaga. 

Saate aktiveerida eelarve juhtimise tüübiga **Kogusumma** põhikontode puhul. Seda funktsiooni toetatakse eelarvegruppide abil. Iga kogusumma põhikonto puhul tuleb eelarvegrupi puhul juhitav eelarve luua lehel **Eelarve juhtimise konfiguratsioon**. Teie määratud kriteeriumid peavad sisaldama kogusumma põhikontot ja kontode vahemikku. Eelarvegruppide loomise protsessi kiirendamiseks saate kasutada andmeüksust Eelarve juhtimise grupid. 

Eelarve kasutamisel aruandluses (nt finantsaruandes) koosneb kogusummat kajastav eelarvesumma järgmistest summadest:

-   eelarvetest, mis on loodud igast kande pearaamatukontost summakonto intervalli jooksul;
-   eelarvesummast, mis on sisestatud otse summakontole.

Seega saate luua eraldi eelarved summakonto intervalli olulisimate kandekontode puhul ja lisada seejärel saadaoleva eelarvesumma summakontole.




