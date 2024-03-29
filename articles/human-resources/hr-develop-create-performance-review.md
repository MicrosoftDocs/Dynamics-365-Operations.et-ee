---
title: Jõudluse ülevaadete loomine
description: Selles artiklis selgitatakse, kuidas luua jõudluse ülevaadet ja kirjeldatakse ülevaate iga jaotise eesmärki.
author: twheeloc
ms.date: 08/26/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EssWorkspace, HcmDiscussionNewDialog, HcmDiscussion, HcmDiscussionChangeSettings, HcmDiscussionAddGoalDialog, HcmTopicCreate, HcmMeasurementDetailDialog, HcmPerfJournalAdd, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae2de087f4e345ba826ddbe8a65f917476bd6894
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872177"
---
# <a name="create-performance-reviews"></a>Jõudluse ülevaadete loomine


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]


Selles artiklis selgitatakse, kuidas luua jõudluse ülevaadet ja kirjeldatakse ülevaate iga jaotise eesmärki. Protseduuri loomisel kasutati demoettevõtte USMF andmeid.

1. Avalehel valige tööruum **Töötaja iseteenindus**.
2. Uue ülevaate loomiseks valige **Uus ülevaade**.
3. Väljale **Ülevaate tüüp** sisestage või valige väärtus.
4. Väljale **Jõudlusperiood** sisestage või valige väärtus.
5. Väljale **Lõppkuupäev** sisestage kuupäev.
6. Valige nupp **OK**. Ülevaate saab luua ka malli põhjal. See on ülevaate loomiseks parim viis, kuna igas jaotises on teave, mida ülevaate alustamiseks vajate.  
7. Saate kuvada või peita vahekaarte, näiteks manuste vahekaarti.

    1. Valige toimingupaanil dialoogimenüü avamiseks **Kuva jaotised**.
    1. Valige välja **Kuva manused** väärtuseks **Jah** või **Ei**, et kuvada või peita manuste vahekaart.
    1. Valige käsk **Salvesta**.

8. Eesmärgi lisamiseks valige **Lisa ülevaatele eesmärk**. Kui olete lõpetanud, valige **OK**.
9. Valige **Lisa kompetentsus**, et avada rippdialoog.
10. Sisestage väärtus väljale **Pealkiri**.
11. Väljale **Kirjeldus** sisestage `Increase customer skills by working with the support team`.
12. Valige nupp **OK**.
13. Valige **Ahenda kõik**.
14. Valige **Laienda kõik**.
15. Valige **Lisa kommentaar**.
16. Valige **Sisesta**.
17. Valige vahekaart **Mõõtmed**.
18. Valige **Lisa mõõtmine**, et avada dialoogimenüü.
19. Väljale **Mõõtmed** sisestage või valige väärtus.
26. Väljale **Sihtsumma** sisestage arv.
20. Valige nupp **OK**.
21. Valige vahekaart **Toimingud**.
22. Valige **Lisa**.
23. Sisestage väärtus väljale **Pealkiri**.
24. Sisestage väärtus väljale **Kirjeldus**.
25. Väljale **Alguskuupäev** sisestage kuupäev.
26. Väljale **Lõpetamiskuupäev** sisestage kuupäev.
27. Valige väärtus **Jah** väljal **Arenguplaan**.
28. Sisestage väärtus väljale **Märksõnad**.
29. Valige käsk **Salvesta**.
30. Valige vahekaart **Hinnangud**.  

    - Kiirkaardi **Hinnangu üksikasjad** abil on töötajatel võimalik ennast hinnata ja juhatajal võimalik hinnata töötajat. Kaalude kasutamisel arvutatakse tulemuste kaalumisväärtus automaatselt.  
    - Selle jaotise vaatamiseks lubage parameetrisätted töötaja hinnangute kuvamiseks inimressursside **jagatud parameetrite** lehel.  

31. Valige vahekaart **Nõusolekud**. Kui ülevaates kasutatakse töövoogu, ilmuvad nõusolekud ainult siis, kui töövoog on lõpetatud. Kui töövoogu ei kasutata, on siin kirjas nii töötaja kui ka juht. **Nõutav** ruut on märgitud **Väljalogimised** jaoks valitud ülevaatuse tüübi sätete põhjal.  
32. Valige vahekaart **Üldine**.

    - Jõudlusperiood loob alguse ja lõpu vaikekuupäevad. Neid kuupäevi saab muuta.  
    - Olekud juhivad juurdepääsu ülevaatusele. Olek **Alustamata** lubab kõigil ülevaadet redigeerida. Olek **Pooleli** lubab ainult töötajal ülevaadet vaadata ja redigeerida. Olek **Ülevaatuseks valmis** võimaldab ainult juhil ülevaatust vaadata ja muuta. **Lõplik ülevaatuse** olek võimaldab nii töötajal kui ka juhatajal ülevaadet vaadata ja redigeerida, kui ülevaatuse tüübis on valitud suvand **Luba redigeerimine lõplikus ülevaates**. Olekud **Lõpetatud** ja **Tühistatud** muudavad ülevaatuse kirjutuskaitstuks. Kui ülevaatuse väärtus on **Tagasi lükatud** ja see saadetakse töövõtjale tagasi, siis saavad nii töötaja kui juht teha vajalikke parandusi, et töötaja saaks selle uuesti esitada.

33. Sisestage väärtus väljale **Ülevaade**.
34. Valige vahekaart **Ülevaade**. Kui ülevaade liigub olekute vahel, saavad töötaja ja juhataja lisada kommentaare iga eesmärgi või kompetentsuse kohta.  
35. Valige vahekaart **Nõusolekud**. Töötaja ja juhataja saavad anda ülevaate nõusoleku. Kui kõik nõutud nõusolekud on lõpetatud, muudetakse olek **Lõpetatuks** ja enam ei saa muudatusi teha.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
