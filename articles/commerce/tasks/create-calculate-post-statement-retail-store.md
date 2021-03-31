---
title: Jaekaupluse jaoks väljavõtete loomine, arvutamine ja sisestamine
description: See protseduur kirjeldab kaupluse kohta väljavõtte loomise, arvutamise ja sisestamise etappe.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 455dee5a14ca0c44ba823a467baa78352b367ec8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221301"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a>Jaekaupluse jaoks väljavõtete loomine, arvutamine ja sisestamine

[!include [banner](../includes/banner.md)]

See protseduur kirjeldab kaupluse kohta väljavõtte loomise, arvutamise ja sisestamise etappe. Samade ülesannete jaoks saab konfigureerida ka pakett-töid. Pakett-tööde konfigureerimise ja käitamise etapid leiate teistest teemadest. Selle protseduuri tegemiseks peavad teil olema kassas lõpule viidud ja seejärel Dynamics Dynamics 365 Commerce-i tõmmatud kanded. See salvestis kasutab demoettevõtte USRT andmeid.

1. Valige avalehel **Kaupluse rahandus**.
2. **Väljavõtte** valimine
3. Valige rippmenüüst suvand **Kaupluse number**.
4. Valige nupp **OK**.
5. Rühm **Häälestus** sisaldab sätteid, mis määravad, millised kanded kaasatakse väljavõttesse ja kuidas need väljavõtteridadele grupeeritakse. Saate rühma **Häälestus** avada ja neid sätteid muuta, kuid võite kasutada ka vaikesätteid.  
    - Väli **Väljavõtteviis** määratleb väljavõtteridade grupeerimise viisi.  
    - Valige väli **töötaja või register**, kui soovite arvutada väljavõtte ainult kindla töötaja või registri kohta.  
6. Valige suvand väljal **Sulgemismeetod**.
7. Valige toimingupaanilt **Lause arvutamine**.
8. Valige **Jah**.
    - Pärast väljavõtte arvutamist peaksid olema loodud read koos kogusummadega iga kasutatud makseviisi ja väljavõtteviisi kohta.  
    - Sisestage igale reale inventeeritud summa, kui see tuleb sisestada või seda värskendada. Inventeeritud summa väli täidetakse summadega kassas tehtud päevakassadest.  
9. Valige toimingupaanilt **Sisesta väljavõte**.
10. Valige suvand **Sule**.
11. Sulgege leht.
12. Valige avalehel **Kaupluse rahandus**.
13. Klõpsake vahekaarti **Sisestatud väljavõtted**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]