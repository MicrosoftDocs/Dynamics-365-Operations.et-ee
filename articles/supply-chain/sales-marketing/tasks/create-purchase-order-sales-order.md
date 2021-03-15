---
title: Ostutellimuse loomine müügitellimuselt
description: See protseduur näitab, kuidas koostada müügitellimusel põhinevat ostutellimust.
author: omulvad
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5cabb1647b2008bbb67a7b9d6789fddab66b54e3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974831"
---
# <a name="create-a-purchase-order-from-a-sales-order"></a>Ostutellimuse loomine müügitellimuselt

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas koostada müügitellimusel põhinevat ostutellimust. Tootekogused ostutellimusel määratakse siis nii, et need täidaksid algse müügitellimuse nõudluse. Selline müüginõudluse rahuldamine on alternatiiv põhjalikumale ja optimeeritud meetodile nimega jaotusnõuete plaanimine. Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega.


## <a name="create-a-purchase-order-from-a-sales-order"></a>Ostutellimuse loomine müügitellimuse põhjal
1. Avage **Navigeerimispaan > Moodulid > Müük ja turundus > Müügitellimused > Kõik müügitellimused**.
2. Klõpsake valikut **Uus**.
3. Klõpsake väljal **Kliendi konto** otsingu avamiseks ripploendi nuppu.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake valikut **OK**.
6. Väljal **Kaubakood** klõpsake ripploendi nuppu, et avada otsing.
7. Otsige loendist ja valige soovitud kirje. USMF-i kasutamisel võite valida väärtuse D0001.  
8. Sisestage arv väljale **Kogus**.
9. Klõpsake käsku **Lisa rida**.
10. Väljal **Kaubakood** klõpsake ripploendi nuppu, et avada otsing.
11. Otsige loendist ja valige soovitud kirje. USMF-i kasutamisel võite valida väärtuse T0020.  
12. Klõpsake loendis valitud real olevat linki.
13. Sisestage arv väljale **Kogus**.
14. Klõpsake valikut **Salvesta**.
15. Klõpsake **Tegevuspaanil** valikut **Müügitellimus**.
16. Klõpsake valikut **Ostutellimus**. Lehel **Ostutellimuse loomine** on kõik avatud müügitellimuse read, mis on müügitellimuselt kopeeritud. Saate vaadata tellimuse üksikasju ja vajaduse korral muuta valitud üksikasju nagu ostu kogus ja hinnatingimused, enne ostude loomist. 
17. Valige suvand **Lisa kõik**.
    - Kui soovite luua ostutellimused ainult müügitellimuse ridade alamkogumile, valige need eraldi.  
    - Väli **Hankija konto** võib juba hankija numbrit sisaldada või mitte sisaldada. Kui tootele on (seotud kauba laovarudes) seadistatud vaikehankija, kopeeritakse reale see hankija. Vastasel korral tuleb hankija sisestada käsitsi.  Selles juhendis, olenemata sellest, kas väljal **Hankija konto** on juba väärtus või mitte, juhendavad järgmised toimingud teid valima uut hankijat, kes on iga rea puhul erinev.  
18. Klõpsake väljal **Hankija konto** otsingu avamiseks ripploendi nuppu.
19. Otsige loendist ja valige soovitud kirje.
20. Klõpsake loendis valitud real olevat linki.
21. Valige teine tellimuserida.
22. Klõpsake väljal **Hankija konto** otsingu avamiseks ripploendi nuppu.
23. Otsige loendist ja valige soovitud kirje.
24. Klõpsake loendis valitud real olevat linki.
25. Klõpsake valikut **Kinnita**.
26. Klõpsake valikut **OK**. Sõnum teavitab teid, et loodud on vähemalt üks ostutellimus. Süsteem koostab eraldi ostutellimuse iga hankija puhul, kelle müügitellimuse ridadel määrasite. See tähendab, et kui sama hankija peab tarnima mitu müügitellimuse rida, koostatakse üks mitme reaga ostutellimus.  

## <a name="review-purchase-orders-created-from-sales-orders"></a>Vaadake müügitellimustest loodud ostutellimused üle.
1. Paanil **Toimingupaan** klõpsake **Üldine**.
2. Klõpsake valikut **Seotud tellimused**. Lehel **Seotud tellimused** on kõik tellimused, mis müügitellimusest loodi. Selles näites on kaks ostutellimust, mis on koostatud vastavalt kahele hankijale. 
3. Klõpsake, et järgida linki väljal **Ostutellimus**. Iga ostutellimuse rida on seotud müügitellimuse reaga, mis viis ostuni. Seos müügitellimusega on näidatud **Toote vahekaardil** kiirkaardil **Rea üksikasjad** väljadel **Viite tüüp**, **Viitenumber** ja **Viitepartii**.  
4. Laiendage või ahendage jaotist **Rea üksikasjad**.
5. Klõpsake vahekaarti **Toode**.
    - **Viitepartii** tagab, et selle ostu kulud kantakse manustatud müügitellimusele.  
    - Saate liikuda algse müügitellimuse juurde, avades lingi väljal **Viitenumber**.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]