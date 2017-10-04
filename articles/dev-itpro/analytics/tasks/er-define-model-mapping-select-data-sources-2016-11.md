--- 
title: "Elektroonilise aruandluse (ER) mudeli vastenduse määratlemine ja andmeallikate valimine"
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab valida andmeallikaid elektroonilise aruandluse (ER) andmemudeli jaoks."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 9a7d8c4335ab29174fe4e4f3d6c4a771c23c746d
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="define-model-mapping-and-select-data-sources-for-electronic-reporting-er"></a>Elektroonilise aruandluse (ER) mudeli vastenduse määratlemine ja andmeallikate valimine

[!include[task guide banner](../../includes/task-guide-banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab valida andmeallikaid elektroonilise aruandluse (ER) andmemudeli jaoks. Andmeallikad seotakse valitud andmemudeli üksikute komponentidega kujundamise ajal ja täidetakse selle andmemudeli äriandmetega töö ajal. Selles näites valite andmeallikad olemasoleva andmemudeli jaoks, mis on loodud näidisettevõtte Litware, Inc. jaoks. Nende etappide lõpuleviimiseks peate kõigepealt läbima etapid protseduuris Uue andmemudeli loomine.


## <a name="open-the-electronic-reporting-configurations-tree"></a>Elektroonilise aruandluse konfiguratsioonipuu avamine
1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
2. Klõpsake valikut Aruandluse konfiguratsioonid.

## <a name="insert-a-new-model-mapping"></a>Sisestage uue mudeli vastendamine
1. Valige puul suvand Maksed (lihtsustatud mudel).
2. Klõpsake valikut Kujundaja.
3. Klõpsake suvandit Mudeli vastendamine andmeallikaga.
4. Klõpsake valikut Uus.
    * See loob uue kirje, mis vastendab andmemudeli andmeallikatega. Selles näites vastendate andmemudeli andmeallikatega soovitud maksetüübi puhul: kreeditiülekanne.     Konkreetse andmemudeli puhul on võimalik kavandada rohkem kui ühe vastendamise. Näiteks võite luua vastendamise eri maksetüüpide puhul, nagu otsekorraldus või kreeditiülekanded. Selles näites loote vastendamise kreeditiülekannete puhul.  
5. Sisestage väljale Nimi suvand Kreeditiülekande vastendamine.
    * Kreeditiülekande vastendamine  
6. Sisestage väljale Kirjeldus suvand Maksemudeli vastendamine (kreeditiülekanne).
    * Maksemudeli vastendamine (kreeditiülekanne)  
7. Väljale Definitsioon tippige „CustomerCreditTransferInitiation”.
    * CustomerCreditTransferInitiation  
8. ResolveChanges definitsiooni.
9. Klõpsake nuppu Salvesta.

## <a name="define-required-data-sources-for-the-current-model-mapping"></a>Praeguse mudeli vastendamise puhul nõutud andmeallikate määratlemine
1. Klõpsake valikut Kujundaja.
2. Valige puul suvand "Dynamics 365 for Operations\tabeli kirjed".
3. Klõpsake suvandit Juure lisamine.
    * Sisestage maksekannete juurde pääsemiseks see andmeallikas.  
4. Sisestage väljale Nimi suvand Kanded.
    * Kanded  
5. Sisestage väljale Silt suvand Kanded.
    * Kanded  
6. Sisestage väljale Spikker suvand Pearaamatu töölehe read.
    * Pearaamatu töölehe read  
7. Valige väljal Päringu küsimine suvand Jah.
    * Valige Jah.  
8. Sisestage väljale Tabel suvand LedgerJournalTrans.
    * LedgerJournalTrans  
9. Klõpsake nuppu OK.
    * Valige tabel LedgerJournalTrans praeguse andmemudeli andmeallikana.  
10. Valige puul suvand Funktsioonid\arvutatud väli.
11. Klõpsake vahekaarti Lisa.
    * Klõpsake uue arvutatud välja lisamiseks käsku Lisa.  
12. Sisestage väljale Nimi suvand $EndToEndID.
    * $EndToEndID  
13. Klõpsake suvandit Muuda valemit.
14. Valige puul suvand String\ÜHENDA.
15. Klõpsake suvandit Funktsiooni lisamine.
16. Laiendage puul suvandit Kanded.
17. Valige puul suvand Kanded\kanne.
18. Klõpsake suvandit Andmeallika lisamine.
19. Väljale Valem sisestage „CONCATENATE(Transactions.Voucher, "-", ”.
    * Sisestage valemi lõppu [ , “-“, ].  
20. Valige puul suvand String\TEKST.
21. Klõpsake suvandit Funktsiooni lisamine.
22. Valige puul suvand Transactions\Record-ID(RecId).
23. Klõpsake suvandit Andmeallika lisamine.
24. Väljale Valem sisestage „CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))”.
    * Sisestage valemi lõppu [))].  
25. Klõpsake nuppu Salvesta.
    * Veenduge, et loodud valemis poleks tuvastatud tõrkeid. Vaadake valemi redaktori kontrolli all olevat vahekaarti TÕRKED.  
26. Sulgege leht.
27. Klõpsake nuppu OK.
    * Lisage arvutatud väli sellele andmeallikale.  
28. Klõpsake vahekaarti Lisa.
    * Klõpsake uue arvutatud välja lisamiseks käsku Lisa.  
29. Sisestage väljale Nimi suvand $Amount.
    * $Amount  
30. Klõpsake suvandit Muuda valemit.
31. Laiendage puul suvandit Kanded.
32. Valige puul suvand Transactions\Debit(AmountCurDebit).
33. Klõpsake suvandit Andmeallika lisamine.
34. Väljale Valem sisestage „Transactions.AmountCurDebit - ”.
    * Sisestage valemi lõppu [ - ].  
35. Valige puul suvand Transactions\Credit(AmountCurCredit).
36. Klõpsake suvandit Andmeallika lisamine.
37. Klõpsake nuppu Salvesta.
38. Sulgege leht.
39. Klõpsake nuppu OK.
    * See lisab arvutatud välja $Amount praeguse andmemudeli puhul valitud andmeallikale.  
40. Valige puul suvand „Kanded\$Summa“.
41. Laiendage puul suvandit Kanded.
42. Puuvaates laiendage või ahendage suvandit „Kanded\$Summa“.
43. Puuvaates laiendage või ahendage valikut „Kanded”.
44. Valige puul suvand "Dynamics 365 for Operations\tabeli kirjed".
45. Klõpsake suvandit Juure lisamine.
    * Sisestage see andmeallikas ettevõtte pangakonto üksikasjade juurde pääsemiseks.  
46. Sisestage väljale Nimi suvand BankAccount.
    * BankAccount  
47. Sisestage väljale Silt suvand Pangakonto.
    * Pangakonto  
48. Sisestage väljale Spikker suvand Pangakonto.
    * Pangakonto  
49. Valige väljal Päringu küsimine suvand Jah.
    * Valige Jah.  
50. Sisestage väljale Tabel suvand BankAccountTable.
    * BankAccountTable  
51. Klõpsake nuppu OK.
    * Valige tabel BankAccountTable praeguse andmemudeli andmeallikana.  
52. Klõpsake suvandit Juure lisamine.
    * Sisestage see andmeallikas ettevõtte rekvisiitide juurde pääsemiseks.  
53. Sisestage väljale Nimi suvand Ettevõte.
    * Ettevõte  
54. Sisestage väärtus väljale Silt.
    * Ettevõtte andmed  
55. Sisestage väljale Spikker suvand Ettevõtte andmed.
    * Ettevõtte andmed  
56. Valige väljal Päringu küsimine suvand Jah.
    * Valige Jah.  
57. Sisestage väljale Tabel suvand CompanyInfo.
    * CompanyInfo  
58. Klõpsake nuppu OK.
    * Valige tabel CompanyInfo praeguse andmemudeli andmeallikana.  
59. Valige puul suvand Funktsioonid\arvutatud väli.
60. Klõpsake suvandit Juure lisamine.
    * Sisestage arvutatud väli uue andmeallikana.  
61. Sisestage väljale Nimi suvand ProcessingDateTime.
    * ProcessingDateTime  
62. Sisestage väljale Silt suvand Töötlemise kuupäev ja kellaaeg.
    * Töötlemise kuupäev ja kellaaeg  
63. Klõpsake suvandit Muuda valemit.
64. Puuvaates valige „Kuupäev/kellaaeg\SESSIONNOW”.
65. Klõpsake suvandit Funktsiooni lisamine.
66. Klõpsake nuppu Salvesta.
67. Sulgege leht.
68. Klõpsake nuppu OK.
    * Lisage arvutatud väli ProcessingDateTime praeguse andmemudeli andmeallikana.  
69. Klõpsake nuppu Salvesta.
70. Sulgege leht.
71. Sulgege leht.
72. Sulgege leht.

