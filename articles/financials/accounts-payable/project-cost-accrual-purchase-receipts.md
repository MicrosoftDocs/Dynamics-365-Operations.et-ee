---
title: Projektikulu juurdekasv ostu sissetulekute korral
description: "Selles teemas kirjeldatakse, kuidas ostu sissetulekutest kogunevaid projektikulusid saab Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis jälgida."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: f7355dc856d97a19d0f7558061b3e2d9902dab65
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---

# <a name="project-cost-accrual-on-purchase-receipts"></a>Projektikulu juurdekasv ostu sissetulekute korral

[!include[banner](../includes/banner.md)]


Selles teemas kirjeldatakse, kuidas ostu sissetulekutest kogunevaid projektikulusid saab Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis jälgida. 

Projekti arved saabuvad sageli kaupade ja teenuste üleandmisest hiljem, millel võib olla märkimisväärne mõju projekti juhtimismõõdikutele (KPI-dele). Nende kannete jälgimise võimalus nii finants- kui ka projektiaruannetes on oluline.

Seda illustreerib järgmine näidisstsenaarium. 

Contoso Consulting on käivitanud uue pilvejuurutusprojekti. Luuakse ostutellimus projekti jaoks arvuti ostmiseks. Arvuti hind on 1500 $ ja paigaldusteenuste hind 150 $. Hankija on arvuti kohale toonud ja paigaldanud, kuid arve pole veel ettevõttesse Contoso Consulting jõudnud. Projektijuht soovib näha projekti maksumuse koondsummat 1650 $ enne arve kohaletoimetamist. See kulu peaks kajastuma ka ettevõtte kuu lõpu finantsaruannetes. 

Koondkulu tuleb kajastada nii finantstaseme kui ka projekti taseme aruandluses. Finance and Operationsis saab toote sissetuleku finantsuuendus jälgida kauba ja hanke kategooriates. 

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

Finance and Operationsis ei mõjuta toote sissetuleku sisestamine projekti andmeid. Lahendusena võite koostada hankija arve mustandi otse pärast ostukviitungi sisestamist. Minge lehele **Ostutellimus** &gt; **Vahekaart Arve** &gt; **Loo** &gt; **Arve**. Nii koostatakse ootel arvedokument, mis muudab projekti andmeid. 

Hankija arve mustandi loomisel luuakse ootel projektikanded. 
[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png) 

Lehel **Kooskõlastatud kulu** suletakse 1. etapis loodud kirjed ja luuakse uued kirjed, mis kajastavad ootel hankija arvest pärinevat kulu kooskõlastust. Kooskõlastatud kulu väljale **Kande päritolu** määratakse väärtus **Hankija arve**.
[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)

Hankija arve jääb ootel olekusse, kuni saabub tegelik hankija arve.




