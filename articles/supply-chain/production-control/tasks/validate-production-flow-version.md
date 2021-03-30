---
title: Tootmisvoo ja versiooni kinnitamine
description: See protseduur kirjeldab, kuidas luua uus tootmisvoog ja esimene versioon lean manufacturingi jaoks.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2bceb5b61fea55c78cb2bb65b8d7cde66679ef01
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254259"
---
# <a name="validate-a-production-flow-and-version"></a>Tootmisvoo ja versiooni kinnitamine

[!include [banner](../../includes/banner.md)]

See protseduur kirjeldab, kuidas luua uus tootmisvoog ja esimene versioon lean manufacturingi jaoks. Eeltingimused: Tuleb määratleda lean manufacturingi tootmisparameetrid ja klassiaja mõõtühikud. Peate määratlema ka Väärtuse voo ja Tootmisgrupi. Tootmisvoogude ja tegevuste kontseptsioonidega tutvumiseks vaadake lean manufacturingi ülevaateid. See protseduur viitab demoandmetes juriidilisele isikule USMF. Eeldusel, et juriidiline isik on seadistatud lean manufacturingi jaoks, võib samas kasutada teisi juriidilisi isikuid.


## <a name="create-a-production-flow"></a>Tootmisvoo loomine
1. Minge jaotisse Tootmise juhtimine > Seadistus > Kulusäästlik tootmisvoog > Tootmisvood.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Nimi.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.
6. Klõpsake loendis valitud real olevat linki.
    * Väärtuse voog on tootmisüksus, mis hõlmab kõiki väärtuse voo tegevusi ja voogusid.   Selles etapis on tootmisüksused piiratud juriidilise isikuga ja muid funktsioone neil pole.  
7. Klõpsake väljal Tootmisgrupp otsingu avamiseks ripploendi nuppu.
8. Klõpsake loendis valitud real olevat linki.
    * Tootmisgrupid võimaldavad tootmisprotsessi jaoks materjali, tööjõu ja lõpetamata toodangu kontode määratlemist. Raamatupidamise konteksti seostamiseks tootmisvooga tuleb valida tootmisgrupp.  
9. Klõpsake nuppu Salvesta.

## <a name="create-a-production-flow-version"></a>Tootmisvoo versiooni loomine
1. Klõpsake vahekaarti Lisa.
2. Sisestage kuupäev ja kellaaeg väljale Aegumiskuupäev.
    * Saate värskendada versiooni aegumiskuupäeva igal ajal ja isegi aktiivsete versioonide puhul. Versiooni aegumiskuupäeva abil saate plaanida versiooni kasutusest kõrvaldamist.  
3. Klõpsake nuppu OK.
4. Märkige loendis valitud rida.
5. Sisestage väärtus väljale Ühik.
6. Valige taktiühik.
7. Sisestage number väljale Keskmine takti aeg.
    * Tootmisvoo versiooni takti juhtimiseks määratlege suunatud keskmine takti aeg.   Takti määratletakse kogusena ajaperioodi kohta.  Selles näiteks on takti aeg 0,2 tundi 10 tk kohta. Kaheksatunnise tööaja puhul vastab see igapäevasele läbilaskevõimele 400 tk.  
8. Sisestage number väljale Kogus tsükli kohta.
9. Laiendage või ahendage jaotist Versiooni üksikasjad.
10. Sisestage number väljale Minimaalne takti aeg.
    * Minimaalne takti aeg peab olema väiksem või sama kui keskmine takti aeg.  
11. Sisestage number väljale Maksimaalne takti aeg.
    * Maksimaalne takti aeg peab olema suurem või sama kui keskmine takti aeg.  
12. Sisestage väljale Tegeliku tsükliaja periood päevade arv
    * Tegeliku tsükliaja periood on tegelikust minutist tagasisuunas koondatud tööde päevade arv tegeliku tsükliaja arvutamiseks. Väärtust saab igal ajal muuta ja seda kasutatakse ainult tegelike tsükliaegade arvutamiseks.  
13. Klõpsake nuppu Salvesta.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]