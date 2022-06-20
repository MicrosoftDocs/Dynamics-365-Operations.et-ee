---
title: Lisandunud projektikulud ostutarnete loenditest
description: See artikkel kirjeldab, kuidas ostu sissetulekutest kogunenud projekti kulusid saab jälgida moodulis Microsoft Dynamics 365 Finantsid.
author: sunfzam
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: twheeloc
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a138fd41269fad2e9ac489664ca81c3ee12f830d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856853"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a>Lisandunud projektikulud ostutarnete loenditest

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas ostu sissetulekutest kogunenud projekti kulusid saab jälgida moodulis Microsoft Dynamics 365 Finantsid. 

Projekti arved saabuvad sageli kaupade ja teenuste üleandmisest hiljem, millel võib olla märkimisväärne mõju projekti juhtimismõõdikutele (KPI-dele). Nende kannete jälgimise võimalus nii finants- kui ka projektiaruannetes on oluline.

Seda illustreerib järgmine näidisstsenaarium. 

Contoso Consulting on käivitanud uue pilvejuurutusprojekti. Luuakse ostutellimus projekti jaoks arvuti ostmiseks. Arvuti hind on 1500 $ ja paigaldusteenuste hind 150 $. Hankija on arvuti kohale toonud ja paigaldanud, kuid arve pole veel ettevõttesse Contoso Consulting jõudnud. Projektijuht soovib näha projekti maksumuse koondsummat 1650 $ enne arve kohaletoimetamist. See kulu peaks kajastuma ka ettevõtte kuu lõpu finantsaruannetes. 

Koondkulu tuleb kajastada nii finantstaseme kui ka projekti taseme aruandluses. Toote sissetuleku finantsuuendust saab jälgida kauba ja hanke kategooriates. 

Tehke kaupadele lehel **Ostureskontro parameetrid** valik **Sisesta toote sissetulek pearaamatusse**.
[![Ostureskontro parameetrite leht.](./media/accruals1-1024x409.png)](./media/accruals1.png) 

Hankekategooriate puhul tehke lehel **Kategooria poliitikareegel** valik **Ostmise** poliitikad ja valige siis iga hankekategooria kohta **Kogunev ostukulu vastuvõtmisel**.
[![Kategooria poliitikareegli leht.](./media/accruals2-1024x569.png)](./media/accruals2.png) 

Toote sissetulekuga seotud kannete sisestamisel kasutatakse kontosid **Arvele kandmata ostukulud** ja **Ostu viitvõlg** jaotises **Sisestamise seadistus**.

Kasutades sama stsenaariumi, vaatame, kuidas toote sissetuleku sisestamine mõjutab pearaamatu ja projekti andmeid. 

**1. etapp:** looge ja kinnitage uus projekti ostutellimus, mis kajastab arvuti ostu 1500 $ eest ja paigaldusteenuste ostu 150 $ eest.
[![Uue ostutellimuse loomine.](./media/accruals4-1024x497.png)](./media/accruals4.png) 

Kui ostutellimus on kinnitatud, luuakse projektile kooskõlastatud kulu kanded. 
[![Loodud kanded.](./media/accruals5-1024x219.png)](./media/accruals5.png) 

> [!NOTE]
> Kooskõlastatud kulu kannete väljal **Kande päritolu** on määratud väärtus **Ostutellimus**. Ostutellimuse koostamine ja kinnitamine ei loo projektile kandeid. 

**2. etapp:** kaubad ja teenused jõuavad kohale ja registreeritakse toote sissetulek. 

Toote sissetuleku sisestamisel luuakse kanne ja see sisestatakse pearaamatusse. Kanne debiteerib ostukulu, arveldamata kulu ja krediteerib ostu juurdekasvukontot. 
[![Kande tehingukanded.](./media/accruals6-1024x214.png)](./media/accruals6.png)

> [!NOTE]
> Toote sissetuleku sisestamisel kasutatakse hankekategooriate ja toodete sisestamise seadistust ning mitte projektikategooriate sisestamise seadistust. Ostu viitvõlgade õigeks kajastamiseks tuleb seda seadistust kohandada. 

Hankekategooriat saab lehel **Hankekategooria** projektikategooriatega vastendada.
[![Hankekategooria leht.](./media/accruals7-1024x390.png)](./media/accruals7.png)

**3. etapp:** hankija arve mustandi koostamine. 

Toote sissetuleku sisestamine ei mõjuta projekti andmeid. Lahendusena võite koostada hankija arve mustandi otse pärast ostukviitungi sisestamist. Minge lehele **Ostutellimus** &gt; **Vahekaart Arve** &gt; **Loo** &gt; **Arve**. Nii koostatakse ootel arvedokument, mis muudab projekti andmeid. 

Hankija arve mustandi loomisel luuakse ootel projektikanded. 
[![Ootel projektikanded.](./media/accruals8-1024x225.png)](./media/accruals8.png) 

Lehel **Kooskõlastatud kulu** suletakse 1. etapis loodud kirjed ja luuakse uued kirjed, mis kajastavad ootel hankija arvest pärinevat kulu kooskõlastust. Kooskõlastatud kulu väljale **Kande päritolu** määratakse väärtus **Hankija arve**.
[![Kooskõlastatud kulude leht.](./media/accruals9-1024x200.png)](./media/accruals9.png)

Hankija arve jääb ootel olekusse, kuni saabub tegelik hankija arve.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
