---
title: Projektikulu juurdekasv ostu sissetulekute korral
description: "Selles teemas kirjeldatakse, kuidas ostu sissetulekutest kogunevaid projektikulusid saab Microsoft Dynamics 365 for Operationsis jälgida."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 9caa1f7818e21ae448effc6169e1fe02c8edf510
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="project-cost-accrual-on-purchase-receipts"></a>Projektikulu juurdekasv ostu sissetulekute korral

[!include[banner](../includes/banner.md)]


Selles teemas kirjeldatakse, kuidas ostu sissetulekutest kogunevaid projektikulusid saab Microsoft Dynamics 365 for Operationsis jälgida. 

Projekti arved saabuvad sageli kaupade ja teenuste üleandmisest hiljem, millel võib olla märkimisväärne mõju projekti juhtimismõõdikutele (KPI-dele). Nende kannete jälgimise võimalus nii finants- kui ka projektiaruannetes on oluline.

Seda illustreerib järgmine näidisstsenaarium. 

Contoso Consulting on käivitanud uue pilvejuurutusprojekti. Luuakse ostutellimus projekti jaoks arvuti ostmiseks. Arvuti hind on 1500 $ ja paigaldusteenuste hind 150 $. Hankija on arvuti kohale toonud ja paigaldanud, kuid arve pole veel ettevõttesse Contoso Consulting jõudnud. Projektijuht soovib näha projekti maksumuse koondsummat 1650 $ enne arve kohaletoimetamist. See kulu peaks kajastuma ka ettevõtte kuu lõpu finantsaruannetes. 

Koondkulu tuleb kajastada nii finantstaseme kui ka projekti taseme aruandluses. Dynamics 365 for Operationsis saab toote sissetuleku finantsuuendus jälgida kauba ja hanke kategooriates. 

Tehke kaupadele lehel **Ostureskontro parameetrid** valik **Sisesta toote sissetulek pearaamatusse**.
[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png) 

Hankekategooriate puhul tehke lehel **Kategooria poliitikareegel** valik **Ostmise** poliitikad ja valige siis iga hankekategooria kohta **Kogunev ostukulu vastuvõtmisel**.
[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png) 

Toote sissetulekuga seotud kannete sisestamisel kasutatakse kontosid **Arvele kandmata ostukulud** ja **Ostu viitvõlg** jaotises **Sisestamise seadistus**.
[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png) 

Kasutades sama stsenaariumi, vaatame, kuidas toote sissetuleku sisestamine mõjutab pearaamatu ja projekti andmeid. 

**1. etapp:** looge ja kinnitage uus projekti ostutellimus, mis kajastab arvuti ostu 1500 $ eest ja paigaldusteenuste ostu 150 $ eest.
[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Kui ostutellimus on kinnitatud, luuakse projektile kooskõlastatud kulu kanded. 
[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> Kooskõlastatud kulu kannete väljal **Kande päritolu** on määratud väärtus **Ostutellimus**. Ostutellimuse koostamine ja kinnitamine ei loo projektile kandeid. 

**2. etapp:** kaubad ja teenused jõuavad kohale ja registreeritakse toote sissetulek. 

Toote sissetuleku sisestamisel luuakse kanne ja see sisestatakse pearaamatusse. Kanne debiteerib ostukulu, arveldamata kulu ja krediteerib ostu juurdekasvukontot. 
[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Toote sissetuleku sisestamisel kasutatakse hankekategooriate ja toodete sisestamise seadistust ning mitte projektikategooriate sisestamise seadistust. Ostu viitvõlgade õigeks kajastamiseks tuleb seda seadistust kohandada. 

Hankekategooriat saab lehel **Hankekategooria** projektikategooriatega vastendada.
[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)

**3. etapp:** hankija arve mustandi koostamine. 

Dynamics 365 for Operationsis ei mõjuta toote sissetuleku sisestamine projekti andmeid. Lahendusena võite koostada hankija arve mustandi otse pärast ostukviitungi sisestamist. Minge lehele **Ostutellimus** &gt; **Vahekaart Arve** &gt; **Loo** &gt; **Arve**. Nii koostatakse ootel arvedokument, mis muudab projekti andmeid. 

Hankija arve mustandi loomisel luuakse ootel projektikanded. 
[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png) 

Lehel **Kooskõlastatud kulu** suletakse 1. etapis loodud kirjed ja luuakse uued kirjed, mis kajastavad ootel hankija arvest pärinevat kulu kooskõlastust. Kooskõlastatud kulu väljale **Kande päritolu** määratakse väärtus **Hankija arve**.
[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)

Hankija arve jääb ootel olekusse, kuni saabub tegelik hankija arve.




