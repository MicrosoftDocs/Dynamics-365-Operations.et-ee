---
title: Finantsaasta sulgemine
description: See protseduur kirjeldab rahandusaasta sulgemise protsessi etappe, millega kantakse saldod uude finantsaastasse üle.
author: aprilolson
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1ade9af06848b125fb6253ea1182f6098588150
ms.sourcegitcommit: 88f8a0369ce66b82314db9639491b695e18a7e5c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902503"
---
# <a name="close-the-fiscal-year"></a>Finantsaasta sulgemine

[!include [banner](../../includes/banner.md)]

See protseduur kirjeldab rahandusaasta sulgemise protsessi etappe, millega kantakse saldod uude finantsaastasse üle.


## <a name="validate-year-end-close-parameters"></a>Aastalõpu sulgemise parameetrite kontrollimine
1. Avage **Navigeerimispaan > Moodulid > Pearaamat > Pearaamatu häälestus > Pearaamatu parameetrid**.
2. Laiendage jaotist **Rahandusaasta** sulgemine.
3. Valige suvandi **Kustuta aasta lõpetamise kanded ülekandmisel** väärtuseks „Jah“ või „Ei“.
    
    Kui rahandusaasta on juba suletud ja aastalõpu sulgemine käivitatakse uuesti, on see säte oluline. Kui väärtuseks on määratud Jah, kustutatakse eelmise aastalõpu sulgemise kanne ja luuakse uus kanne kõigile kontode algsaldodele. Kui väärtuseks on määratud Ei, jääb eelmine kanne alles ja uus kanne luuakse ainult korrigeerimiskannetele, mis sisestati pärast viimast aastalõpu sulgemist.

4. Valige suvandi **Loo ülekande ajal sulgemiskanded** väärtuseks „Jah“ või „Ei“.

    Kui väärtuseks on määratud Jah, luuakse kaks kannet. Suletav rahandusaasta kohta luuakse üks kanne, et viia kõigi pearaamatukontode saldod nulli ja järgmine finantsaasta luuakse algsaldode kohta teine kanne. Kui väärtuseks on määratud Ei, luuakse järgmises rahandusaastas algsaldode jaoks üks kanne.  

5. Valige suvandi **Määra rahandusaasta olek püsivalt suletuks** väärtuseks „Jah“ või „Ei“.

    Kui väärtuseks on määratud Jah, määratakse rahandusaasta olekuks Jäädavalt suletud.  Kuna jäädavalt suletud aastat ei saa uuesti avada, tasub määrata selle valiku väärtuseks Ei.  

6. Valige suvandi **Kande number tuleb aastalõpu sulgemise käigus täita** väärtuseks „Jah“ või „Ei“.

    Kui väärtuseks on määratud Jah, tuleb aastalõpu sulgemisprotsessi käigus kande number käsitsi sisestada. Selle kande numbri loomiseks ei kasutata numbriseeriat. Selle väärtuse olekuks tasub määrata Jah.  

7. Sulgege leht.
8. Minge jaotisse **Pearaamat > Perioodi sulgemine > Rahandusaasta sulgemine**.
9. Klõpsake aastalõpu sulgemise malli loomiseks nuppu **Uus**.

    Juriidiliste isikute grupile, mille puhul aastalõpu sulgemine käivitada, saab luua malli. Seda malli saab igal aastal uuesti kasutada.  

10. Sisestage väljale **Grupi nimi** aastalõpu sulgemise malli nimi.
11. Valige väljal **Rahanduskalender** finantsaasta, mille jaoks mall luuakse.

    Aastalõpu sulgemise malli saab kokku panna ainult sama rahandusaastat kasutavad juriidilised isikud. Seda seetõttu, et aastalõpu sulgemine toimub rahandusaasta, mitte kuupäeva valimisega.  

12. Klõpsake **Toimingupaanil** valikut **Salvesta**.
13. Klõpsake jaotises **Juriidilised isikud** nuppu **Lisa**, et valida selle malli juriidilised isikud.
    
    Juriidilisi isikuid saab lisada, valides juriidilised isikud või organisatsiooni hierarhia.  Lisatakse ainult need organisatsiooni hierarhiad, millel on valitud sama rahanduskalender.  

14. Valige juriidilised isikud või organisatsiooni hierarhia.
15. Klõpsake valikut **OK**.
16. Valige „Jah“ või „Ei“ **Edasta bilansidimensioon**.

    Selle valiku väärtuseks tasub bilansikontode puhul määrata Jah. See säilitab bilansikontode algsaldode loomisel sisestatud kannete finantsdimensioonid. Tulu- ja kulukontode puhul võite valida finantsdimensioonide säilitamise (Sule kõik), kui saldod viiakse jaotisse Jaotamata kasum, või lasta finantsdimensioonid asendada teise dimensiooniväärtusega (Sule üksik). Kui teete valiku Sule üksik, saate määratleda igale dimensioonile konkreetse dimensiooniväärtuse või isegi selle tühjaks jätta.  

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
