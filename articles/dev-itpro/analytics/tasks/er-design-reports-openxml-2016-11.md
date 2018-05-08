--- 
title: Elektroonilise aruandluse (ER) jaoks OpenXML-i vormingus aruannete genereerimiseks konfiguratsiooni koostamine
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua uue elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab malli elektrooniliste dokumentide loomiseks vormingus OPENXML."
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
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 09789957839097ba2898544102af908c198090c7
ms.contentlocale: et-ee
ms.lasthandoff: 11/14/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a>Elektroonilise aruandluse (ER) jaoks OpenXML-i vormingus aruannete genereerimiseks konfiguratsiooni koostamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua uue elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab malli elektrooniliste dokumentide loomiseks vormingus OPENXML. Seda konfiguratsiooni kasutatakse hankija maksete töötlemiseks.



Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc. Neid etappe saab teha ka GBSI ettevõttes.



Etappide lõpuleviimiseks, peate esmalt läbima protseduuri Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine etapid. Peate alla laadima ja salvestama Microsoft Exceli faili [Maksearuande mall](https://go.microsoft.com/fwlink/?linkid=862266). 

## <a name="upload-the-payments-data-model-configuration"></a>Makse andmemudeli konfiguratsiooni üleslaadimine
1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
2. Märkige loendis valitud rida.
    * Valige konfiguratsiooni pakkuja näidisettevõtte Litware, Inc. jaoks. Kui seda konfiguratsiooni pakkujat ei kuvata, peate esmalt läbima etapid protseduuris Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks.  
3. Klõpsake valikut Määra aktiivseks.
4. Klõpsake valikut Hoidlad.
    * Valige võimaluse korral tüübi Operationsi ressursid jaoks hoidla. Kui see on saadaval, jätke uue hoidla loomise järgmised etapid vahele.  
5. Klõpsake valikut Lisa rippdialoogi avamiseks.
6. Sisestage väljale Konfiguratsiooni hoidla tüüp tekst Operatsiooniressursid.
7. Klõpsake käsku Loo hoidla.
8. Klõpsake nuppu OK.
9. Klõpsake valikut Ava.
10. Valige puul väärtus Maksemudel.
11. Klõpsake Import.
    * Importige see andmemudel. Seda kasutatakse andmeallikana uues vormingu konfiguratsioonis. Jätke see etapp vahele, kui see konfiguratsioon on juba imporditud.  
12. Klõpsake nuppu Jah.
13. Sulgege leht.
14. Sulgege leht.

## <a name="create-a-new-format-configuration"></a>Uue vormingu konfiguratsiooni loomine
1. Klõpsake valikut Aruandluse konfiguratsioonid.
2. Valige puul väärtus Maksemudel.
3. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
4. Sisestage väljale Uus suvand Andmemudelil PaymentModel põhinev vorming.
    * Looge vorming, mis põhineb andmemudelil PaymentModel.  
5. Tippige väljale Nimi tekst Töölehe aruande näide.
    * Töölehe aruande näide  
6. Tippige väljale Kirjeldus tekst Töölehe aruande näide hankijate maksete jaoks.
    * Töölehe aruande näide hankijate maksete jaoks.  
7. Sisestage või valige väärtus väljal Andmemudeli definitsioon.
    * Valige määratlus CustomerCreditTransferInitiation.  
8. Klõpsake Loo konfiguratsioon.

## <a name="design-a-new-document-in-openxml-worksheet-format"></a>Uue dokumendi koostamine töölehe vormingus OPENXML
1. Tehke puul valik Maksemudel \ töölehe aruande näide.
2. Klõpsake valikut Kujundaja.
3. Klõpsake toimingupaanil nuppu Impordi.
4. Klõpsake käsku Impordi Excelist.
5. Klõpsake suvandit Manused.
    * Manustage olemasolev Exceli dokument mallina.  
6. Klõpsake valikut Uus.
7. Klõpsake suvandit Fail.
    * Osutage olemasolevale Exceli failile.  
8. Sulgege leht.
9. Sisestage või valige väärtus väljal Mall.
    * Valige manustatud Exceli fail, mida kasutada mallina.  
10. Klõpsake nuppu OK.
    * Pange tähele, et ER-i vormingu komponendid on loodud kujundamisvormingus viitava MS Exceli dokumendi struktuuri alusel (nimega vahemikud).  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a>Uue andmeallika loomine kogusummade arvutamises valuutakoodide järgi
1. Klõpsake vahekaarti Vastendus.
2. Klõpsake suvandit Lisa juur rippdialoogi avamiseks.
3. Valige puul väärtus Funktsioonid\grupeerimisalus.
4. Tippige väljale Nimi tekst PaymentByCurrency.
    * PaymentByCurrency  
5. Klõpsake suvandit Grupi redigeerimise alus.
6. Laiendage puus sõlme „model”.
7. Valige puul suvand model\Payments.
8. Klõpsake suvandit Lisa väli üksusele.
9. Klõpsake suvandit Mida grupeerida.
10. Laiendage puus sõlme model\Payments.
11. Valige puul väärtus model\Payments\Currency.
12. Klõpsake suvandit Lisa väli üksusele.
13. Klõpsake suvandit Grupeeritud väljad.
14. Valige puul väärtus model\Payments\Instructed Amount(InstructedAmount).
15. Klõpsake suvandit Lisa väli üksusele.
16. Klõpsake suvandit Kogumi väljad.
17. Valige suvand väljalt Meetod.
    * Valige summa liitmisfunktsioon.  
18. Tippige väljale Nimi tekst TotalInstructuredAmount.
    * TotalInstructuredAmount  
19. Klõpsake nuppu Salvesta.
20. Sulgege leht.
21. Klõpsake nuppu OK.

## <a name="map-format-components-to-data-sources"></a>Vormingu komponentide vastendamine andmeallikatega
1. Laiendage puus sõlme „model”.
2. Laiendage puus sõlme model\Payments.
3. Laiendage puul suvandit model\Payments\Initiating Party(InitiatingParty).
4. Valige puul väärtus model\Payments\Initiating Party(InitiatingParty)\Name.
5. Puuvaates laiendage valikut „Excel\ReportHeader”.
6. Puuvaates valige „Excel\ReportHeader\CompanyName”.
7. Klõpsake valikut Seo.
8. Laiendage puus sõlme model\Payments\Creditor.
9. Laiendage puul suvandit model\Payments\Creditor\Identification.
10. Tehke puul valik model\Payments\Creditor\Identification\Source ID(SourceID).
11. Puuvaates laiendage „Excel\PaymLines”.
12. Puuvaates valige „Excel\PaymLines\VendAccountName”.
13. Klõpsake valikut Seo.
14. Valige puul suvand model\Payments\Creditor\Name.
15. Puuvaates valige „Excel\PaymLines\VendName”
16. Klõpsake valikut Seo.
17. Laiendage puul valikut model\Payments\Creditor Agent(CreditorAgent).
18. Tehke puul valik model\Payments\Creditor Agent(CreditorAgent)\Name.
19. Puuvaates valige „Excel\PaymLines\Pank”
20. Klõpsake valikut Seo.
21. Tehke puul valik model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber).
22. Puuvaates valige „Excel\PaymLines\RoutingNumber”
23. Klõpsake valikut Seo.
24. Laiendage puus sõlme „model\Payments\Creditor Account(CreditorAccount)”.
25. Laiendage puus sõlme „model\Payments\Creditor Account(CreditorAccount)\Identification”.
26. Tehke puus valik model\Payments\Creditor Account(CreditorAccount)\Identification\Number.
27. Puuvaates valige „Excel\PaymLines\AccountNumber”.
28. Klõpsake valikut Seo.
29. Valige puul väärtus model\Payments\Instructed Amount(InstructedAmount).
30. Puuvaates valige „Excel\PaymLines\Deebet”.
31. Klõpsake valikut Seo.
32. Laiendage puus sõlme model\Payments\Creditor.
33. Laiendage puus sõlme „model\Payments\Creditor Account(CreditorAccount)”.
34. Laiendage puul valikut model\Payments\Creditor Agent(CreditorAgent).
35. Valige puul väärtus model\Payments\Currency.
36. Puuvaates valige „Excel\PaymLines\Valuuta”.
37. Klõpsake valikut Seo.
38. Laiendage puul valikut PaymentByCurrency.
39. Laiendage puul valikut PaymentByCurrency\grouped.
40. Tehke puul valik PaymentByCurrency\grouped\Currency.
41. Puuvaates laiendage valikut „Excel\SummaryLines”.
42. Puuvaates valige „Excel\SummaryLines\SummaryCurrency”.
43. Klõpsake valikut Seo.
44. Laiendage puul valikut PaymentByCurrency\aggregated.
45. Tehke puul valik PaymentByCurrency\aggregated\TotalInstructuredAmount.
46. Puuvaates valige „Excel\SummaryLines\SummaryAmount”.
47. Klõpsake valikut Seo.
48. Tehke puul valik PaymentByCurrency.
49. Puuvaates valige „Excel\SummaryLines”.
50. Klõpsake valikut Seo.
51. Valige puul suvand model\Payments.
52. Puuvaates valige „Excel\PaymLines”.
53. Klõpsake valikut Seo.
54. Klõpsake nuppu Salvesta.
55. Sulgege leht.

## <a name="use-the-created-configuration-for-payments-processing"></a>Loodud konfiguratsiooni kasutamine maksete töötlemiseks
1. Klõpsake valikut Muuda olekut.
2. Klõpsake valikut Valmis.
3. Klõpsake nuppu OK.
4. Sulgege leht.
5. Sulgege leht.
6. Avage Ostureskontro > Makse seadistus > Makseviisid.
7. Kasutage kiirfiltrit, et filtreerida välja Makseviis väärtusega „Elektrooniline”.
    * Elektrooniline  
8. Klõpsake nuppu Redigeeri.
9. Laiendage jaotist Failivormingud.
10. Valige väljal Üldine elektrooniline aruandlus suvand Jah.
11. Sisestage väärtus väljale Ekspordivormingu konfiguratsioon või valige see.
    * Valige konfiguratsioon Töölehe aruande näide.  
12. Klõpsake nuppu Salvesta.
13. Sulgege leht.

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a>Loodud konfiguratsiooni kasutamine makse töölehtede töötlemise testimiseks
1. Avage Ostureskontro > Maksed > Makse tööleht.
2. Klõpsake valikut Uus.
    * Looge uus maksetööleht.  
3. Sisestage väljale Nimi tekst „VendPay”.
    * VendPay  
4. Klõpsake valikut Read.
5. Määrake väljal Konto väärtused GB_SI_000001.
    * GB_SI_000001  
6. Määrake suvandi Deebet väärtuseks 1000.
7. Klõpsake valikut Uus.
8. Määrake väljal Konto väärtused GB_SI_000005.
    * GB_SI_000005  
9. Määrake suvandi Deebet väärtuseks 2000.
10. Tippige väljale Valuuta väärtus EUR.
    *  eurot  
11. Määrake väljal Vastaskonto väärtused GBSI OPER.
    * GBSI OPER  
12. Tippige väljale Makseviis tekst Elektrooniline.
    * Elektrooniline  
13. Klõpsake nuppu Salvesta.
14. Klõpsake valikut Loo maksed.
15. Tippige väljale Makseviis tekst Elektrooniline.
    * Elektrooniline  
16. Väljale Failinimi tippige Maksed.
    * Tippige näiteks tekst Maksed.  
17. Tippige väljale Pangakonto tekst GBSI OPER.
    * GBSI OPER  
18. Klõpsake nuppu OK.
19. Klõpsake nuppu OK.
    * Vaadake loodud tööleht üle, sh makseridade üksikasjad kui ka selles makseteates kasutatud iga valuutakoodi summad.  


