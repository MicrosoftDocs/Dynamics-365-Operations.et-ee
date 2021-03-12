---
title: Kauba saabumise ülevaateprofiili seadistamine
description: Selles teemas keskendutakse saabumise ülevaate profiilile.
author: ShylaThompson
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ecfe132d9b0e096c5fdf015f80a6efb34c9b178
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961424"
---
# <a name="set-up-an-item-arrival-overview-profile"></a>Kauba saabumise ülevaateprofiili seadistamine

[!include [banner](../../includes/banner.md)]]

Selles teemas keskendutakse saabumise ülevaate profiilile. Saabumisülevaate profiil on kogumik reegleid, mida rakendatakse, kui kasutaja avaneb lehe Saabumisülevaade. Saate seda protseduuri kasutada demoandmete ettevõttes USMF. Seda protseduuri viib tavaliselt läbi vastuvõtuametnik.

1. Navigeerimispaanil avage **Moodulid > Varude haldus > Seadistus > Jaotus > Saabumise ülevaate profiilid**.
2. Valige suvand **Uus**. Kuna töötate täis veokikoormate mahalaadimisel peaaegu alati samas laos, peaksite looma saabuvate kaupade registreerimise lihtsustamiseks saabumisülevaate profiili.  
3. Trükkige väärtus väljale **Saabumise ülevaate profiili nimi**.
4. Valige suvand väljal **Näita ridu**. Valige milliseid ridu näidata kviitungitel.  

    - **Kõik** – näitab kõiki ridu, olenemata olekust.   
    - **Töötluses** – näitab kviitungitel kõiki ridu, millel on töötlemine kas lõpetatud või osaline. See tähendab, et iga rea puhul on saabumistöölehele registreeritud täielik või osaline kogus.   
    - **Lõpetamata** – näitab kviitungitel kõiki ridu, millel on töötlemine kas puudu või osaline. See tähendab, et iga rea puhul on saabumistöölehele registreeritud mitte midagi või ainult osa kogusest.  

5. Jaotise **Saabumise suvandid** laiendamine või ahendamine.
6. Sisestage väärtus väljale **Päevi edasi**. See seadistab filtri kuvama sissetuleku ridu, mille saabumist eeldatakse järgmise paari päeva jooksul (olenevalt teie määratud numbrist).  
7. Sisestage väärtus väljale **Päevi tagasi**. See seadistab filtri kuvama sissetuleku ridu, mille saabumist eeldatakse arv päevi enne tänast.  
8. Sisestage väärtus väljale **Laod**. Saate filtreerida ühe või mitme lao alusel.  
9. Valige väärtus väljal **Tarneviis**. See määrab filtri kuvama ainult selle tarneviisiga sissetulekuread.  
10. Valige WHS väljal **Nimi**.
11. Valige ladu 24 väljal **Ladu**. See on vaikeladu, mida kasutatakse seda profiili kasutavate registreeritud sissetuleku ridadega.  
12. Valige väljal **Asukoht** suvand **Baydoor**. See on vaikeasukoht, mida kasutatakse seda profiili kasutavate registreeritud sissetuleku ridadega.  
13. Jaotise **Saabumise päringu üksikasjad** laiendamine või ahendamine.
14. Valige koht 2 väljal **Piira kohaga**. See määrab filtri kuvama ainult selle tegevuskohaga sissetulekuread.  
15. Määrake suvandi **Ostutellimused** väärtuseks **Jah**. Saate valida sissetulekuridu ostutellimustest.  
16. Määrake suvandi tellimuste **Edastus** väärtuseks **Jah**. Saate valida sissetulekuridu üleviimistellimustest.  
17. Valige käsk **Salvesta**.
18. Sulgege leht.

