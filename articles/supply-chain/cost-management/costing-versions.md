---
title: Ülevaade kuluversioonidest
description: Selles artiklis antakse teavet kuluversioonide, nende haldamise ja nendesse kaastavate andmetüüpide kohta. Kuluversiooni peaeesmärk hõlmab kaupade, kulukategooriate kulukirjeid ja kaudsete kuluarvutuste arvutusvalemeid.
author: AndersGirke
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "54532"
- intro-internal
ms.assetid: cd239da5-f434-4d1b-8196-5414c888d76d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27ad1f1d8ae60eef5607bafb9aaf9604784099e4
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983093"
---
# <a name="costing-versions-overview"></a>Ülevaade kuluversioonidest

[!include [banner](../includes/banner.md)]

Selles artiklis antakse teavet kuluversioonide, nende haldamise ja nendesse kaastavate andmetüüpide kohta. Kuluversiooni peaeesmärk hõlmab kaupade, kulukategooriate kulukirjeid ja kaudsete kuluarvutuste arvutusvalemeid.

Kuluversioon saab pakkuda üht või mitut eesmärki, olenevalt kuluversioonis olevatest andmetest. Kuluversiooni peaeesmärk hõlmab kaupade, kulukategooriate kulukirjeid ja kaudsete kuluarvutuste arvutusvalemeid. Kuluversioon võib sisaldada standardsete kulukirjete kogumit või planeeritud kulukirjete kogumit, mis põhinevad kuluversioonile määratud kulutüübil.

## <a name="costing-versions-for-standard-or-planned-costs"></a>Standardkulude või plaanitud kulude kuluversioonid
### <a name="standard-costs"></a>Standardkulud

Kuluversioon võib toetada standardkulu laomudelit kaupade puhul, mille kuluversioon sisaldab kaupade ja tootmisprotsesside kohta standardsete kulukirjete kogumit. Tootmisprotsesside kuluandmed esitatakse protsessitoimingute puhul kulukategooriatena ja tootmise üldkulude arvutusvalemitena.

### <a name="planned-costs"></a>Plaanitud kulud

Kuluversioon võib sisaldada kaupade ja tootmisprotsesside plaanitud kulukirjete kogumit. Plaanitud kulusid sisaldavat kuluversiooni kasutatakse sageli kuluarvutussimulatsioonide toetamiseks, nt näiteks simulatsioonide puhul, mille käigus on näha ostetava materjali või tootmisprotsessi maksumuse muutumise mõju toodetud kaupade arvutatud kuludele. Plaanitud kulude kauba kulukirjeid saab kasutada ka tegelike kulude laomudeli toetamiseks, esitades kauba maksumuse algväärtused. Need väärtused sisaldavad toodetud kaupade plaanitud kulude arvutust.

## <a name="entering-costs"></a>Kulude sisestamine
Kulukirjete andmete haldamine kuluversioonis hõlmab ostetud kaupade ja laoalade vahel üle viidud kaupade kulude sisestamist. Tootjatele mõeldud lisaandmete haldus hõlmab protsessitoimingutega seotud kulukategooriate sisestamist, tootmise üldkulusid kajastavate kaudsete kulude arvutusvalemite sisestamist ja toodetud kaupade kulude arvutamist. 

Kuluversiooni kauba kuluandmed sisaldavad vähemalt ühte kulukirjet iga kauba kohta. Kauba kulukirje esmakordsel sisestamisel on sellel olek **Ootel** ja plaanitav jõustumiskuupäev. Kauba kulukirje aktiveerimisel määratakse olekuks **Aktiivne** ja jõustumiskuupäevaks määratakse aktiveerimiskuupäev. Erinevad kauba kulukirjed võivad kajastada erinevaid laoalasid, jõustumiskuupäevi või olekuid. Kui arvutate toodetavate kaupade kulusid tulevase kuupäeva kohta, kasutatakse koosluse arvutuses kulukirjeid, millel on vastav jõustumiskuupäev, olenemata sellest, kas olek on **Ootel** või **Aktiivne**. Kauba praegust aktiivset kulukirjet kasutatakse tootmistellimuse kulude ja hindamiseks ning laokannete väärtuse arvestamiseks standardse kulu laomudeli põhjal. Kulukategooriate kulukirjete ja kaudsete kulude kalkulatsioonivalemite haldus sarnaneb kauba kulukirjete haldusele. 

Kaks blokeerivat kuluversiooni poliitikat määravad, kas ootel kulusid saab hallata ja kas ootel kulusid saab aktiveerida. Kasutage blokeerimispoliitikaid kuluversiooni kulukirjete andmehalduse lubamiseks ja seejärel nende takistamiseks. 

Kuluversioon võib mallkoosluse kalkulatsiooni eesmärkidel sisaldada ka kauba müügihindade või ostuhindade andmeid.

## <a name="item-sales-prices-for-bom-calculations"></a>Kauba müügihinnad koosluse arvutuste jaoks
Müügihindade andmete kaasamise peamine põhjus on säilitada toodetud kauba arvutatud müügihind. Arvutatud müügihinda saab seejärel analüüsida, et määrata, kuidas komponendid, protsessioperatsioonid ja üldkulud maksumust ja müügihinda mõjutavad. 

Teine põhjus müügihindade andmete kaasamiseks on määratleda koostiskaupade müügihinna kirjed. Seejärel saab neid kirjeid kasutada toodetavate kaupade müügihinna arvutamiseks. Esmalt tuleb määrata müügihinna mudel, mis on manustatud koosluse arvutusgruppi, ja määrata koosluse arvutusgrupp ostetud kaupadele. Seejärel, kui teete koosluse arvutusi, mis kasutavad plaanitud kulusid, tuleb valida koosluse arvutusgrupi omahinna mudel. 

Vastasel korral kasutatakse müügihinna kirjeid ainult viiteteabena, olenemata sellest, kas kirjed on käsitsi sisestatud või arvutatud. Kauba müügihinna kirje aktiveerimisega saate uuendada kauba baasmüügihinda. Kuid baasmüügihind pole laoalapõhine ja seda saab käsitsi alistada. Kauba baasmüügihinda kasutatakse müügitellimuste ja müügipakkumiste vaikemüügihinnana.

## <a name="item-purchase-prices-for-bom-calculations"></a>Kauba ostuhinnad koosluse arvutuste jaoks
Ostuhinna andmete lubamise peamine eesmärk on koostiskaupade ostuhinna kirjete määramine, et neid kirjeid saaks siis kasutada toodetud kaupade kulude arvutamiseks. Kauba ostuhinna kirjed tuleb sisestada käsitsi. 

Ostuhinna sisu lubamiseks tuleb esmalt määratleda koosluse arvutusgrupp, mis sisaldab kauba ostuhinna omahinna mudelit, ja määrata see koosluse arvutusgrupp ostetud kaupadele. Seejärel saate kasutada koosluse kalkulatsioonigrupi omahinna mudelit, kui teete koosluse arvutusi, milles kasutatakse plaanitud kulusid toodetud kaupade müügihinna arvutamiseks. 

Viiteteabena kasutatakse ka kaupade ostuhinna kirjeid. Kauba ostuhinna kirje oleku muutmisega olekust **Ootel** olekusse **Aktiivne** saate uuendada kauba baasostuhinda. Kuid baasostuhind pole laoalapõhine ja seda saab käsitsi alistada. Kauba baasostuhinda kasutatakse ostutellimustes vaikeostuhinnana.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]