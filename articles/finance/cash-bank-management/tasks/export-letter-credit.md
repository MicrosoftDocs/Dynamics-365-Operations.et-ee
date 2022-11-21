---
title: Akreditiivi eksport
description: See protseduur selgitab akreditiivi eksportimise protsessi.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf06a73bf7665059658c7884a0b9f973929d647c
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779550"
---
# <a name="export-letter-of-credit"></a>Akreditiivi eksport

[!include [banner](../../includes/banner.md)]

See protseduur selgitab akreditiivi eksportimise protsessi.

Akreditiiv on panga väljastatud lepe, milles pank nõustub tagama makse ostja nimel, kui ostja ja müüja vahelise leppe tingimused on täidetud.



Käivitage **panga süsteemiteenuse häälestamine ja sisestusreeglite** protseduur **Credit_Create protseduuri** enne seda protseduuri panga süsteemiteenuse lepingu protseduuri. Selleks et protseduur õnnestuks, peab USMF-i demoettevõte olema valitud.


## <a name="create-sales-order-for-export-letter-of-credit"></a>Akreditiivi eksportimise jaoks müügitellimuse loomine
1. Minge kõigi **> müügireskontro > müügireskontrosse**.
2. Klõpsake valikut **Uus**.
3. Klõpsake väljal **Kliendi konto** otsingu avamiseks ripploendi nuppu.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake loendis valitud real olevat linki.
6. Laiendage või ahendage **jaotist** Üldine.
7. Klõpsake väljal **Sait** otsingu avamiseks ripploendi nuppu.
    * Valige **sait**, kus välja antud kaup ladustatakse.  
8. Klõpsake loendis valitud real olevat linki.
9. Väljal **Ladu** klõpsake ripploendi nuppu, et avada otsing.
    * **Valige ladu**, kus väljaminev kaup ladustatakse.  
10. Klõpsake loendis valitud real olevat linki.
    * Märkus: pangadokumendi **tüübi** väli tuleb valida **akreditiiviga**.  
11. **Väljal Pangadokumendi tüüp** valige akreditiivi **.**
12. Saate jaotist Tarne laiendada või **ahendada**.
    * Valige **tarnekuupäeva kontroll** = **Pole**.  
13. Sisestage **väljale Nõutav** sissetulekukuupäev kuupäev.
14. Klõpsake valikut **OK**.
15. Väljal **Kaubakood** klõpsake ripploendi nuppu, et avada otsing.
    * Valige väljastamiseks/müümiseks vajalik kaup.  
16. Otsige loendist ja valige soovitud kirje.
17. Klõpsake loendis valitud real olevat linki.
18. Sisestage arv väljale **Ühiku hind**.
19. Laiendage või ahendage jaotist **Rea üksikasjad**.
20. Klõpsake vahekaardil **Tarne**.
21. Sisestage **väljale Nõutav** lähetuskuupäev kuupäev.
22. Sisestage **kinnitatud** lähetuskuupäeva väljale kuupäev.
23. Tegevuspaanil klõpsake nuppu **Haldamine**.
24. Klõpsake **akreditiivile**
25. **Tippige väärtus väljale** Pangadokumendi number.
26. Sisestage **aegumiskuupäeva** väljale kuupäev ja kellaaeg.
27. Laiendage või ahendada **panga üksikasjade** jaotist.
28. **Otsingu avamiseks** klõpsake väljaAndv pank ripploendit.
29. Klõpsake loendis valitud real olevat linki.
30. **Otsingu avamiseks klõpsake** nõustamise panga väljal ripploendit.
31. Otsige loendist ja valige soovitud kirje.
32. Klõpsake loendis valitud real olevat linki.
33. Klõpsake **müügitellimuse saadetiste toomiseks**.
34. Klõpsake käsku **Väljasta pangadokument**.
35. Sulgege leht.

## <a name="post-packing-slip"></a>Saatelehe sisestamine
1. Klõpsake tegevuspaanil valikut **Komplekteerimine ja pakkimine.**
2. Klõpsake **käsku Sisesta saateleht**.
3. Laiendage või ahendage jaotist **Parameetrid**.
4. Valige väljal **Kogus** suvand **Kõik**.
5. Laiendage või ahendage **jaotist** Seadistus.
6. **Sisestage kuupäev väljale** Saatelehe kuupäev.
7. Valige saadetise number.
8. Klõpsake loendis valitud real olevat linki.
9. Klõpsake valikut **OK**.
10. Klõpsake valikut **OK**.

## <a name="post-sales-invoice"></a>Müügiarve sisestamine
1. Klõpsake toimingupaanil valikut **Arve**.
2. Klõpsake **Arve**.
3. Laiendage või ahendage **jaotist** Ülevaade.
4. Valige saadetise **number**.
5. Klõpsake loendis valitud real olevat linki.
6. Laiendage või ahendage **jaotist** Seadistus.
7. Sisestage kuupäev väljale **Arve kuupäev**.
8. Klõpsake valikut **OK**.
9. Klõpsake valikut **OK**.

## <a name="shipment-document-submitted-status"></a>Saadetise dokumendi esitamise olek
1. Tegevuspaanil klõpsake nuppu **Haldamine**.
2. Klõpsake **akreditiivile**
3. Laiendage või ahendage **jaotist** Read.
    * Märkus: dokumendi **esitatud** välja väärtuseks tuleks määrata **Jah**.  

## <a name="verify-export-letter-of-credit"></a>Akreditiivi eksportimise kinnitamine
1. Minge sularaha **ja panga > akreditiivid > Ekspordi akreditiivi ja sissenõude importimine**.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
    * Kontrollige, **kas ekspordi akreditiivi** saadetise **olek on** **Arveldatud**.  

## <a name="customer-payment"></a>Kliendi makse
1. Avage müügireskontro **> Maksete > maksetööleht**.
2. Klõpsake valikut **Uus**.
3. Märkige loendis valitud rida.
4. Klõpsake väljal **Nimi** otsingu avamiseks ripploendi nuppu.
5. Klõpsake loendis valitud real olevat linki.
6. Klõpsake **Read**.
7. Väljale **Kuupäev** sisestage kuupäev.
8. Täpsustage soovitud väärtusi väljal **Konto**.
9. Klõpsake nuppu **Tasakaalustamine**.
10. Valige märkeruut jaotise Kogusummad päises.
    * Märkus: seadke välja **Kuva** väärtuseks **Akreditiivi**.  
11. Otsige loendist ja valige soovitud kirje.
12. Märkige või tühjendage **ruut** Märgi.
13. Klõpsake valikut **OK**.
14. Klõpsake vahekaardil **Makse**.
    * Kontrollige pangadokumendi numbrit ja saadetise numbri üksikasju.  
15. Klõpsake käsku **Sisesta**.

## <a name="verify-export-letter-of-credit-after-payment"></a>Akreditiivi eksportimise kinnitamine pärast makset
1. Minge sularaha **ja panga > akreditiivid > Ekspordi akreditiivi ja sissenõude importimine**.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
    * Kontrollige, et **saadetise olek Makse** = **saadud ja** **Saldo summa** = **0,00**.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
