---
title: Akreditiivi eksport
description: See protseduur selgitab akreditiivi eksportimise protsessi.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3cd18320ca8505b1357ce505dfb4c94e81aaae91
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442327"
---
# <a name="export-letter-of-credit"></a>Akreditiivi eksport

[!include [banner](../../includes/banner.md)]

See protseduur selgitab akreditiivi eksportimise protsessi.

Akreditiiv on panga väljastatud lepe, milles pank nõustub tagama makse ostja nimel, kui ostja ja müüja vahelise leppe tingimused on täidetud.



Enne seda protseduuri käitage protseduuri „Pangateenuste ja sisestusreeglite seadistamine” ja „Akreditiivi jaoks panga süsteemiteenuse leppe loomine”. Selleks et protseduur õnnestuks, peab USMF-i demoettevõte olema valitud.




## <a name="create-sales-order-for-export-letter-of-credit"></a>Akreditiivi eksportimise jaoks müügitellimuse loomine
1. Avage Müügireskontro > Tellimused > Kõik müügitellimused.
2. Klõpsake valikut Uus.
3. Klõpsake väljal Kliendi konto otsingu avamiseks ripploendi nuppu.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake loendis valitud real olevat linki.
6. Laiendage või ahendage jaotist Üldine.
7. Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.
    * Valige laoala, kus väljastatavat kaupa ladustatakse.  
8. Klõpsake loendis valitud real olevat linki.
9. Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.
    * Valige ladu, kus väljastatavat kaupa ladustatakse.  
10. Klõpsake loendis valitud real olevat linki.
    * Märkus. Väljal Pangadokumendi tüüp tuleb valida väärtus „Akreditiiv”.  
11. Valige väljal Pangadokumendi tüüp suvand Akreditiiv.
12. Laiendage või ahendage jaotist Tarne.
    * Valige suvandi Tarnekuupäeva kontroll sätteks Puudub.  
13. Sisestage kuupäev väljale Nõutav sissetulekukuupäev.
14. Klõpsake nuppu OK.
15. Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.
    * Valige väljastamiseks/müümiseks vajalik kaup.  
16. Otsige loendist ja valige soovitud kirje.
17. Klõpsake loendis valitud real olevat linki.
18. Sisestage arv väljale Ühiku hind.
19. Laiendage või ahendage jaotist Rea üksikasjad.
20. Klõpsake vahekaarti Tarne.
21. Sisestage kuupäev väljale Nõutav lähetuskuupäev.
22. Sisestage kuupäev väljale Kinnitatud lähetuskuupäev.
23. Klõpsake tegumiribal valikut Haldamine.
24. Klõpsake suvandit Akreditiiv.
25. Tippige väärtus väljale Pangadokumendi number.
26. Sisestage kuupäev ja kellaaeg väljale Aegumiskuupäev.
27. Laiendage või ahendage jaotist Panga üksikasjad.
28. Klõpsake väljal Väljaandev pank otsingu avamiseks ripploendi nuppu.
29. Klõpsake loendis valitud real olevat linki.
30. Klõpsake väljal Nõustav pank otsingu avamiseks ripploendi nuppu.
31. Otsige loendist ja valige soovitud kirje.
32. Klõpsake loendis valitud real olevat linki.
33. Klõpsake suvandit Müügitellimuse saadetiste toomine.
34. Klõpsake suvandit Pangadokumendi väljastamine.
35. Sulgege leht.

## <a name="post-packing-slip"></a>Saatelehe sisestamine
1. Klõpsake toimingupaanil valikut Komplekteerimine ja pakkimine.
2. Klõpsake valikut Saatelehe sisestamine.
3. Laiendage või ahendage jaotist Parameetrid.
4. Väljal Kogus valige Kõik.
5. Laiendage või ahendage jaotist Häälestus.
6. Sisestage kuupäev väljale Saatelehe kuupäev.
7. Valige saadetise number.
8. Klõpsake loendis valitud real olevat linki.
9. Klõpsake nuppu OK.
10. Klõpsake nuppu OK.

## <a name="post-sales-invoice"></a>Müügiarve sisestamine
1. Klõpsake toimingupaanil valikut Arve.
2. Klõpsake valikut Arve.
3. Laiendage või ahendage jaotist Ülevaade.
4. Valige saadetise number.
5. Klõpsake loendis valitud real olevat linki.
6. Laiendage või ahendage jaotist Häälestus.
7. Sisestage kuupäev väljale Arve kuupäev.
8. Klõpsake nuppu OK.
9. Klõpsake nuppu OK.

## <a name="shipment-document-submitted-status"></a>Saadetise dokumendi esitamise olek
1. Klõpsake tegumiribal valikut Haldamine.
2. Klõpsake suvandit Akreditiiv.
3. Laiendage või ahendage jaotist Read.
    * Märkus. Välja „Dokument on saadetud” väärtus peab olema „Jah”.  

## <a name="verify-export-letter-of-credit"></a>Akreditiivi eksportimise kinnitamine
1. Avage jaotis Sularaha- ja pangahaldus > Akreditiivid > Ekspordi akreditiiv ja sissenõue.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
    * Veenduge, et akreditiivi eksportimise tarne olek oleks „Arveldatud”.  

## <a name="customer-payment"></a>Kliendi makse
1. Avage Müügireskontro > Maksed > Makse tööleht.
2. Klõpsake valikut Uus.
3. Märkige loendis valitud rida.
4. Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.
5. Klõpsake loendis valitud real olevat linki.
6. Klõpsake valikut Read.
7. Sisestage kuupäev väljale Kuupäev.
8. Täpsustage soovitud väärtusi väljal Konto.
9. Klõpsake suvandit Tasakaalustused.
10. Valige märkeruut jaotise Kogusummad päises.
    * Märkus. Valige väljal Kuva suvand „Akreditiiv”.  
11. Otsige loendist ja valige soovitud kirje.
12. Märkige või tühjendage ruut Märgi.
13. Klõpsake nuppu OK.
14. Klõpsake vahekaarti Makse.
    * Kontrollige pangakonto numbri ja saadetise numbri üksikasju  
15. Klõpsake valikut Sisesta.

## <a name="verify-export-letter-of-credit-after-payment"></a>Akreditiivi eksportimise kinnitamine pärast makset
1. Avage jaotis Sularaha- ja pangahaldus > Akreditiivid > Ekspordi akreditiiv ja sissenõue.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
    * Veenduge, et tarne olek oleks Makse vastu võetud ja saldo summa oleks 0.00.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]