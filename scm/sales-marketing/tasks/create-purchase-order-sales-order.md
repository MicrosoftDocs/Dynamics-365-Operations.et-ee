--- 
title: "Ostutellimuse loomine müügitellimuselt"
description: "See protseduur näitab, kuidas koostada müügitellimusel põhinevat ostutellimust."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5c569b6e58507e3b7707e4a56b22d2d60660f144
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-purchase-order-from-a-sales-order"></a>Ostutellimuse loomine müügitellimuselt

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas koostada müügitellimusel põhinevat ostutellimust. Tootekogused ostutellimusel määratakse siis nii, et need täidaksid algse müügitellimuse nõudluse. Selline müüginõudluse rahuldamine on alternatiiv põhjalikumale ja optimeeritud meetodile nimega jaotusnõuete plaanimine. Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega.


## <a name="create-a-purchase-order-from-a-sales-order"></a>Ostutellimuse loomine müügitellimuselt
1. Avage Müük ja turundus > Müügitellimused > Kõik müügitellimused.
2. Klõpsake valikut Uus.
3. Klõpsake väljal Kliendi konto otsingu avamiseks ripploendi nuppu.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake nuppu OK.
6. Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.
7. Otsige loendist ja valige soovitud kirje.
    * USMF-i kasutamisel võite valida väärtuse D0001.  
8. Sisestage arv väljale Kogus.
9. Klõpsake käsku Lisa rida.
10. Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.
11. Otsige loendist ja valige soovitud kirje.
    * USMF-i kasutamisel võite valida väärtuse T0020.  
12. Klõpsake loendis valitud real olevat linki.
13. Sisestage arv väljale Kogus.
14. Klõpsake nuppu Salvesta.
15. Klõpsake toimingupaanil valikut Müügitellimus.
16. Klõpsake valikut Ostutellimus.
    * Lehel Ostutellimuse loomine on kõik avatud müügitellimuse read, mis on müügitellimuselt kopeeritud. Saate vaadata tellimuse üksikasju ja vajaduse korral muuta valitud üksikasju nagu ostu kogus ja hinnatingimused, enne ostude loomist.  
17. Valige suvand Lisa kõik.
    * Kui soovite luua ostutellimused ainult müügitellimuse ridade alamkogumile, valige need eraldi.  
    * Hankija konto väljal võib juba olla või mitte olla hankija number. Kui tootele on (seotud kauba laovarudes) seadistatud vaikehankija, kopeeritakse reale see hankija. Vastasel korral tuleb hankija sisestada käsitsi.  Selles juhendis, olenemata sellest, kas väljal Hankija konto on juba väärtus või mitte, juhendavad järgmised toimingud teid valima uut hankijat, kes on iga rea puhul erinev.  
18. Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.
19. Otsige loendist ja valige soovitud kirje.
20. Klõpsake loendis valitud real olevat linki.
21. Valige teine tellimuserida.
22. Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.
23. Otsige loendist ja valige soovitud kirje.
24. Klõpsake loendis valitud real olevat linki.
25. Klõpsake suvandit Kinnita.
26. Klõpsake nuppu OK.
    * Sõnum teavitab teid, et loodud on vähemalt üks ostutellimus. Süsteem koostab eraldi ostutellimuse iga hankija puhul, kelle müügitellimuse ridadel määrasite. See tähendab, et kui sama hankija peab tarnima mitu müügitellimuse rida, koostatakse üks mitme reaga ostutellimus.  

## <a name="review-purchase-orders-created-from-sales-orders"></a>Vaadake müügitellimustest loodud ostutellimused üle.
1. Klõpsake toimingupaanil valikut Üldine.
2. Klõpsake valikut Seotud tellimused.
    * Lehel Seotud tellimused on kõik tellimused, mis müügitellimusest loodi. Selles näites on kaks ostutellimust, mis on koostatud vastavalt kahele hankijale.  
3. Klõpsake, et järgida linki väljal Ostutellimus.
    * Iga ostutellimuse rida on seotud müügitellimuse reaga, mis viis ostuni. Seos müügitellimusega on näidatud vahekaardil Toode kiirkaardil Rea üksikasjad väljadel Viite tüüp, Viitenumber ja Viitepartii.  
4. Laiendage või ahendage jaotist Rea üksikasjad.
5. Klõpsake vahekaarti Toode.
    * Viitepartii tagab, et selle ostu kulud kantakse manustatud müügitellimusele.  
    * Saate liikuda algse müügitellimuse juurde, avades lingi väljal Viitenumber.  


