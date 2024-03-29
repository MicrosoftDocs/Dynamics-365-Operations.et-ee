---
title: Elektrooniline aruandlus. Loodud vormingu komponentide vastendamine andmemudeli elementidega (november 2016)
description: See artikkel kirjeldab, kuidas vastendada andmemudeli elemendid loodud elektroonilise aruandluse (ER) konfiguratsiooni komponentidega.
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner
ms.openlocfilehash: d1dee2a26edd5a2162bb8c5cebaf014825f4e5a2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290210"
---
# <a name="er-map-components-of-the-created-format-to-data-model-elements-november-2016"></a>Elektrooniline aruandlus. Loodud vormingu komponentide vastendamine andmemudeli elementidega (november 2016)

[!include [banner](../../includes/banner.md)]

Järgmine protseduur näitab, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis olev kasutaja saab vastendada andmemudeli elemente loodud elektroonilise aruandluse (ER) konfiguratsiooni komponentidega, mis määratleb maksete äridomeeni elektroonilise dokumendi. Seda vormingut kasutatakse hiljem maksete töötlemiseks elektrooniliste dokumentide loomiseks. Selles näites saate luua vormingukonfiguratsiooni näidisettevõttele „Litware, Inc.”. Neid toiminguid saab teha igas ettevõttes, kuna ER-i konfiguratsioonid on kõigi ettevõtete vahel ühiskasutuses. Nende etappide lõpule viimiseks peate esmalt viima lõpule tegevusejuhises „Vormingu konfiguratsiooni loomine” esitatud etapid.


## <a name="select-a-format-configuration"></a>Vormingu konfiguratsiooni valimine
1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
2. Klõpsake valikut Aruandluse konfiguratsioonid.
3. Laiendage puustruktuuris suvandit Maksed (lihtsustatud mudel).
4. Tehke puustruktuuris valik 'Maksed (lihtsustatud mudel)\BACS (UK fiktiivne)'.
5. Klõpsake valikut Kujundaja.

## <a name="map-format-components-to-data-model-elements"></a>Vormingu komponentide vastendamine andmemudeli elementidega
1. Klõpsake nuppu Laienda/ahenda.
2. Klõpsake vahekaarti Vastendus.
3. Laiendage puus sõlme „model”.
4. Puuvaates valige „Xml\Teade\ProcessingDate\DateTime”.
5. Puuvaates valige „mudel\ProcessingDateTime”.
6. Klõpsake valikut Seo.
7. Puuvaates valige „Xml\Teade\MessageId\String”.
8. Puuvaates valige „mudel\MessageIdentification”.
9. Klõpsake valikut Seo.
10. Laiendage puus sõlme model\Payments.
11. Puuvaates valige „Xml\Teade\Maksed\Kaup\Summa\String”.
12. Puuvaates valige „mudel\Maksed\InstructedAmount”.
13. Klõpsake valikut Seo.
14. Puuvaates valige „Xml\Teated\Maksed\Kaup\TransDate\DateTime”.
15. Puuvaates valige „mudel\Maksed\TransactionDate”.
16. Klõpsake valikut Seo.
17. Puuvaates valige „Xml\Teade\Maksed\Kaup\Kirjeldus\String”.
18. Valige puul suvand model\Payments\Description.
19. Klõpsake valikut Seo.
20. Puuvaates valige „Xml\Teade\Maksed\Kaup\Valuuta\String”.
21. Valige puul väärtus model\Payments\Currency.
22. Klõpsake valikut Seo.
23. Puuvaates valige „Xml\Teade\Maksed\Kaup\ID”.
24. Puuvaates valige „mudel\Maksed\End2EndID”.
25. Klõpsake valikut Seo.
26. Laiendage puus sõlme model\Payments\Creditor.
27. Laiendage puus sõlme model\Payments\Creditor\Account.
28. Laiendage puus sõlme model\Payments\Creditor\Agent.
29. Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Nimi\String”.
30. Valige puul suvand model\Payments\Creditor\Name.
31. Klõpsake valikut Seo.
32. Puuvaates valige „Xml\Teated\Maksed\Kaup\Hankija\Pank\RoutingNumber\String”.
33. Puuvaates valige „mudel\Maksed\Kreeditor\Agent\RoutingNumber”.
34. Klõpsake valikut Seo.
35. Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Pank\AccountNumber\String”.
36. Valige puul suvand model\Payments\Creditor\Account\Number.
37. Klõpsake valikut Seo.
38. Puuvaates valige „Xml\Teade\Maksed\Kaup\Maksja\Nimi\String”.
39. Laiendage puus sõlme model\Payments\Debtor.
40. Laiendage puus sõlme model\Payments\Debtor\Account.
41. Laiendage puus sõlme model\Payments\Debtor\Agent.
42. Valige puul suvand model\Payments\Debtor\Name.
43. Klõpsake valikut Seo.
44. Puuvaates valige „Xml\Teade\Maksed\Kaup\Maksja\Pank\RoutingNumber\String”.
45. Puuvaates valige „mudel\Maksed\Deebitor\Agent\RoutingNumber”.
46. Klõpsake valikut Seo.
47. Puuvaates valige „Xml\Teade\Maksed\Kaup\Maksja\Pank\AccountNumber\String”.
48. Valige puul suvand model\Payments\Debtor\Account\Number.
49. Klõpsake valikut Seo.
50. Puuvaates valige „Xml\Teade\Maksed\Kaup”.
51. Valige puul suvand model\Payments.
52. Klõpsake valikut Seo.
53. Klõpsake nuppu Salvesta.

## <a name="validate-format-mapping"></a>Vormingu vastendamise kinnitamine
1. Klõpsake suvandit Kinnita.
    * Kinnitage uus vastendus tagamaks, et kõikide sidumistega on korras.  
2. Sulgege leht.

## <a name="change-status-of-the-current-version-of-format-configuration"></a>Vormingu konfiguratsiooni praeguse versiooni oleku muutmine
Järgmistes etappides muudate vormingu konfiguratsiooni oleku suvandilt Mustand suvandile Lõpule viidud, et muuta see maksedokumendi loomiseks kättesaadavaks.  
1. Klõpsake valikut Muuda olekut.
2. Klõpsake valikut Valmis.
3. Sisestage väljale Kirjeldus soovitud väärtus.
    * Näiteks „versioon 1”.  
4. Klõpsake nuppu OK.
5. Valige praeguse konfiguratsiooni lõpuleviidud versioon.
    * Pange tähele, et konfiguratsioon salvestatakse kui lõpetatud versioon 1.1: andmemudeli versioonil 1 põhineva vormingu versioon 1.  

## <a name="define-effective-date-for-completed-version-of-format"></a>Vormingu lõpetatud versiooni jõustumiskuupäeva määratlemine
Iga vormingu versiooni saab konfigureerida kasutamiseks kättesaadavaks teatud kuupäevast alates. Kui kindlal kuupäeval on aktiivne rohkem kui ühe vormingu versioon, valitakse kasutamiseks uusim vorming (versiooninumbri põhjal). Õige versiooni valimiseks kasutatakse seansi kuupäeva väärtust.  

## <a name="restrict-access-to-created-format-from-companies"></a>Juurdepääsu piiramine loodud vormingult ettevõtetelt
1. Laiendage jaotist ISO-riigi-/regioonikoodid.
    * Iga vormingu juurdepääsu saab piirata, tuvastades teatud riigid/regioonid, kus vormingut rakendatakse. Kui teatud vormingu puhul on riikide/regioonide loend tühi, saab seda vormingut kasutada mis tahes ettevõttes. Kui riikide/regioonide loendisse sisestatakse mõni ISO-riigi/-regiooni kood, saab seda vormingut kasutada ainult ettevõtetes, mille peamine aadress on riigis/regioonis.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
