--- 
title: "Tootmisvoo mudelite määratlemine"
description: "Tootmisvoo mudelid kirjeldavad, kuidas lean manufacturingi töörakkude võimsust arvutatakse ja hoitakse."
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 3da0b5c4fc50136a98017e37b65afea9f8ec7b38
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="define-production-flow-models"></a>Tootmisvoo mudelite määratlemine

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tootmisvoo mudelid kirjeldavad, kuidas lean manufacturingi töörakkude võimsust arvutatakse ja hoitakse. Seetõttu on tootmisvoo mudeli määratlus töörakkude määratluse eeltingimus. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="define-a-production-flow-model"></a>Määratlege tootmisvoo mudel. 
1. Avage Tootmise juhtimine > Häälestamine > Kulusäästlik tootmisvoog > Tootmisvoo mudelid.
2. Klõpsake valikut Uus.
3. Sisestage väljale Tootmisvoo mudel tootmisvoo mudeli ID.
4. Valige suvand väljalt Mudeli tüüp.
    * Mudelitüüpe on kaks: Läbilaskevõime tüüp ja Tundide tüüp. Läbilaskevõime tüübi puhul väljendatakse ja arvutatakse seda tootmisvoo mudelit kasutavate töörakkude võimsust tootekogustes. Tundide tüübi puhul väljendatakse ja arvutatakse seda tootmisvoo mudelit kasutavate töörakkude võimsust tundides. Pange tähele, et seda atribuuti ei saa muuta olemasolevaks tootmisvoo mudeliks. Kui töörakul on võimsuse reserveeringuid, ei saa tootmisvoo mudeli tüüpi muuta.  
5. Saate sisestada päevade arvu EPE tsüklis.
    * Ajavahemik kirjeldab perioodi, millal iga tootmisvoos või töörakus toodetavat osa toodetakse vähemalt üks kord. Mida lühem EPE tsükkel, seda paindlikum on tootmisprotsess. Kui EPE tsükkel = 0, saab kogu nõudluse toota samal päeval. EPE tsüklit kasutatakse säästliku protsessi tööde plaanimiseks. Töö plaanimisel tööraku puhul, mille EPE tsükkel on 5, otsib plaanimisprotsess tööraku võimsust valemiga Tähtaeg – EPE tsükkel (5 päeva enne tähtaega), et toode saaks selle tsükli jooksul valmis. Tootevarude täitmisaeg on tavaliselt suurem kui või võrdne seotud tootmisprotsessi EPE tsükliga.  
6. Valige suvand väljalt Plaanimisperioodi tüüp.
    * Kui töörakul on võimsuse reserveeringuid, ei saa plaanimisperioodi tüüpi muuta. Saate valida antud tööraku jaoks ainult sama perioodi tüübiga tootmisvoo mudeleid.  
7. Sisestage arv väljale Plaanimise ajapiir.
    * Plaanimise ajapiir kirjeldab päevade arvu, millal seotud töörakkude võimsust saab reserveerida. Sisestage päevade arv väljale Plaanimise ajapiir.   Kanbani protsessitöid, mis jäävad sellest perioodist välja, ei plaanita automaatplaanimisega. Plaanimise ajapiir on tavaliselt kahekordne tootmisvoos või töörakus toodetud toodete lao täitmisaeg. EPE tsükkel ei tohi olla pikem kui pool plaanitavast ajapiirist.     
8. Valige suvand väljal Võimsuse puudujäägi reaktsioon.
    * Suvandid on järgmised. Lükka edasi – plaanitud sündmuse kogunõudlus lükatakse edasi järgmisesse saadaoleva jõudlusega tootmispäeva. Tühista – plaanitud sündmuse automaatne plaanimine lõpetatakse ja seotud tööd jäetakse plaanimata.   Lisa taotletud päevale – valitud tööd plaanitakse valitud ajavahemikule. See koormab tööraku antud päevaks üle ja eeldab, et plaanija vaatab toimingu üle ja tegutseb käsitsi.   Jaota saadaolevatele perioodidele – plaanitud sündmuse erinevad tööd jagatakse kõiki saadaolevate tootmispäevade vahel alates esimesest saadaolevast päevast. Minimaalne jaotuskogus on kanban-töö kogus. Jaotus määrab igale piisavalt suure saadaoleva jõudlusega päevale minimaalse plaanimiskoguse (kanban-koguse).  

