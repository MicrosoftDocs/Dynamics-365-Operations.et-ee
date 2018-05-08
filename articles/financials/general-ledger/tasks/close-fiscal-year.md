--- 
title: Finantsaasta sulgemine
description: "See protseduur kirjeldab rahandusaasta sulgemise protsessi etappe, millega kantakse saldod uude finantsaastasse üle."
author: aprilolson
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4f2f1f1206f3cb3534ef93923d4945bb63814514
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="close-the-fiscal-year"></a>Finantsaasta sulgemine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur kirjeldab rahandusaasta sulgemise protsessi etappe, millega kantakse saldod uude finantsaastasse üle.


## <a name="validate-year-end-close-parameters"></a>Aastalõpu sulgemise parameetrite kontrollimine
1. Minge jaotisse Pearaamat > Pearaamatu seadistamine > Pearaamatu parameetrid.
2. Laiendage jaotist Rahandusaasta sulgemine.
3. Valige suvandi Kustuta aasta lõpetamise kanded ülekandmisel sätteks Jah või Ei.
    * Kui rahandusaasta on juba suletud ja aastalõpu sulgemine käivitatakse uuesti, on see säte oluline. Kui väärtuseks on määratud Jah, kustutatakse eelmise aastalõpu sulgemise kanne ja luuakse uus kanne kõigile kontode algsaldodele. Kui väärtuseks on määratud Ei, jääb eelmine kanne alles ja uus kanne luuakse ainult korrigeerimiskannetele, mis sisestati pärast viimast aastalõpu sulgemist.  
4. Valige suvandi Loo ülekande ajal sulgemiskanded sätteks Jah või Ei.
    * Kui väärtuseks on määratud Jah, luuakse kaks kannet. Üks kanne luuakse suletavas rahandusaastas, et viia tulu- ja kulukontode saldod nulli, ja teine kanne luuakse järgmises rahandusaastas algsaldode jaoks. Kui väärtuseks on määratud Ei, luuakse järgmises rahandusaastas algsaldode jaoks üks kanne.  
5. Valige suvandi Määra rahandusaasta olek püsivalt suletuks sätteks Jah või Ei.
    * Kui väärtuseks on määratud Jah, määratakse rahandusaasta olekuks Jäädavalt suletud.  Kuna jäädavalt suletud aastat ei saa uuesti avada, tasub määrata selle valiku väärtuseks Ei.  
6. Valige suvandi Kande number tuleb aastalõpu sulgemise käigus täita sätteks Jah või Ei.
    * Kui väärtuseks on määratud Jah, tuleb aastalõpu sulgemisprotsessi käigus kande number käsitsi sisestada. Selle kande numbri loomiseks ei kasutata numbriseeriat. Selle väärtuse olekuks tasub määrata Jah.  
7. Sulgege leht.
8. Minge jaotisse Pearaamat > Perioodi sulgemine > Rahandusaasta sulgemine.
9. Klõpsake aastalõpu sulgemise malli loomiseks nuppu Uus.
    * Juriidiliste isikute grupile, mille puhul aastalõpu sulgemine käivitada, saab luua malli. Seda malli saab igal aastal uuesti kasutada.  
10. Sisestage väljale Grupi nimi aastalõpu sulgemise malli nimi.
11. Valige rahandusaasta, mille jaoks mall luuakse.
    * Aastalõpu sulgemise malli saab kokku panna ainult sama rahandusaastat kasutavad juriidilised isikud. Seda seetõttu, et aastalõpu sulgemine toimub rahandusaasta, mitte kuupäeva valimisega.  
12. Kasutage otseteed kirje salvestamiseks.
13. Klõpsake nuppu Lisa juriidiliste isikute valimiseks sellele mallile.
    * Juriidilisi isikuid saab lisada, valides juriidilised isikud või organisatsiooni hierarhia.  Lisatakse ainult need organisatsiooni hierarhiad, millel on valitud sama rahanduskalender.  
14. Valige juriidilised isikud või organisatsiooni hierarhia.
15. Klõpsake nuppu OK.
16. Valige, kas finantsdimensioonid viiakse järgmisse rahandusaastasse üle.
    * Selle valiku väärtuseks tasub bilansikontode puhul määrata Jah.  See säilitab bilansikontode algsaldode loomisel sisestatud kannete finantsdimensioonid.  Tulu- ja kulukontode puhul võite valida finantsdimensioonide säilitamise (Sule kõik), kui saldod viiakse jaotisse Jaotamata kasum, või lasta finantsdimensioonid asendada teise dimensiooniväärtusega (Sule üksik). Kui teete valiku Sule üksik, saate määratleda igale dimensioonile konkreetse dimensiooniväärtuse või isegi selle tühjaks jätta.  
17. Klõpsake nuppu Salvesta.
18. Käivitage aastalõpu sulgemine, tehes tegumiribal valiku Rahandusaasta sulgemise käivitamine.
    * Valitud mallil käivitatakse aastalõpu sulgemine.  
19. Valige mallilt kõik juriidilised isikud või nende alamkogum, mille puhul aastalõpu sulgemine käivitada.
    * Aastalõpu sulgemise esmakordsel käivitamisel võib enamik organisatsioone otsustada algsaldode saamiseks käivitada aastalõpu sulgemise kõigi malli juriidiliste isikute puhul. Kui pärast seda tehakse korrigeerimiskandeid, võite valida aastalõpu sulgemise käivitamise ainult nende juriidiliste isikute puhul, kellel on korrigeerimisi.  
20. Klõpsake nuppu OK.
21. Valige finantsaasta, mille puhul aastalõpu sulgemine käivitada.
22. Tippige väärtus väljale Kanne.
    * On hea mõte lisada kande numbrisse rahandusaasta, et loodud aastalõpu sulgemise kannet oleks lihtsam leida.  
23. Aastalõpu sulgemine käivitub vaikimisi partiina.
    * Aeganõudvate protsesside puhul on mõistlik kasutada partiirežiimi. See on tavaliselt üks neist protsessidest, seetõttu on vaikesäte partiirežiimi kasutamine.  
24. Klõpsake nuppu OK.


