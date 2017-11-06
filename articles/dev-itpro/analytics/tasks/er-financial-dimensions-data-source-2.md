--- 
title: Elektroonilise aruandluse (ER) mudelite vastendamine finantsdimensioonide kasutamiseks andmeallikana
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a3eafa7b66dcc0c2481d7eeaf98bed7f58e4be33
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="map-models--to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a>Elektroonilise aruandluse (ER) mudelite vastendamine finantsdimensioonide kasutamiseks andmeallikana

[!include[task guide banner](../../includes/task-guide-banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana. Neid toiminguid saab teha igas ettevõttes.

Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (1. osa: andmemudeli koostamine).


## <a name="add-required-data-sources-to-model-mapping"></a>Vajalike andmeallikate lisamine mudelivastendusele
1. Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.
2. Valige puult Finantsdimensioonide näidismudel.
3. Klõpsake valikut Kujundaja.
4. Klõpsake suvandit Mudeli vastendamine andmeallikaga.
5. Klõpsake valikut Uus.
6. Tehke väljal Definitsioon valik Kirje.
7. Tippige Dimensioonide andmete vastendamine väljale Nimi.
8. Tippige Dimensioonide andmete vastendamine väljale Kirjeldus.
9. Klõpsake nuppu Salvesta.
10. Klõpsake valikut Kujundaja.
11. Valige puul suvand „Dynamics 365 for Operations\tabel“.
12. Klõpsake suvandit Juure lisamine.
13. Sisestage väljale Nimi suvand Ettevõte.
14. Sisestage väljale Tabel suvand CompanyInfo.
15. Klõpsake nuppu OK.
16. Valige puult Funktsionid \ Finantsdimensioonide üksikasjad.
17. Klõpsake suvandit Juure lisamine.
    * See andmeallikas määrab, kuidas määratletakse finantsdimensioonide ulatus mis tahes aruande puhul, mis kasutab seda mudelit andmeallikana.  
18. Sisestage väärtus väljale Nimi.
19. Valige väljal Dimensioonide küsimine suvand Jah.
    * Valige Jah, et lubada kasutajal valida käitusajal dimensioone vormilt Kasutaja dialoog. Kui olekuks on määratud Ei, kasutatakse vaikimisi kõiki praeguse eksemplari finantsdimensioone.  
20. Tehke väljal Finantsdimensioonide valimine valik Juriidiline isik.
    * Valige Kõik, et võimaldada kasutajal valida praeguse eksemplari soovitud dimensioone väljalt Otsing.  Valige Juriidiline isik, et võimaldada kasutajal valida ettevõtte dimensioone väljalt Otsing.  Valige Dimensioon, et võimaldada kasutajal valida dimensioone, kasutades ühte dimensioonikogumit.  
21. Valige väljal Põhikonto küsimine suvand Jah.
    * Määrake valiku Põhikonto küsimine väärtuseks Jah, et lasta kasutajatel valida põhikontot dimensioonide loendi osana.   Kui väärtus on Ei, ei lisata põhikontot dimensioonide loendisse ja valik On põhikonto kohustuslik on aktiivne. Kui valiku On põhikonto kohustuslik väärtuseks on määratud Jah, siis lisatakse põhikonto dimensioonide loendisse kasutaja valikust olenemata.  
22. Klõpsake nuppu OK.
23. Valige puul suvand "Dynamics 365 for Operations\tabeli kirjed".
24. Klõpsake suvandit Juure lisamine.
25. Tippige väljale Nimi tekst LedgerJournal.
26. Valige väljal Päringu küsimine suvand Jah.
27. Tippige väljale Tabel tekst LedgerJournalTable.
28. Klõpsake nuppu OK.

## <a name="map-data-model-elements-to-added-data-sources"></a>Andmemudeli elementide vastendamine lisatud andmeallikatega
1. Laiendage puul väärtust 'Tööleht.
2. Laiendage puul väärtust Tööleht \ Kanne.
3. Laiendage puul väärtust Tööleht \ Kanne \ Dimensioonide andmed.
4. Laiendage puul valikut Dimensioonide seadistamine.
5. Laiendage puul valikut LedgerJournal.
6. Laiendage puul valikut „LedgerJournal\<Seosed“.
7. Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans“.
8. Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Kanne“.
9. Valige puult Tööleht \ Kanne \ Kanne.
10. Klõpsake valikut Seo.
11. Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)“.
    * Pange tähele, et igasuguse viite puhul finantsdimensioonidele, mille väärtuseks on määratud näiteks LedgerDimension, on saadaval vastav andmeallika üksus (LedgerDimension.Dimension). See andmeallika üksus pakub selle dimensioonikogumi finantsdimensioone kirjete loendina.  
12. Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)“.
13. Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid“.
14. Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Väärtus“.
15. Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Definitsioon“.
16. Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Definitsioon\Nimi“.
17. Valige puult Tööleht \ Kanne \ Dimensioonide andmed \ Nimi.
18. Klõpsake valikut Seo.
19. Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Väärtus\Kirjeldus“.
20. Valige puult Tööleht \ Kanne \ Dimensioonide andmed \ Kirjeldus.
21. Klõpsake valikut Seo.
22. Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Väärtus\Kood“.
23. Valige puult Tööleht \ Kanne \ Dimensioonide andmed \ Kood.
24. Klõpsake valikut Seo.
25. Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid“.
26. Valige puult Tööleht \ Kanne \ Dimensioonide andmed.
27. Klõpsake valikut Seo.
28. Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Debit(AmountCurDebit)“.
29. Valige puult Tööleht \ Kanne \ Deebet.
30. Klõpsake valikut Seo.
31. Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Date(TransDate)“.
32. Valige puult Tööleht \ Kanne \ Kuupäev.
33. Klõpsake valikut Seo.
34. Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Currency(CurrencyCode)“.
35. Valige puult Tööleht \ Kanne \ Valuuta.
36. Klõpsake valikut Seo.
37. Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Credit(AmountCurCredit)“.
38. Valige puult Tööleht \ Kanne \ Kreedit.
39. Klõpsake valikut Seo.
40. Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans“.
41. Valige puult Tööleht \ Kanne.
42. Klõpsake valikut Seo.
43. Valige puult LedgerJournal \ Töölehe partiinumber(JournalNum).
44. Valige puult Tööleht \ Partii.
45. Klõpsake valikut Seo.
46. Valige puult LedgerJournal.
47. Valige puult Tööleht.
48. Klõpsake valikut Seo.
49. Laiendage puul väärtust Dimensioonid.
50. Laiendage puul väärtust Dimensioonid \ Põhikonto ja dimensioonid.
51. Laiendage puul väärtust Dimensioonid \ Põhikonto ja dimensioonid \ Definitsioon.
52. Valige puult Dimensioonid \ Põhikonto ja dimensioonid \ Definitsioon \ Nimi.
53. Valige puult Dimensioonide seadistus \ Kood.
54. Klõpsake valikut Seo.
55. Valige puult Dimensioonid \ Põhikonto ja dimensioonid \ Definitsioon \ Aruande veeru nimi.
56. Valige puult Dimensioonide seadistus \ Nimi.
57. Klõpsake valikut Seo.
58. Valige puult Dimensioonid \ Põhikonto ja dimensioonid.
59. Valige puult Dimensioonide seadistus.
60. Klõpsake valikut Seo.
61. Valige puult väärtus Ettevõte.
62. Klõpsake nuppu Redigeeri.
63. Sisestage väljale expressionAsStringText väärtus Company.'find()'.'name()'.
    * Company.'find()'.'name()'  
64. Klõpsake nuppu Salvesta.
65. Sulgege leht.
66. Klõpsake nuppu Salvesta.
67. Sulgege leht.

## <a name="complete-this-draft-models-version"></a>Täitke see mudeli mustandi versioon
1. Sulgege leht.
2. Sulgege leht.
3. Klõpsake valikut Muuda olekut.
4. Klõpsake valikut Valmis.
5. Klõpsake nuppu OK.

