---
title: " Alushind ja kaubanduslepped"
description: See protseduur juhendab kanalispetsiifiliste müügihinna kaubanduslepete loomisel.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 4830ac553318cfbb3cb74395d1662e74dff75290
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "320416"
---
# <a name="base-price-and-trade-agreements"></a> Alushind ja kaubanduslepped

[!include[task guide banner](../includes/task-guide-banner.md)]

See protseduur juhendab kanalispetsiifiliste müügihinna kaubanduslepete loomisel. Protseduur kasutab demoettevõtte USRT andmeid.

1. Avage Jaemüük ja kaubandus > Hinnad ja allahindlused > Hinnagrupid > Kõik hinnagrupid.
    * Kaubanduslepped määratakse konkreetsetesse kanalitesse hinnagruppide kaudu. Hinnagruppide kasutamine kaubanduslepete määramiseks kanalisse võimaldab kanalispetsiifilist hindade määramist.  
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Hinnagrupid.
4. Sisestage väärtus väljale Nimi.
5. Klõpsake nuppu Salvesta.
6. Sulgege leht.
7. Avage Jaemüük ja kaubandus > Kanalid > Jaemüügikauplused > Kõik jaemüügikauplused.
8. Valige loendist New York.
9. Klõpsake tegevuspaneelil valikut Store (Kauplus).
10. Klõpsake valikut Hinnagrupid.
11. Klõpsake valikut Uus.
12. Klõpsake väljal Price groups (Hinnagrupid) otsingu avamiseks ripploendi nuppu.
13. Otsige loendist ja valige soovitud kirje.
14. Klõpsake nuppu Salvesta.
15. Sulgege leht.
16. Sulgege leht.
17. Avage Jaemüük ja kaubandus > Tooted ja kategooriad > Väljastatud tooted kategooria järgi.
18. Klõpsake loendis valitud real olevat linki.
19. Klõpsake nuppu Redigeeri.
20. Vajutage jaotise Sell (Müük) väljaulatuvat osa.
21. Sisestage väljale Price (Hind) number.
    * Seda hinda kasutatakse, kui kohalduvaid kaubandusleppeid ei leita.  
22. Klõpsake nuppu Salvesta.
23. Klõpsake toimingupaanil suvandit Müük.
24. Klõpsake Create trade agreements (Loo kaubanduslepped).
25. Klõpsake Uus.
26. Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.
27. Valige loendist Retail (Jaemüük).
    * Demoandmetes on Jaemüügi töölehe nimi vaikimisi seotud müügihinnaga. See tähendab, et kõik uued loodud read lülituvad vaikimisi kaubanduslepete kohastele müügihindadele.  
28. Klõpsake valikut Read.
29. Valige väljal Account code (Konto kood) Group (Grupp).
30. Klõpsake väljal Konto valik otsingu avamiseks ripploendi nuppu.
31. Otsige loendist ja valige soovitud kirje.
    * See viib lõpule ühenduse valikute Kanal > Hinnagrupp > Kaubanduslepe vahel.  
32. Sisestage väärtus väljale Item relation (Kauba seos).
33. Sisestage arv väljale Summa valuutas.
34. Märkige ruut Find next (Leia järgmine) või eemaldage sellest märge.
    * Kui valiku Leia järgmine väärtuseks on Jah, jätkab hinnamootor madalama müügihinnaga kohalduvate kaubanduselepete otsimist. Kui valiku Leia järgmine väärtuseks on Ei, lõpetab hinnamootor otsimise ja kasutab kaubanduslepet.  
35. Klõpsake valikut Sisesta.
36. Klõpsake nuppu OK.
37. Sulgege leht.
38. Klõpsake toimingupaanil suvandit Müük.
39. Klõpsake Sales price (Müügihind).

