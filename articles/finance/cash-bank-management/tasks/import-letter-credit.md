---
title: Akreditiivi importimine
description: See protseduur selgitab akreditiivi importimise protsessi.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95a79b3c391c15099aee0a8d34419e1cf48fafbc
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803987"
---
# <a name="import-letter-of-credit"></a>Akreditiivi importimine

[!include [banner](../../includes/banner.md)]

See protseduur selgitab akreditiivi importimise protsessi. Enne seda protseduuri tuleb häälestada järgmised üksused: panga süsteemiteenused, sisestusreeglid, panga süsteemiteenuse lepe ja hankija panga üksikasjad.

See protsess kasutab demoettevõtte USMF-i andmeid.


## <a name="create-a-purchase-order-with-letter-of-credit"></a>Ostutellimuse loomine akreditiiviga
1. Minge kõigi **> ostutellimuste > ostureskontrosse**.
2. Klõpsake valikut **Uus**.
3. Sisestage või valige väärtus väljale **Hankija konto**.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake loendis valitud real olevat linki.
6. Laiendage jaotist **Üldine**.
7. Sisestage või valige väärtus väljale **Sait**.
8. Klõpsake loendis valitud real olevat linki.
9. Sisestage või valige väärtus väljale **Ladu**.
10. Klõpsake loendis valitud real olevat linki.
11. Sisestage kuupäev väljale **Aruandluskuupäev.**
12. **Sisestage kuupäev väljale Tarnekuupäev.**

>[!Note] 
>Pangadokumendi **tüübi väli** peaks olema **akreditiiviväli**.  

13. Klõpsake valikut **OK**.
14. Sisestage või valige väärtus väljale **Kauba kood**.
15. Otsige loendist ja valige soovitud kirje.
16. Klõpsake loendis valitud real olevat linki.
17. Laiendage jaotist **Rea üksikasjad**.
18. Klõpsake vahekaardil **Tarne** .
19. **Sisestage kuupäev väljale Tarnekuupäev.**
20. Väljale **Kinnitatud tarnekuupäev** sisestage kuupäev.
21. Sisestage arv väljale **Ühiku hind**.
    * Määratlege akreditiivi üksikasjad.  
22. Tegevuspaanil klõpsake nuppu **Haldamine**.
23. Klõpsake **akreditiivi / sissenõude importimise**
24. Sisestage **väljale Rakenduse** kuupäev kuupäev ja kellaaeg.
    * Kontrollige **, et pangakonto** väljal oleks vaikimisi aktiivne pangakonto, mis põhineb avalduse kuupäeval.  
25.  **Tippige väärtus väljale** Pangadokumendi number.
26.  **Sisestage sissetuleku kuupäev** ja kellaaeg väljale Sissetuleku kuupäev.
27. Laiendage jaotist **Pank** .
28. Sisestage **aegumiskuupäeva** väljale kuupäev ja kellaaeg.
29. Laiendage jaotist **Panga** üksikasjad.
30. Sisestage **või valige väärtus väljal** Nõustav pank.
31. Klõpsake loendis valitud real olevat linki.
32. Klõpsake nuppu **Salvesta**.
33. Klõpsake **ostutellimuse saadetiste toomiseks**.
34. Sulgege leht.
35. Klõpsake toimingupaanil valikut **Ost**.
36. Klõpsake käsku **Kinnita**.
37. Tegevuspaanil klõpsake nuppu **Haldamine**.
38. Klõpsake **akreditiivi / sissenõude importimine**
39. Klõpsake nuppu **Töötle**.
40. Klõpsake käsku **Kinnita**.
    * Veenduge, et süsteemiteenuse saldo vähendaks ostutellimuse summat. Selles näites on ostusumma = 500,00, süsteemiteenuse limiit = 10 000,00, seega on süsteemiteenuse saldo = 9500,00.  
41. Sulgege leht.
42. Sisestage arv väljale **Ühiku hind**.
43. Klõpsake nuppu **Salvesta**.
44. Klõpsake toimingupaanil valikut **Ost**.
45. Klõpsake käsku **Kinnita**.
    * Akreditiivi muutmine ühiku hinna muudatuse tõttu  
46. Tegevuspaanil klõpsake nuppu **Haldamine**.
47. Klõpsake **akreditiivi / sissenõude importimine**
    * Parandage akreditiivi ühiku hinna muutuse tõttu.  
48. Klõpsake nuppu **Töötle**.
49. Klõpsake **nuppu Muuda**.
50. Klõpsake käsku **Eemalda**.
51. Klõpsake nuppu **Jah**.
52. Klõpsake **ostutellimuse saadetiste toomiseks**.
53. Klõpsake nuppu **Töötle**.
54. Klõpsake käsku **Kinnita**.
    * Veenduge, et süsteemiteenuse saldo vähendaks ostutellimuse summat. Selles näites on muudetud ostusumma = 600,00, süsteemiteenuse limiit = 10 000,00, seega on süsteemiteenuse saldo = 9400,00.  
55. Sulgege leht.

## <a name="post-packing-slip"></a>Saatelehe sisestamine
1. Klõpsake toimingupaanil valikut **Vastuvõtt**.
2. Klõpsake valikut **Toote sissetulek**.
3.  **Tippige PurchParmTable_Num** väärtus väljale.
    * Valige saadetise **number,** mis on loodud akreditiivi viitega.  
4. Klõpsake loendis valitud real olevat linki.
5. Sisestage **kuupäev väljale** Toote sissetuleku kuupäev.
6. Klõpsake valikut **OK**.
7. Sulgege leht.
8. Sulgege leht.

## <a name="verify-import-letter-of-credit-status"></a>Akreditiivi importimise oleku kinnitamine
1. Avage sularaha **ja panga > akreditiivid > Impordi akreditiivi ja sissenõude importimine**.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
    * Akreditiivi **importimise oleku kontrollimine**     
4. Sulgege leht.
5. Sulgege leht.

## <a name="post-purchase-invoice"></a>Ostuarve sisestamine
1. Minge kõigi **> ostutellimuste > ostureskontrosse**.
    * Valige akreditiiviga loodud ostutellimus.  
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
4. Klõpsake toimingupaanil valikut **Arve**.
5. Klõpsake **Arve**.
6. Sisestage väärtus väljale **Arv**.
7. Sisestage **või** valige väärtus väljal Saadetise number.
8. Klõpsake loendis valitud real olevat linki.
9. Sisestage kuupäev väljale **Arve kuupäev**.
10. **Klõpsake suvandit Värskenda vastendamise olek.**
11. Klõpsake käsku **Sisesta**.
12. Sulgege leht.
13. Sulgege leht.

## <a name="verify-import-letter-of-credit-status-and-printing"></a>Kinnitage akreditiivi importimise olek ja printimine

1. Avage sularaha **ja panga > akreditiivid > Impordi akreditiivi ja sissenõude importimine**.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
    * Kinnitage akreditiivi importimine.  
    * Kinnita: saadetise  **olek Arveldatud** = **panga**  süsteemiteenuse üksikasjad  
4. Klõpsake **käsku Vaata**.
5. Klõpsake **käsku Prindi avaldus**.
6. Klõpsake valikut **OK**.
    * Veenduge, et akreditiiv prinditaks.  
7. Sulgege leht.
8. Sulgege leht.
9. Sulgege leht.

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a>Akreditiiviga loodud ostuarve makse töölehe sisestamine
1. Minge jaotisse **Ostureskontro > Maksed > Makse tööleht**.
2. Klõpsake valikut **Uus**.
3. Sisestage või valige väärtus väljal **Nimi**.
4. Klõpsake loendis valitud real olevat linki.
5. Klõpsake **Read**.
6. Väljale **Kuupäev** sisestage kuupäev.
7. Täpsustage soovitud väärtusi väljal **Konto**.
8. Klõpsake käsku **Tasakaalusta kanded**.
9. Laiendage **jaotist Kogusummad** .
10.  **Valige suvand** väljal Näita.
    * Kontrollige, et **pangadokumendi number** ja **saadetise numbri väljad** on värskendatud.  
11.  **Märkige ruut** Märgi.
12. Klõpsake valikut **OK**.
13. Klõpsake vahekaarti Makse.
    * Kontrollige, et **pangadokumendi number** ja **saadetise numbri väljad** on värskendatud.  
14. Klõpsake käsku **Sisesta**.
15. Sulgege leht.
16. Sulgege leht.

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a>Pärast arve tasumist kontrollige akreditiivi importimise olekut
1. Avage sularaha **ja panga > akreditiivid > Impordi akreditiivi ja sissenõude importimine**.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
    * Akreditiivi **importimise oleku kontrollimine**   
4. Sulgege leht.

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a>Kontrollige panga süsteemiteenuse limiiti ja tulususe aruannet
1. Avage sularaha **- ja pangahalduse > päringud ja aruanded > akreditiivid või garantiikirjad > panga teenuseid ja tulususaruannet**.
2. Jaotise kaasamiseks laiendage valikut **Kirjed**.
3. Klõpsake käsku **Filtreeri**.
    * Määratlege **nõutava** pangakonto väli Kriteeriumid.  
4. Sisestage või valige väärtus väljal **Kriteeriumid**.
5. Klõpsake loendis valitud real olevat linki.
6. Klõpsake valikut **OK**.
7. Klõpsake valikut **OK**.
    * Kinnitage aruanne, kus on loetletud kanded.  
    * Veenduge, et aruandes oleks loetletud kanded koos pangadokumendi numbri, süsteemiteenuse limiidi, kasutatud summa ja süsteemiteenuse saldo summa.  
8. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
