---
title: Finantsaasta sulgemine
description: See protseduur kirjeldab rahandusaasta sulgemise protsessi etappe, millega kantakse saldod uude finantsaastasse üle.
author: aprilolson
ms.date: 11/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d52e6789a96defaf1d0132fe97fc183a05af207
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779796"
---
# <a name="close-the-fiscal-year"></a>Finantsaasta sulgemine

[!include [banner](../../includes/banner.md)]

See protseduur kirjeldab rahandusaasta sulgemise protsessi etappe, millega kantakse saldod uude finantsaastasse üle.


## <a name="validate-year-end-close-parameters"></a>Aastalõpu sulgemise parameetrite kontrollimine
1. Avage **Navigeerimispaan > Moodulid > Pearaamat > Pearaamatu häälestus > Pearaamatu parameetrid**.
2. Laiendage jaotist **Rahandusaasta** sulgemine.
3. Ülekande **ajal** aasta **sulgemiskannete** **kustutamise suvandile Jah või** Ei.
    
Kui rahandusaasta on juba suletud ja aastalõpu sulgemine käivitatakse uuesti, on see säte oluline. Kui seatud väärtusele **Jah**, kustutatakse eelmise aasta lõpu sulgemise kanne ja kõigile kontodele, mille algsaldod algavad, luuakse uus kanne. Kui valitud **on Ei**, jääb eelmine kanne alles ning pärast eelmise aasta lõppu sisestatud kannete korrigeerimiseks luuakse uus kanne.

4. Ülekande **ajal** sulgemiskannete **loomise** suvandile **Jah või** Ei.

Kui on seatud väärtusele **Jah**, luuakse kaks tehingut. Suletav rahandusaasta kohta luuakse üks kanne, et viia kõigi pearaamatukontode saldod nulli ja järgmine finantsaasta luuakse algsaldode kohta teine kanne. Kui seatud väärtusele **Ei**, luuakse algsaldode jaoks järgmisel rahandusaastal üks kanne.  

5. Valige **Suvand Jah** või **Ei**, et finantsaasta **olekuks määrata jäädavalt suletud**.

Kui valitud on **Jah**, seatakse finantsaasta olekuks **Jäädavalt suletud**. Kuna jäädavalt suletud aastat ei saa uuesti avada, oleks selle suvandi väärtuseks määrata **Ei**.  

6. Aasta **lõpu** sulgemise **suvandi** jooksul **tuleb kandenumbri jaoks sisestada väärtus Jah või** Ei.

Kui seatud väärtusele **Jah**, tuleb kande number aasta lõpu sulgemise protsessis käsitsi sisestada. Selle kande numbri loomiseks ei kasutata numbriseeriat. Hea tava on seada selle väärtuseks **Jah**.  

7. Sulgege leht.
8. Minge jaotisse **Pearaamat > Perioodi sulgemine > Rahandusaasta sulgemine**.
9. Klõpsake aastalõpu sulgemise malli loomiseks nuppu **Uus**.

Juriidiliste isikute grupile, mille puhul aastalõpu sulgemine käivitada, saab luua malli. Seda malli saab igal aastal uuesti kasutada.  

10. Sisestage **väljale Grupi** nimi aasta lõpu sulgemise malli nimi.
11. Valige väljal **Rahanduskalender** finantsaasta, mille jaoks mall luuakse.

Aastalõpu sulgemise malli saab kokku panna ainult sama rahandusaastat kasutavad juriidilised isikud. Seda seetõttu, et aastalõpu sulgemine toimub rahandusaasta, mitte kuupäeva valimisega.  

12. Klõpsake **Toimingupaanil** valikut **Salvesta**.
13. Klõpsake jaotises **Juriidilised isikud** nuppu **Lisa**, et valida selle malli juriidilised isikud.
    
Juriidilisi isikuid saab lisada, valides juriidilised isikud või organisatsiooni hierarhia. Lisatakse ainult need organisatsiooni hierarhiad, millel on valitud sama rahanduskalender.  

14. Valige juriidilised isikud või organisatsiooni hierarhia.
15. Klõpsake valikut **OK**.
16. Ülekande **bilansidimensioonis** **valige** **Jah või Ei.**

On hea, kui seadistada see valik bilansikontode **puhul** väärtusele Jah. See säilitab bilansikontode algsaldode loomisel sisestatud kannete finantsdimensioonid. Kasumi- ja kahjumikontode puhul saate valida finantsdimensioonide säilitamise (**Sulge** kõik), kui saldod teisaldatakse jaotamata kasumisse või saate valida, et finantsdimensioonid asendatakse teise dimensiooniväärtusega (**sule üksik**). Kui valite väärtuse **Sule** üksik, saate igale dimensioonile määrata kindla dimensiooniväärtuse või isegi jätta selle tühjaks.  

17. Klõpsake valikut **Salvesta**.
18. Käivitage aastalõpu sulgemine valides **Rahandusaasta sulgemise käivitamine** **Toimingupaanil**. Valitud mallil käivitatakse aastalõpu sulgemine.  
19. Valige mallilt kõik juriidilised isikud või nende alamkogum, mille puhul aastalõpu sulgemine käivitada.

Aastalõpu sulgemise esmakordsel käivitamisel võib enamik organisatsioone otsustada algsaldode saamiseks käivitada aastalõpu sulgemise kõigi malli juriidiliste isikute puhul. Kui pärast seda tehakse korrigeerimiskandeid, võite valida aastalõpu sulgemise käivitamise ainult nende juriidiliste isikute puhul, kellel on korrigeerimisi.  

20. Klõpsake valikut **OK**.
21. Valige finantsaasta, mille puhul aastalõpu sulgemine käivitada.
22. Tippige väärtus väljale **Kanne**. On hea mõte lisada kande numbrisse rahandusaasta, et loodud aastalõpu sulgemise kannet oleks lihtsam leida.  
23. Aastalõpu sulgemine käivitub vaikimisi partiina. Aeganõudvate protsesside puhul on mõistlik kasutada partiirežiimi. See on tavaliselt üks neist protsessidest, seetõttu on vaikesäte partiirežiimi kasutamine.  
24. Klõpsake valikut **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
