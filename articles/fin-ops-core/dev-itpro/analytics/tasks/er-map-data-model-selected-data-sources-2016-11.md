---
title: Elektroonilise aruandluse andmemudeli vastendamine valitud andmeallikatele
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis kasutaja saab elektroonilise aruandluse (ER) andmemudeli vastendada valitud rakenduse Microsoft Dynamics 365 Finance andmeallikatega.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2d09370b0e08897799d40c41c20c21b58e885dc
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684303"
---
# <a name="er-map-data-model-to-selected-data-sources"></a>Elektroonilise aruandluse andmemudeli vastendamine valitud andmeallikatele

[!include [banner](../../includes/banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis kasutaja saab elektroonilise aruandluse (ER) andmemudeli vastendada valitud andmeallikatega. Seda mudeli vastendamist kasutatakse hiljem andmeallikana vormingu konfiguratsioonis, mida kasutatakse elektrooniliste maksedokumentide haldamiseks. Selles näites vastendate näidisettevõtte Litware, Inc andmemudelit andmeallikatega. Nende etappide lõpule viimiseks peate esmalt lõpetama etapid protseduuris „Andmeallikate valimine mudeli vastendamiseks”.


## <a name="open-er-configurations-tree"></a>Avatud elektroonilise aruandluse konfiguratsioonide puu
1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
2. Klõpsake suvandit Konfiguratsioonid.

## <a name="select-created-model-mapping"></a>Loodud mudeli vastendamise valimine
1. Valige puul suvand Maksed (lihtsustatud mudel).
    * Veenduge, et mudeli konfiguratsioon „Maksed (lihtsustatud mudel)” oleks eelnevalt loodud. Vastasel juhul lõpetage kohe ja naaske pärast tegevusejuhise „Uue konfiguratsiooni loomine valitud domeeni andmemudeliga” lõpule viimist.  
2. Klõpsake suvandit Mudeli koostaja.
3. Klõpsake suvandit Mudeli vastendamine andmeallikaga.
4. Valige kirje Kreeditiülekande vastendamine.
    * Kreeditiülekande vastendamine  

## <a name="bind-created-data-sources-to-data-model-elements"></a>Loodud andmeallikate sidumine andmemudeli elementidega
1. Klõpsake valikut Kujundaja.
2. Valige puul suvand Töötluse kuupäev ja kellaaeg (ProcessingDateTime).
3. Valige puul suvand Processing date(ProcessingDateTime).
4. Klõpsake valikut Seo.
5. Valige puul suvand Payment message identification(MessageIdentification).
6. Laiendage puul suvandit Kanded.
7. Valige puul suvand Transactions\Journal batch number(JournalNum).
8. Klõpsake valikut Seo.
9. Valige puul suvand Maksed.
10. Valige puul suvand Kanded.
11. Klõpsake valikut Seo.
12. Laiendage puus sõlme Payments= Transactions.
13. Laiendage puus sõlme Payments= Transactions\Creditor.
14. Laiendage puus sõlme Payments= Transactions\Creditor\Account.
15. Valige puul suvand Payments= Transactions\Creditor\Account\Currency code(Currency).
16. Laiendage puus sõlme Transactions\vendBankAccountInTransactionCompany().
17. Valige puul suvand Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode).
18. Klõpsake valikut Seo.
19. Valige puul suvand Payments= Transactions\Creditor\Account\IBAN code(IBAN).
20. Valige puul suvand Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN).
21. Klõpsake valikut Seo.
22. Valige puul suvand Payments= Transactions\Creditor\Account\Number.
23. Valige puul suvand Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum).
24. Klõpsake valikut Seo.
25. Laiendage puus sõlme Payments= Transactions\Creditor\Agent.
26. Valige puul suvand Payments= Transactions\Creditor\Agent\Name.
27. Valige puul suvand Transactions\vendBankAccountInTransactionCompany()\Name.
28. Klõpsake valikut Seo.
29. Valige puul suvand Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber).
30. Valige puul suvand Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum).
31. Klõpsake valikut Seo.
32. Valige puul suvand Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT).
33. Valige puul suvand Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo).
34. Klõpsake valikut Seo.
35. Valige puul suvand Payments= Transactions\Creditor\Name.
36. Laiendage puus sõlme Transactions\findVendTable().
37. Valige puult 'Transactions\findVendTable()\name()'.
38. Klõpsake valikut Seo.
39. Valige puul suvand Payments= Transactions\Currency code(Currency).
40. Laiendage puus valikut „Transactions\>Relations“.
41. Laiendage puus sõlme „Transactions\>Relations\Currency table(Currency)“.
42. Valige puul suvand „Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)“.
43. Klõpsake valikut Seo.
44. Laiendage puus sõlme Payments= Transactions\Debtor.
45. Laiendage puus sõlme Payments= Transactions\Debtor\Account.
46. Valige puul suvand Payments= Transactions\Debtor\Account\Currency code(Currency).
47. Valige puul suvand Bank Account(BankAccount).
48. Laiendage puus sõlme Bank Account(BankAccount).
49. Valige puul suvand Bank Account(BankAccount)\Currency(CurrencyCode).
50. Klõpsake valikut Seo.
51. Valige puul suvand Bank Account(BankAccount)\IBAN.
52. Valige puul suvand Payments= Transactions\Debtor\Account\IBAN code(IBAN).
53. Klõpsake valikut Seo.
54. Valige puul suvand Payments= Transactions\Debtor\Account\Number.
55. Valige puul suvand Bank Account(BankAccount)\Bank account number(AccountNum).
56. Klõpsake valikut Seo.
57. Laiendage puus sõlme Payments= Transactions\Debtor\Agent.
58. Valige puul suvand Payments= Transactions\Debtor\Agent\Name.
59. Valige puul suvand Bank Account(BankAccount)\Name.
60. Klõpsake valikut Seo.
61. Valige puul suvand Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber).
62. Valige puul suvand Bank Account(BankAccount)\Routing number(RegistrationNum).
63. Klõpsake valikut Seo.
64. Valige puul suvand Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT).
65. Valige puul suvand Bank Account(BankAccount)\SWIFT code(SWIFTNo).
66. Klõpsake valikut Seo.
67. Valige puul suvand Payments= Transactions\Debtor\Name.
68. Valige puul suvand Company information(Company).
69. Laiendage puus sõlme Company information(Company).
70. Valige puul suvand Company information(Company)\Name.
71. Klõpsake valikut Seo.
72. Valige puul suvand Payments= Transactions\Description.
73. Valige puul suvand Transactions\Description(Txt).
74. Klõpsake valikut Seo.
75. Valige puul suvand Payments= Transactions\End to end identification code(End2EndID).
76. Valige puul suvand „Transactions\$EndToEndID“.
77. Klõpsake valikut Seo.
78. Valige puul suvand Payments= Transactions\Instructed amount(InstructedAmount).
79. Valige puul suvand „Kanded\$Summa“.
80. Klõpsake valikut Seo.
81. Valige puul suvand Payments= Transactions\Transaction date(TransactionDate).
82. Valige puul suvand Transactions\Date(TransDate).
83. Klõpsake valikut Seo.

## <a name="validate-created-mapping"></a>Loodud vastendamise kinnitamine
1. Klõpsake suvandit Kinnita.
    * Kinnitage uus vastendus tagamaks, et kõikide sidumistega on korras.  
2. Klõpsake noolt jaotise Vigade loend laiendamiseks või ahendamiseks.
3. Klõpsake nuppu Salvesta.
4. Sulgege leht.
5. Sulgege leht.
6. Sulgege leht.

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a>Mudeli konfiguratsiooni praeguse versiooni oleku muutmine
1. Klõpsake valikut Muuda olekut.
    * Muutke kujundatud mudeli konfiguratsiooni olekut suvandilt Mustand suvandile Lõpule viidud, et muuta see kättesaadavaks maksevormingu kujundamiseks.  
2. Klõpsake valikut Valmis.
    * Valige Lõpeta.  
3. Sisestage väljale Kirjeldus soovitud väärtus.
    * Näiteks „versioon 1”.  
4. Klõpsake nuppu OK.
5. Valige praeguse konfiguratsiooni lõpetatud versioon.
    * Pange tähele, et loodud konfiguratsioon salvestatakse kui lõpetatud versioon 1.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]