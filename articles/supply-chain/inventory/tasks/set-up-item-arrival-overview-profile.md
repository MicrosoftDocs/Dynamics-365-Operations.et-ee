---
title: Kauba saabumise ülevaateprofiili häälestus
description: See artikkel keskendub saabumise ülevaate profiili seadistusele.
author: yufeihuang
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8517710f5d0be1859f86449152712d950281769a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872003"
---
# <a name="set-up-an-item-arrival-overview-profile"></a>Kauba saabumise ülevaateprofiili häälestus

[!include [banner](../../includes/banner.md)]

See artikkel keskendub saabumise ülevaate profiili seadistusele. Saabumisülevaate profiil on kogumik reegleid, mida rakendatakse, kui kasutaja avaneb lehe Saabumisülevaade. Saate seda protseduuri kasutada demoandmete ettevõttes USMF. Seda protseduuri viib tavaliselt läbi vastuvõtuametnik.

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
