---
title: Tootmisprotsessis kasutatud kulukategooriad
description: See artikkel annab teavet protsesse kasutavate tootmiskeskkondade puhul kehtivate kulukategooriate kohta.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjCategory, RouteCostCategoryPrice
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78153
ms.assetid: a3fdc76c-0a27-4723-b1c7-4322f707d89e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 12e712e0a28ada0716d35b7105fb20c354d1bc18
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="cost-categories-used-in-production-routing"></a>Tootmisprotsessis kasutatud kulukategooriad

[!include[banner](../includes/banner.md)]


See artikkel annab teavet protsesse kasutavate tootmiskeskkondade puhul kehtivate kulukategooriate kohta.

Kulukategooriad rakenduvad protsessi kasutatavatele tootmiskeskkondadele. Need määratakse operatsiooniressurssidele ja protsessi toimingutele tunnikulude ja kulu osade segmentimise eesmärkidel toodetud kauba kalkuleeritud kuludes. Kulukategooriatele määratud kulugrupid liigitavad toodetavad kulu osad operatsiooniressursside ja tegevuse tüübi (nt häälestus ja käitusaeg) alusel. Kulugrupi määramise spetsiifilisus pakub protsessiteabel põhinevat tootmise üldkulude kalkuleerimist. 

**Märkus:** tootmiskeskkondades tuntakse kulukategooriaid mitme teise nime alusel (nt palgatariifi koodid või masina määra koodid). 

Igal kulukategoorial on seotud kulukirjed ja kulugrupp. Erinevad kulukategooriad on vajalikud erinevate tootmiseesmärkide jaoks.

-   Määrake erinevad tunnikulud olenevalt operatsiooniressursist. Näiteks võivad kulud erineda mitmesugust tüüpi tööoskuste, masinate või tootmisrakkude puhul.
-   Määrake erinevad tunnikulud protsessi toiminguga seotud häälestus- või käitusajale.
-   Määrake operatsiooniressursi kulud tunnikulude asemel väljundi koguse alusel, nt tükipalga määr tööjõu eest maksmiseks.
-   Pakkuge kulupanuste kulugrupi segmentimist toodetud kauba arvutatud kuluks. Näiteks saate segmentida tööjõu- ja masinakulusid.
-   Esitage üldkulude kalkulatsiooni valemite kulugrupi alus, nt tööjõu- ja masinapõhiste üldkulude või käitusajaga seotud üldkulude valemid.

Kulukategooria saab määrata protsessitoimingu häälestusajale, töötlemisajale ja kogusele. Kui näiteks kulud või kulugrupi segmentimine kulud on häälestuse ja töötlemise aja vahel erinevad, peab erinevad kulukategooriad neile määratlema ja määrama häälestuse ja töötlemise ajale. Kulukategooriate valikuline kasutus häälestusaja, töötlemisaja ja koguse puhul määratletakse toimingule määratud protsessigrupi alusel. Kulukategooriate määramine ajale ja kogusele võib lehel **Tootmise juhtimise parameetrid** määratletud ettevõtteüleste poliitikate alusel kohustuslik olla. 

Igal kulukategoorial on talle määratud kulud, mis põhinevad kuluversiooni kulukirjete definitsioonil. Lehel **Kulukategooria hind** saab määratleda konkreetse kuluarvutuse versiooni ja laoala kulukirjed. Kulukategooria kulukirje esmakordsel sisestamisel on sellel olek **Ootel** ja ettenähtud jõustumiskuupäev. Kauba kulukirje aktiveerimisel määratakse olekuks **Praegu aktiivne** ja jõustumiskuupäevaks määratakse aktiveerimiskuupäev. Erinevad kauba kulukirjed võivad kajastada erinevaid laoalasid, jõustumiskuupäevi või olekuid. Tulevase või olnud kuupäevaga koosluse kalkulatsioonid kasutavad kulukirjeid vastava kehtiva kuupäevaga. Praegust aktiivset kulukirjet kasutatakse tootmistellimuse kulude hindamiseks ja kinnitatud aja hindamiseks tootmistellimuse suhtes. 

Kulukategooria kulukirje võib olla laoalapõhine või ettevõtteülene. Kulukirje muutmiseks laoalapõhiseks tuleb määrata sellele laoala. Vastasel juhul näitab tühi väärtus, et kulukirje rakendub ettevõttes kõikidele laoaladele. Kuna kulud võivad näiteks laoalade vahel erineda, peab kulukirjed laoalapõhistena määratlema. 

Protsessi toiming pärib tavaliselt kulukategooriad, mis on operatsiooniressursile või koondtoimingutele määratud. Tootmistellimuse loomisel kajastavad tootmisprotsessi protsessi toimingud valitud protsessi versiooni. Te saate tootmisprotsessi toimingutele määratud kulukategooriad tühistada. 

Mõnda tüüpi tootmistöö võib rakenduda projekti ajaprognoosidele ja aruandlusele. Sellisel juhul on tootmise ja projekti jaoks vaja kulukategooriat. Projektiga seostuv lisateave peab olema määratletud, kui kulukategooria on projektides kasutamiseks lipuga märgitud.




