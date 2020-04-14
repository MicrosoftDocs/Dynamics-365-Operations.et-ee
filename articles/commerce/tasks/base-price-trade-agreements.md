---
title: " Alushind ja kaubanduslepped"
description: See protseduur juhendab kanalispetsiifiliste müügihinna kaubanduslepete loomisel.
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 022db9365f25c1d3e387870dd9d173077d864b3d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141518"
---
# <a name="base-price-and-trade-agreements"></a> Alushind ja kaubanduslepped

[!include [banner](../includes/banner.md)]

See protseduur juhendab kanalispetsiifiliste müügihinna kaubanduslepete loomisel. Protseduur kasutab demoettevõtte USRT andmeid.

1. Avage **Navigeerimispaanil** jaotis **Moodulid > Jaemüük ja kaubandus > Hinnakujunduse ja allahindluse haldus > Hinnagrupid >Kõik hinnagrupid**. Kaubanduslepped määratakse konkreetsetesse kanalitesse hinnagruppide kaudu. Hinnagruppide kasutamine kaubanduslepete määramiseks kanalisse võimaldab kanalispetsiifilist hindade määramist.  
2. Klõpsake valikut **Uus**.
3. Väljale **Hinnagrupid** tippige väärtus.
4. Sisestage väärtus väljale **Nimi**.
5. Klõpsake valikut **Salvesta**.
6. Sulgege leht.
7. Avage **Navigatsioonipaneelil** suvand **Moodulid > Jaemüük ja kaubandus > Kanalid > Kauplused > Kõik kauplused**.
8. Valige loendist New York.
9. Toimingupaanil klõpsake **Kauplus**.
10. Klõpsake **Hinnagrupid**.
11. Klõpsake valikut **Uus**.
12. Väljal **Hinnagrupid** klõpsake rippmenüü nuppu, et avada otsing.
13. Otsige loendist ja valige soovitud kirje.
14. Klõpsake valikut **Salvesta**.
15. Sulgege leht.
16. Sulgege leht.
17. Paanil **Navigeerimispaan** avage **Moodulid > Jaemüük ja kaubandus > Tooted ja kategooriad > Väljastatud tooted kategooria alusel**.
18. Klõpsake loendis valitud real olevat linki.
19. Klõpsake valikut **Redigeeri**.
20. Laiendage vahekaart **Müük**.
21. Väljale **Hind** sisestage arv. Seda hinda kasutatakse, kui kohalduvaid kaubandusleppeid ei leita.  
22. Klõpsake valikut **Salvesta**.
23. Klõpsake paanil **Tegevuspaan** nuppu **Müük**.
24. Klõpsake **Loo kaubanduslepe**.
25. Klõpsake valikut **Uus**.
26. Klõpsake väljal **Nimi** otsingu avamiseks ripploendi nuppu.
27. Valige loendist **Kaubandus**. Demoandmetes on **Kaubanduse** töölehe nimi vaikimisi seotud **Müügihinnaga**. See tähendab, et kõik uued loodud read lülituvad vaikimisi kaubanduslepete kohastele müügihindadele.  
28. Klõpsake paanil **Tegevuspaan** valikut **Read**.
29. Väljal **Konto kood** valige 'Grupeeri'.
30. Klõpsake väljal **Konto valik** otsingu avamiseks ripploendi nuppu.
31. Otsige loendist ja valige soovitud kirje. See viib lõpule ühenduse valikute Kanal > Hinnagrupp > Kaubanduslepe vahel.  
32. Väljale **Kauba seos** tippige väärtus.
33. Väljale **Summa valuutas** sisestage arv.
34. Vahekaardil **Üksikasjad** märkige või eemaldage märge märkeruudust **Leia järgmine**. Kui suvandi **Leia järgmine** väärtus on 'Jah', jätkab hinnakujunduse mootor kohaldatavate madalam müügihinnaga kaubanduslepete otsimist. Kui suvandi **Leia järgmine** väärtus on 'Ei', lõpetab hinnakujunduse mootor otsingu ja kasutab seda kaubanduslepet.  
35. Klõpsake käsku **Sisesta**.
36. Klõpsake valikut **OK**.
37. Sulgege leht.
38. Klõpsake paanil **Toimingupaan** nuppu Müük.
39. Klõpsake valikut **Müügihinnad**.

