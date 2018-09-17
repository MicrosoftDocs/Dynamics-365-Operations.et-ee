--- 
title: "Kauba saabumise ülevaateprofiili seadistamine"
description: "See ülesanne keskendub saabumisülevaate profiili seadistusele."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 5ddc491d73bbb6ac02e37a9c9b9d93545f6f9556
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---
# <a name="set-up-an-item-arrival-overview-profile"></a>Kauba saabumise ülevaateprofiili seadistamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See ülesanne keskendub saabumisülevaate profiili seadistusele. Saabumisülevaate profiil on kogumik reegleid, mida rakendatakse, kui kasutaja avaneb lehe Saabumisülevaade. Saate seda protseduuri kasutada demoandmete ettevõttes USMF. Seda protseduuri viib tavaliselt läbi vastuvõtuametnik.





1. Avage Varude haldus > Seadistus > Jaotus > Saabumisülevaate profiilid.
2. Klõpsake valikut Uus.
    * Kuna töötate täis veokikoormate mahalaadimisel peaaegu alati samas laos, peaksite looma saabuvate kaupade registreerimise lihtsustamiseks saabumisülevaate profiili.  
3. Sisestage väärtus väljale Saabumisülevaate profiili nimi.
4. Valige suvand väljal Kuva read.
    * Valige, milliseid ridu sissetulekute puhul kuvada: kõik – saate kuvada kõik read olenemata olekust.   Pooleli – kuvatakse read sissetulekute puhul, mil edenemise olekuks on Lõpetatud või Pooleli. See tähendab, et iga rea puhul on saabumistöölehele registreeritud täielik või osaline kogus.   Lõpetamata – kuvatakse read sissetulekute puhul, mil edenemise olekuks on Puudub või Pooleli. See tähendab, et iga rea puhul on saabumistöölehele registreeritud mitte midagi või ainult osa kogusest.  
5. Laiendage või ahendage jaotist Saabumisvalikud.
6. Sisestage väärtus väljale Päevi edasi.
    * See seadistab filtri kuvama sissetuleku ridu, mille saabumist eeldatakse järgmise paari päeva jooksul (olenevalt teie määratud numbrist).  
7. Sisestage väärtus väljale Päevi tagasi.
    * See seadistab filtri kuvama sissetuleku ridu, mille saabumist eeldatakse arv päevi enne tänast.  
8. Sisestage väärtus väljale Laod.
    * Saate filtreerida ühe või mitme lao alusel.  
9. Valige väärtus väljalt Tarneviis.
    * See määrab filtri kuvama ainult selle tarneviisiga sissetulekuread.  
10. Valige väljalt Nimi väärtus WHS.
11. Valige väljalt Ladu ladu 24.
    * See on vaikeladu, mida kasutatakse seda profiili kasutavate registreeritud sissetuleku ridadega.  
12. Valige Baydoor väljalt Asukoht.
    * See on vaikeasukoht, mida kasutatakse seda profiili kasutavate registreeritud sissetuleku ridadega.  
13. Laiendage või ahendage jaotist Saabumispäringu üksikasjad.
14. Väljal Piira tegevuskohaga valige tegevuskoht 2.
    * See määrab filtri kuvama ainult selle tegevuskohaga sissetulekuread.  
15. Määrake valiku Ostutellimused väärtuseks Jah.
    * Saate valida sissetulekuridu ostutellimustest.  
16. Määrake valiku Üleviimistellimused väärtuseks Jah.
    * Saate valida sissetulekuridu üleviimistellimustest.  
17. Klõpsake nuppu Salvesta.
18. Sulgege leht.


