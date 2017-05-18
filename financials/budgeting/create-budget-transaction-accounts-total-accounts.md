---
title: Eelarve loomine kandekontodelt ja summakontodelt
description: "Selles artiklis antakse ülevaade koondkontode alusel eelarvete loomise protsessist. Lisaks selgitatakse, kuidas koondkontode jaoks eelarve juhtimine sisse lülitada, kui eelarve juhtimine on nõutav."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: ea1f8230c360a196f505e0f9d0fb178b43a9072f
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


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




