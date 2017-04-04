---
title: "Ressursi võimalused"
description: "Selles artiklis antakse teavet ressursivõimaluste kohta. Võimsus on operatsiooniressursi võime konkreetset tegevust sooritada. Artiklis selgitatakse, kuidas võimalusi ja seotud mõisteid, näiteks oskustaset ning prioriteeti, kasutatakse tegevuse jaoks sobilike ressursside valimiseks."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WrkCtrCapability, WrkCtrTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 29961
ms.assetid: 30e38233-2a64-4070-911f-8ffd78dd8281
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4463ca8e11115eb83323716faa4ed6b38937a3e4
ms.lasthandoff: 03/31/2017


---

# <a name="resource-capabilities"></a>Ressursi võimalused

Selles artiklis antakse teavet ressursivõimaluste kohta. Võimsus on operatsiooniressursi võime konkreetset tegevust sooritada. Artiklis selgitatakse, kuidas võimalusi ja seotud mõisteid, näiteks oskustaset ning prioriteeti, kasutatakse tegevuse jaoks sobilike ressursside valimiseks.

Võimsus on operatsiooniressursi võime konkreetset tegevust sooritada. Operatsiooniressursile võib olla määratud mitu võimsust ja võimsuse saab määrata mitmele ressursile. Saate ressurssidele ajutiselt võimsusi määrata, määratledes võimsuse määramisele algus- ja aegumiskuupäeva. Kui ressursi võimsus aegub, ei saa ressurssi ajastada projekti ega tootmise jaoks, mille puhul võimsus on nõutav. Aegunud võimsust saab uuendada. Saate võimsused kustutada, eeldades, et need ei ole aktiivse tootmistellimuse protsessi seoses ega tootmisprotsessi osa. Üldiselt olge võimsuste kustutamisel ettevaatlik. Selle asemel korrigeerige võimsusega ressursside aegumiskuupäeva. Võimsusi saab määrata igat tüüpi ressurssidele: tööriist, hankija, masin, asukoht, süsteemiteenus või inimressurss.

## <a name="level"></a>Tase
Mitmel ressursil on tihti sama funktsionaalne võimsus, kuid erinevad oskustasemed (nt tugevus, töötlemiskiirus või täpsus). Seega kui määrate ressursile võimsuse, saate määrata väärtuse **Tase**. Tase on lihtne numbriline väärtus. Kui määrate, et võimsus on tootmisprotsessi ressursi nõue, saate võimsusele määrata ka väärtuse **Minimaalne vajalik tase**. Plaanimismootor valib siis ainult need ressursid, millel on nõutav võimsus tasemel, mis on ressursi nõuetes määratud minimaalse tasemega võrdne või ületab selle.

## <a name="priority"></a>Prioriteet
Sama võimsusega operatsiooniressurssidele saab määrata prioriteedi. Seejärel, mitu ressurssi on võimeid, mis vastavad sõiduplaani nõuete vajalikul tasemel, kui on vaba tootmisvõimsust, ajastamise mootoriga saate valida need vahendid. Kui **prioriteet** valitud selle **esmajoones arvutitootja valik** kohta välja on **planeerimise parameetreid** lehekülg, ressurss, mis on kõrgeim prioriteet (madalaim väärtus on **prioriteet** välja) valitakse esimene planeerimisel.

## <a name="resource-requirements"></a>Ressursi nõuded
Kui määratlete tootmisprotsessile ressursinõudeid, saate määrata nõuetena ühs või mitu võimsust. Tootmise plaanimise ajal vastendatakse protsessi operatsiooni ressursinõuetes määratletud võimsused ressurssidele määratletud võimsustega. Valitakse nõudeid rahuldavate võimsustega ressursid. Kui mitmel ressursil on sama funktsionaalne võimsus, kuid erinevad oskustasemed (nagu tugevus, töötlemiskiirus või täpsus), saate määratleda mitu võimsust või kasutada võimsustaset, et kvalifitseerida ressursi võimsust. Siin on näide.

-   Protsessi puhul on puurimisprotsessi ajaks määratud 10 ühikut tunnis, kuid nõue ise on määratletud kui Puurimine.
-   Teil on puurimismasinad M1 ja M2.
-   Puurimisvõimsus määratakse mõlemale ressursile, masinale M1 ja masinale M2.
-   Masin M1 suudab puurida kaks ühikut tunnis ja masin M2 11 ühikut tunnis.

Selles näites võib plaanimismootor valida mõlemad masinad, sest mõlemad täidavad võimsuse põhinõude (Puurimine). Kuid masin M1 suudab puurida ainult kaks ühikut tunnis. Kuna see määr on palju väiksem kui 10 ühikut tunnis, mis on protsessile määratud, põhjustab masin M1 valimisel tootmisprobleeme. On kaks võimalust selle probleemi lahendamiseks ja tagamaks, et valitakse hoopis masin M2.

-   Looge kaks eraldi võimsust: Aeglane puurimine ja Kiire puurimine. Määratlege Aeglane puurimine puurimisena, mille protsessiaeg on üks kuni üheksa ühikut tunnis. Määratlege Kiire puurimine puurimisena, mille puurimisprotsessiaeg on 10 kuni 19 ühikut tunnis. Seejärel määrata kohapeal M1 kiire puurimine võime ja määrata M2 masina kiire puurimine võime. Lõpuks muutus ressursi võime nõue liinil kiire puurimine. Plaanimismootor valib seejärel õige masina (M2).
-   Kasutage võimsustaset, et kvalifitseerida puurimise võimsus, mis on määratud puurimismasinatele. Määrata M1 masin on puurimine võime 2.0 tasemel ja et M2 masin on võimeline puurimine 11,0 tasandil. Määrake, et 10,0 on vajalik puurimine võime nõue liinil. Plaanimismootor määrab siis, et ainult masin M2 täidab ressursinõuded.

## <a name="competencies-for-human-resources"></a>Inimressursside pädevused
Kui teil on **Inimressursid** tüüpi operatsiooniressursid, mis on seotud töötajatega inimressurssidega, saate tootmisprotsessi jaoks ressursinõuete määratlemisel ära kasutada ka töötajate pädevusi. Teisisõnu, saate määrata nõudeid ka kindlate oskuste, kursuste, sertide või tiitlite kohta. Plaanimismootor saab siis valida ressursid, mis on seotud töötajatega, ja valik põhineb töötajate pädevustel. Pädevused seadistatakse lehel Inimressursid, mitte lehel **Ressursi võimsused**. Kui olete määratlenud oskusi, kursused, sertifikaatide või pealkirjade järele, tuleb kasutada inimressursse ja link iga ressurss ning **inimressursside** tüübile vastavale töötajale. Kui kasutate inimressursside funktsioone, saate määratleda võimete kohta ning **ressursi võimalusi** leht, mis meenutavad takistamist või töötajate pädevust. Kuid leht **Ressursi võimsused** ei sisalda funktsionaalsust, mis on nõutav oskuste, kursuste, sertide või tiitlite säilitamiseks.


