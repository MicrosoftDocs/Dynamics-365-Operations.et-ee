--- 
title: Akreditiivi importimine
description: See protseduur selgitab akreditiivi importimise protsessi.
author: kweekley
manager: AnnBe
ms.date: 02/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 02be2627186a149a05eaccfa3e5906a9fe1d74dd
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="import-a-letter-of-credit"></a>Akreditiivi importimine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur selgitab akreditiivi importimise protsessi. Enne seda protseduuri tuleb häälestada järgmised üksused: panga süsteemiteenused, sisestusreeglid, panga süsteemiteenuse lepe ja hankija panga üksikasjad.

See protsess kasutab demoettevõtte USMF-i andmeid.


## <a name="create-a-purchase-order-with-letter-of-credit"></a>Ostutellimuse loomine akreditiiviga
1. Avage Ostureskontro > Ostutellimused > Kõik ostutellimused.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Hankija konto või valige see.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake loendis valitud real olevat linki.
6. Laiendage jaotist Üldine.
7. Sisestage või valige väärtus väljal Koht.
8. Klõpsake loendis valitud real olevat linki.
9. Sisestage või valige väärtus väljal Ladu.
10. Klõpsake loendis valitud real olevat linki.
11. Sisestage kuupäev väljale Aruandluskuupäev.
12. Sisestage kuupäev väljale Tarnekuupäev.
    * Märkus. Väljal „Pangadokumendi tüüp” tuleb valida väärtus „Akreditiiv”.  
13. Klõpsake nuppu OK.
14. Sisestage või valige väärtus väljal Kaubakood.
15. Otsige loendist ja valige soovitud kirje.
16. Klõpsake loendis valitud real olevat linki.
17. Laiendage jaotist Rea üksikasjad.
18. Klõpsake vahekaarti Tarne.
19. Sisestage kuupäev väljale Tarnekuupäev.
20. Sisestage kuupäev väljale Kinnitatud tarnekuupäev.
21. Sisestage arv väljale Ühiku hind.
    * Määratlege akreditiivi üksikasjad.  
22. Klõpsake tegumiribal valikut Haldamine.
23. Klõpsake suvandit Akreditiiv / sissenõude importimine.
24. Sisestage kuupäev ja kellaaeg väljale Avalduse kuupäev.
    * Veenduge, et väljal „Pangakonto” on aktiivne vaikepangakonto, mis põhineb avalduse kuupäeval.  
25. Tippige väärtus väljale Pangadokumendi number.
26. Sisestage kuupäev ja kellaaeg väljale Sissetuleku kuupäev.
27. Laiendage jaotist Pangadokument.
28. Sisestage kuupäev ja kellaaeg väljale Aegumiskuupäev.
29. Laiendage jaotist Panga üksikasjad.
30. Sisestage või valige väärtus väljal Nõustav pank.
31. Klõpsake loendis valitud real olevat linki.
32. Klõpsake nuppu Salvesta.
33. Klõpsake suvandit Ostutellimuse saadetiste toomine.
34. Sulgege leht.
35. Klõpsake toimingupaanil valikut Ost.
36. Klõpsake käsku Kinnita.
37. Klõpsake tegumiribal valikut Haldamine.
38. Klõpsake suvandit Akreditiiv / sissenõude importimine.
39. Klõpsake suvandit Töötle.
40. Klõpsake käsku Kinnita.
    * Veenduge, et süsteemiteenuse saldo vähendaks ostutellimuse summat.  Selles näites on ostusumma = 500,00, süsteemiteenuse limiit = 10 000,00, seega on süsteemiteenuse saldo = 9500,00.  
41. Sulgege leht.
42. Sisestage arv väljale Ühiku hind.
43. Klõpsake nuppu Salvesta.
44. Klõpsake toimingupaanil valikut Ost.
45. Klõpsake käsku Kinnita.
    * Parandage akreditiivi ühiku hinna muutuse tõttu.  
46. Klõpsake tegumiribal valikut Haldamine.
47. Klõpsake suvandit Akreditiiv / sissenõude importimine.
    * Parandage akreditiivi ühiku hinna muutuse tõttu.  
48. Klõpsake suvandit Töötle.
49. Klõpsake käsku Paranda.
50. Klõpsake nuppu Eemalda.
51. Klõpsake nuppu Jah.
52. Klõpsake suvandit Ostutellimuse saadetiste toomine.
53. Klõpsake suvandit Töötle.
54. Klõpsake käsku Kinnita.
    * Veenduge, et süsteemiteenuse saldo vähendaks ostutellimuse summat.  Selles näites on muudetud ostusumma = 600,00, süsteemiteenuse limiit = 10 000,00, seega on süsteemiteenuse saldo = 9400,00.  
55. Sulgege leht.

## <a name="post-packing-slip"></a>Saatelehe sisestamine
1. Klõpsake toimingupaanil valikut Vastuvõtt.
2. Klõpsake valikut Toote sissetulek.
3. Sisestage väärtus väljale PurchParmTable_Num.
    * Valige saadetise number, mis loodi viitega akreditiivile.  
4. Klõpsake loendis valitud real olevat linki.
5. Sisestage kuupäev väljale Toote sissetuleku kuupäev.
6. Klõpsake nuppu OK.
7. Sulgege leht.
8. Sulgege leht.

## <a name="verify-import-letter-of-credit-status"></a>Akreditiivi importimise oleku kinnitamine
1. Avage jaotis Sularaha- ja pangahaldus > Akreditiivid > Impordi akreditiiv ja sissenõue.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
    * Kinnitage akreditiivi importimise olek.  
4. Sulgege leht.
5. Sulgege leht.

## <a name="post-purchase-invoice"></a>Ostuarve sisestamine
1. Avage Ostureskontro > Ostutellimused > Kõik ostutellimused.
    * Valige akreditiiviga loodud ostutellimus.  
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
4. Klõpsake toimingupaanil valikut Arve.
5. Klõpsake valikut Arve.
6. Sisestage väärtus väljale Arv.
7. Sisestage või valige väärtus väljal Saadetise number.
8. Klõpsake loendis valitud real olevat linki.
9. Sisestage kuupäev väljale Arve kuupäev.
10. Klõpsake valikut Värskenda vastandamise olek.
11. Klõpsake valikut Sisesta.
12. Sulgege leht.
13. Sulgege leht.

## <a name="verify-import-letter-of-credit-status"></a>Akreditiivi importimise oleku kinnitamine
1. Avage jaotis Sularaha- ja pangahaldus > Akreditiivid > Impordi akreditiiv ja sissenõue.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
    * Kinnitage akreditiivi importimine.  
    * Kinnitage: saadetise olek = arveldatud Panga süsteemiteenuse üksikasjad  
4. Klõpsake käsku Kuva.
5. Klõpsake suvandit Avalduse printimine.
6. Klõpsake nuppu OK.
    * Veenduge, et akreditiiv prinditaks.  
7. Sulgege leht.
8. Sulgege leht.
9. Sulgege leht.

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a>Akreditiiviga loodud ostuarve makse töölehe sisestamine
1. Avage Ostureskontro > Maksed > Makse tööleht.
2. Klõpsake valikut Uus.
3. Sisestage või valige väärtus väljal Nimi.
4. Klõpsake loendis valitud real olevat linki.
5. Klõpsake valikut Read.
6. Sisestage kuupäev väljale Kuupäev.
7. Täpsustage soovitud väärtusi väljal Konto.
8. Klõpsake suvandit Kannete tasakaalustamine.
9. Laiendage jaotist Kogusummad.
10. Valige suvand väljal Kuva.
    * Veenduge, et väljad Pangakonto number ja Saadetise number oleksid uuendatud.  
11. Märkige ruut Märgi.
12. Klõpsake nuppu OK.
13. Klõpsake vahekaarti Makse.
    * Veenduge, et väljad Pangakonto number ja Saadetise number oleksid uuendatud.  
14. Klõpsake valikut Sisesta.
15. Sulgege leht.
16. Sulgege leht.

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a>Pärast arve tasumist kontrollige akreditiivi importimise olekut
1. Avage jaotis Sularaha- ja pangahaldus > Akreditiivid > Impordi akreditiiv ja sissenõue.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
    * Kinnitage akreditiivi importimise olek.   
4. Sulgege leht.

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a>Kontrollige panga süsteemiteenuse limiiti ja tulususe aruannet
1. Avage jaotis Sularaha- ja pangahaldus > Päringud ja aruanded > Akreditiivid või garantiikirjad > Pangateenuste ja kasutamise aruanne.
2. Jaotise kaasamiseks laiendage kirjeid.
3. Klõpsake käsku Filtreeri.
    * Määratlege väljal Kriteeriumid nõutav pangakonto.  
4. Sisestage või valige väärtus väljal Kriteeriumid.
5. Klõpsake loendis valitud real olevat linki.
6. Klõpsake nuppu OK.
7. Klõpsake nuppu OK.
    * Kinnitage aruanne, kus on loetletud kanded.  
    * Veenduge, et aruandes oleks loetletud kanded koos pangadokumendi numbri, süsteemiteenuse limiidi, kasutatud summa ja süsteemiteenuse saldo summa.  
8. Sulgege leht.


