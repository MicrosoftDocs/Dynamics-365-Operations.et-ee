---
title: Tootmisvoo versiooni loomine
description: See protseduur keskendub uue tootmisvoo versiooni loomisele.
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 115463c57b28e681d4c6bdc227e35272861779aa
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006912"
---
# <a name="create-a-production-flow-version"></a>Tootmisvoo versiooni loomine

[!include [banner](../../includes/banner.md)]

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
    * Valige tootmisvoole tootmisgrupp. Tootmisgrupid võimaldavad tootmisprotsessi jaoks materjali, tööjõu ja lõpetamata toodangu kontode määratlemist. Raamatupidamise konteksti seostamiseks tootmisvooga tuleb valida tootmisgrupp.  
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

