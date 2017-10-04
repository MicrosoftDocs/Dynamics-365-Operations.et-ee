---
title: "Tootmistellimuse kulu analüüs"
description: "Selles artiklis käsitletakse kuluanalüüsi, mida saab teha lõpetatud ja jooksvate tootmistellimuste puhul. Saate analüüsida eeldatavaid kulusid ja tegelikke kulusid, kasutades lehte Hinnakalkulatsioon või aruannet Kuluhinnangud ja omahind. Saate vaadata hinnanguliste ja tegelike kulude (ja koguste) teavet iga komponendi rea, protsessitoimingu ja kaudse kulu kohta."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 79634
ms.assetid: ded5da04-f787-49f7-b5e5-75c2a2b92930
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1905749fa8db33b960d082d1e22f11206b400eb0
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017

---

# <a name="production-order-cost-analysis"></a>Tootmistellimuse kulu analüüs

[!include[banner](../includes/banner.md)]


Selles artiklis käsitletakse kuluanalüüsi, mida saab teha lõpetatud ja jooksvate tootmistellimuste puhul. Saate analüüsida eeldatavaid kulusid ja tegelikke kulusid, kasutades lehte Hinnakalkulatsioon või aruannet Kuluhinnangud ja omahind. Saate vaadata hinnanguliste ja tegelike kulude (ja koguste) teavet iga komponendi rea, protsessitoimingu ja kaudse kulu kohta.

Tootmistellimus tegelikud kulud põhinevad materjali ja protsessitoimingute kinnitatud tarbimisel. Materjali, protsessitoimingute ja kaudsete kulude kinnitatud tarbimise üksikasjalikele kannetele pääsete ligi lehel **Tootmise sisestamine**.

## <a name="variance-analysis-for-a-completed-production-order"></a>Lõpetatud tootmistellimuse hälvete analüüsimine
Hälbed kajastavad võrdlust aruandes esitatud tootmistegevuste ja toodetava kauba standardkulude vahel. Hälbed ei kajasta tootmistellimuse kuluhinnangute võrdlust. Aruandes esitatud tootmistegevused hõlmavad materjali tarbimist ja protsessioperatsioone koos nendega seotud kaudseid kuludega ning lõpetatuna kinnitatud kogust. Arvestatakse järgmised hälbe tüübid.

-   Partii suuruse hälve
-   Tootmise koguse hälve
-   Tootmishinna hälve
-   Tootmise asendamise hälve

Järgmisel diagrammil on näidatud neli hälvet, mis selgitavad erinevust tootmistellimuse tegelike kulude ja arvutatud kulude vahel kauba kulukirjes tootmistellimuse lõpetamise ajal. 

![Hälbed, mis selgitavad erinevusi lõpule viidud tootmistellimuses](./media/control.jpg) 

Saate tootmishälbeid analüüsida lehega **Hälve** või aruandega **Tootmishälve**. Kasutage kuvamisvalikuid üksikasjalike hälvete vaatamiseks kauba ja operatsiooniressursi või kulugrupi järgi.. Kulude jaotamise poliitika varude parameetrites määratleb, kas hälbeid jälgitakse kulugruppide alusel. Võite kasutada summeeritud hälvete vaatamiseks ka kuvamisvalikuid **üksik**, **mitmekordne** ja **kokku**. Teave üksikasjalike hälvete kohta võib aidata iga hälbe allikat mõista. Hälvete prognoosimiseks enne tootmistellimuse lõpetamist analüüsige üksikasjalikku teavet, mis on antud aruandes **Kuluhinnangud ja omahind**.

## <a name="cost-analysis-for-current-production-orders"></a>Praeguste tootmistellimuste kuluanalüüs.
Eraldiolevad aruanded kajastavad iga kandetüübi teavet. Kasutage neid aruandeid kinnitatud tootmistegevuste kulude analüüsimiseks. Kuvatakse teave ainult nende jooksvate tootmistellimuste kohta, mille olek on **Alustatud** või**Lõpetatuna kinnitatud**.

-   **Lõpetamata materjalid**− see aruanne koosneb komplekteerimislehe kannetest, mis on praeguste tootmistellimuste alusel määratud kande kuupäevaga kinnitatud. Aruanne näitab komponendi väljastatud kogust ja iga kande kulusummat. Kasutage ühe komponendiüksuse valikukriteeriume. Näiteks võite printida komponendi väljastatud koguse teabe võrreldes kehtivate tootmistellimustega. Väljastatud kogust ei värskendata peamise üksuse puhul lõpetatuks märgitud kogustega. Seetõttu võib lõpetamata toormaterjalide tegelik kogus olla liialdatud.
-   **Lõpetamata töö**− see aruanne kajastab protsessi (või töö) kandeid, mis on praeguste tootmistellimuste alusel määratud kande kuupäevaga kinnitatud. Aruanne näitab tunde, summat ja kogust (nii kvaliteetset kui ka veakogust), mis iga kande kohta esitatakse. See sisaldab ka teavet toimingu numbri, toimingu ID ja operatsiooniressursi kohta. Aruandes kuvatakse ka kõikide kannete koondaeg ja -summa tootmistellimusega seoses ning lõpetatuna kinnitatud kogus.
-   **Töödeldavad kaudsed kulud**− selles aruandes on tootmistellimustega seoses tekkinud kaudsed kulud. Need andmed põhinevad protsessitoimingute ja komponentide kinnitatud tarbimisel määratud kande kuupäeval. Aruandes näidatakse kaudse kulu tüüp (lisatasu või määr), kaudse kulu palgalehe kood ning iga kande kulusumma. Selles aruandes ei anta teavet protsessikaardi või komplekteerimisloendi kande kohta, mis kaudse kulu tekitasid.
-   **Lõpetamata toodangu omahinna arvutamine**− see aruanne loetleb määratud kande kuupäevaga tootmistellimuste ühendatud tarbimismaterjalid, protsessioperatsioonid ja kaudsed kulud.
-   **Pooleliolevad lõpetatud kaubad**− see aruanne loetleb määratud kuupäevaga praegused tootmistellimused lõpetatuna kinnitatud kanded.


<a name="see-also"></a>Vt ka
--------

[Tootmishälvete üldpõhjused](common-sources-of-production-variances.md)



