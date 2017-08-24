--- 
title: Tootmisvoo versiooni loomine
description: See protseduur keskendub uue tootmisvoo versiooni loomisele.
author: cvocph
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 3cd2ff6f410e3817f3e23a651b7a2febf38b072b
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-production-flow-version"></a>Tootmisvoo versiooni loomine

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur keskendub uue tootmisvoo versiooni loomisele. Selle protseduuri puhul tuleb määratleda lean manufacturingi tootmisparameetrid ja klassiaja mõõtühikud. Peate määratlema ka väärtuse voo ja tootmisgrupi. Lisateavet tootmisvoogude ja lean manufacturingi tegevuste kohta vaadake Microsoft Dynamics AX-i lean manufacturingi tehnilistest ülevaadetest. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="create-a-production-flow"></a>Tootmisvoo loomine
1. Minge jaotisse Tootmise juhtimine > Seadistus > Kulusäästlik tootmisvoog > Tootmisvood.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Nimi.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.
6. Klõpsake loendis valitud real olevat linki.
    * Valige väärtuse voo tüüpi tootmisüksus. Väärtuse voog on tootmisüksus, mis hõlmab kõiki väärtuse voo tegevusi ja voogusid. Selles etapis on tootmisüksused piiratud juriidilise isikuga ja muid funktsioone neil pole.  
7. Klõpsake väljal Tootmisgrupp otsingu avamiseks ripploendi nuppu.
8. Klõpsake loendis valitud real olevat linki.
    * Valige tootmisvoole tootmisgrupp. Tootmisgrupid võimaldavad tootmisprotsessi jaoks materjali, tööjõu ja lõpetamata toodangu kontode määratlemise. Raamatupidamise konteksti seostamiseks tootmisvooga tuleb valida tootmisgrupp.  
9. Klõpsake nuppu Salvesta.

## <a name="create-a-production-flow-version"></a>Tootmisvoo versiooni loomine
1. Klõpsake vahekaarti Lisa.
2. Sisestage kuupäev ja kellaaeg väljale Aegumiskuupäev.
    * Vajaduse korral määratlege versiooni aegumiskuupäev. Saate seda igal ajal värskendada isegi aktiivsete versioonide puhul. Saate selle abil planeerida versiooni kasutuselt kõrvaldamise.  
3. Klõpsake nuppu OK.
4. Märkige loendis valitud rida.
5. Sisestage väärtus väljale Ühik.
6. Tehke taktiühiku toiming ResolveChanges.
7. Sisestage number väljale Keskmine takti aeg.
    * Määratlege versiooni keskmine takti aeg. Tootmisvoo versiooni takti juhtimiseks määratlege suunatud keskmine takti aeg. Takti määratletakse kogusena ajaperioodi kohta. Selles näiteks on takti aeg 0,2 tundi 10 tk kohta. Kaheksatunnise tööaja puhul vastab see igapäevasele läbilaskevõimele 400 tk.  
8. Sisestage number väljale Kogus tsükli kohta.
    * Määratlege kogus tsükli kohta seoses keskmise takti ajaga.  
9. Laiendage jaotist Versiooni üksikasjad.
10. Sisestage number väljale Minimaalne takti aeg.
    * Määratlege minimaalne takti aeg. Minimaalne takti aeg peab olema väiksem või sama kui keskmine takti aeg.  
11. Sisestage number väljale Maksimaalne takti aeg.
    * Maksimaalne takti aeg peab olema suurem või sama kui keskmine takti aeg.  
12. Sisestage number väljale Tegeliku tsükli aja periood (päevades)
    * Sisestage väljale Tegeliku tsükliaja periood päevade arv. Tegeliku tsükliaja periood on tegelikust minutist tagasisuunas koondatud tööde päevade arv tegeliku tsükliaja arvutamiseks. Väärtust saab igal ajal muuta ja seda kasutatakse ainult tegelike tsükliaegade arvutamiseks.  
13. Klõpsake nuppu Salvesta.


