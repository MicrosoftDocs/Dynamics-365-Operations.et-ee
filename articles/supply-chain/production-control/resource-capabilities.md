---
title: "Ressursi võimalused"
description: "Selles artiklis antakse teavet ressursivõimaluste kohta. Võimsus on operatsiooniressursi võime konkreetset tegevust sooritada. Artiklis selgitatakse, kuidas võimalusi ja seotud mõisteid, näiteks oskustaset ning prioriteeti, kasutatakse tegevuse jaoks sobilike ressursside valimiseks."
author: sorenva
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WrkCtrCapability, WrkCtrTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 29961
ms.assetid: 30e38233-2a64-4070-911f-8ffd78dd8281
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 533faf78e4cc9a091d64f7c6a0f82d14158710c8
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="resource-capabilities"></a>Ressursi võimalused

[!INCLUDE [banner](../includes/banner.md)]

Selles artiklis antakse teavet ressursivõimaluste kohta. Võimsus on operatsiooniressursi võime konkreetset tegevust sooritada. Artiklis selgitatakse, kuidas võimalusi ja seotud mõisteid, näiteks oskustaset ning prioriteeti, kasutatakse tegevuse jaoks sobilike ressursside valimiseks.

Võimsus on operatsiooniressursi võime konkreetset tegevust sooritada. Operatsiooniressursile võib olla määratud mitu võimsust ja võimsuse saab määrata mitmele ressursile. Saate ressurssidele ajutiselt võimsusi määrata, määratledes võimsuse määramisele algus- ja aegumiskuupäeva. Kui ressursi võimsus aegub, ei saa ressurssi ajastada projekti ega tootmise jaoks, mille puhul võimsus on nõutav. Aegunud võimsust saab uuendada. Saate võimsused kustutada, eeldades, et need ei ole aktiivse tootmistellimuse protsessi seoses ega tootmisprotsessi osa. Üldiselt olge võimsuste kustutamisel ettevaatlik. Selle asemel korrigeerige võimsusega ressursside aegumiskuupäeva. Võimsusi saab määrata igat tüüpi ressurssidele: tööriist, hankija, masin, asukoht, süsteemiteenus või inimressurss.

## <a name="level"></a>Tase
Mitmel ressursil on tihti sama funktsionaalne võimsus, kuid erinevad oskustasemed (nt tugevus, töötlemiskiirus või täpsus). Seega kui määrate ressursile võimsuse, saate määrata väärtuse **Tase**. Tase on lihtne numbriline väärtus. Kui määrate, et võimsus on tootmisprotsessi ressursi nõue, saate võimsusele määrata ka väärtuse **Minimaalne vajalik tase**. Plaanimismootor valib siis ainult need ressursid, millel on nõutav võimsus tasemel, mis on ressursi nõuetes määratud minimaalse tasemega võrdne või ületab selle.

## <a name="priority"></a>Prioriteet
Sama võimsusega operatsiooniressurssidele saab määrata prioriteedi. Kui mitmel ressursil on võimed, mis rahuldavad nõutaval tasemel planeerimise nõudeid, ja on vaba võimsust, siis saab plaanimismootor valida nende ressursside seast. Kui lehe **Parameetrite planeerimine** väljal **Esmase ressursi valik** on valitud **Prioriteet**, valitakse plaanimise ajal esmalt ressurss, millel on kõrgeim prioriteet (madalaim numbriline väärtus väljal **Prioriteet**).

## <a name="resource-requirements"></a>Ressursi nõuded
Kui määratlete tootmisprotsessile ressursinõudeid, saate määrata nõuetena ühs või mitu võimsust. Tootmise plaanimise ajal vastendatakse protsessi operatsiooni ressursinõuetes määratletud võimsused ressurssidele määratletud võimsustega. Valitakse nõudeid rahuldavate võimsustega ressursid. Kui mitmel ressursil on sama funktsionaalne võimsus, kuid erinevad oskustasemed (nagu tugevus, töötlemiskiirus või täpsus), saate määratleda mitu võimsust või kasutada võimsustaset, et kvalifitseerida ressursi võimsust. Siin on näide.

-   Protsessi puhul on puurimisprotsessi ajaks määratud 10 ühikut tunnis, kuid nõue ise on määratletud kui Puurimine.
-   Teil on puurimismasinad M1 ja M2.
-   Puurimisvõimsus määratakse mõlemale ressursile, masinale M1 ja masinale M2.
-   Masin M1 suudab puurida kaks ühikut tunnis ja masin M2 11 ühikut tunnis.

Selles näites võib plaanimismootor valida mõlemad masinad, sest mõlemad täidavad võimsuse põhinõude (Puurimine). Kuid masin M1 suudab puurida ainult kaks ühikut tunnis. Kuna see määr on palju väiksem kui 10 ühikut tunnis, mis on protsessile määratud, põhjustab masin M1 valimisel tootmisprobleeme. On kaks võimalust selle probleemi lahendamiseks ja tagamaks, et valitakse hoopis masin M2.

-   Looge kaks eraldi võimsust: Aeglane puurimine ja Kiire puurimine. Määratlege Aeglane puurimine puurimisena, mille protsessiaeg on üks kuni üheksa ühikut tunnis. Määratlege Kiire puurimine puurimisena, mille puurimisprotsessiaeg on 10 kuni 19 ühikut tunnis. Seejärel määrake masinale M1 võimsus Aeglane puurimine ja masinale M2 võimsus Kiire puurimine. Lõpuks muutke protsessi ressursi võimsusnõudeks Kiire puurimine. Plaanimismootor valib seejärel õige masina (M2).
-   Kasutage võimsustaset, et kvalifitseerida puurimise võimsus, mis on määratud puurimismasinatele. Täpsustage, et masinal M1 on puurimisvõimsus tasemel 2,0, ja et masinal M2 on puurimisvõimsus tasemel 11,0. Seejärel täpsustage, et 10,0 on miinimumtase, mis on nõutav protsessi puurimisvõimsuse nõuetes. Plaanimismootor määrab siis, et ainult masin M2 täidab ressursinõuded.

## <a name="competencies-for-human-resources"></a>Inimressursside pädevused
Kui teil on **Inimressursid** tüüpi operatsiooniressursid, mis on seotud töötajatega inimressurssidega, saate tootmisprotsessi jaoks ressursinõuete määratlemisel ära kasutada ka töötajate pädevusi. Teisisõnu, saate määrata nõudeid ka kindlate oskuste, kursuste, sertide või tiitlite kohta. Plaanimismootor saab siis valida ressursid, mis on seotud töötajatega, ja valik põhineb töötajate pädevustel. Pädevused seadistatakse lehel Inimressursid, mitte lehel **Ressursi võimsused**. Kui määratlete oskused, kursused, serdid või tiitlid ressursinõuetena, peate kasutama funktsiooni Inimressursid ja siduma iga **Inimressursid** tüüpi ressursi vastava töötajaga. Kui te ei kasuta funktsiooni Inimressursid, saate määratleda võimsused lehel **Ressursi võimsused**, mis sarnaneb funktsiooni Inimressursid pädevustega või dubleerib neid. Kuid leht **Ressursi võimsused** ei sisalda funktsionaalsust, mis on nõutav oskuste, kursuste, sertide või tiitlite säilitamiseks.




