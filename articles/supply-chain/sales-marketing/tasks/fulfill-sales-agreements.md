--- 
title: "Müügilepingute täitmine"
description: "See protseduur näitab, kuidas müügilepingut täita, seostades sellega müügitellimused."
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f0894bf962c139c2e9e4c9f8d1589fd933afcedb
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="fulfill-sales-agreements"></a>Müügilepingute täitmine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas müügilepingut täita, seostades sellega müügitellimused. Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega. Enne selle juhendiga alustamist veenduge, et teil on olemas kehtiv müügileping, mille tüüp on Toote väärtuse kohustus. Teine võimalus on käivitada ülesanne nimega Müügilepingute koostamine.  




## <a name="release-a-sales-order-from-the-agreement"></a>Müügitellimuse väljastamine lepingust
1. Avage Müük ja turundus > Müügilepingud > Müügilepingud.
2. Avage loendist leping, mille suhtes soovite tellimuse väljastada.
3. Klõpsake tegumiribal valikut Müügileping.
4. Klõpsake valikut Väljalaskeorder.
    * Nagu lehe Loo väljalaskeorder ülaosas näidatud, erinevad müügitellimuse ridade puhul nõutavad andmed, olenevalt sellest, kas leping on koguse- või väärtusepõhine.  
    * Selles juhendis on lepingu tüüp Toote väärtuse kohustus. Sellepärast on selle lehe ridade jaotis tühi. Kui kohustus põhineks kogusel, kopeeritaks rea teave lepingust.  
5. Klõpsake käsku Loo.
    * Saate teate, et müügitellimus on loodud. Kuna tellimus ei sisalda ühtegi rida, peate vabastusprotsessi lõpuleviimiseks sisestama tellimuserea üksikasjad.   
6. Sulgege leht.
7. Sulgege leht.
8. Avage Müük ja turundus > Müügitellimused > Kõik müügitellimused.
9. Otsige loendist üles ja avage tellimus, mis koostati eelmises ülesandes tellimuse väljastamise tulemusena.
10. Klõpsake käsku Lisa rida.
11. Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.
12. Tippige või valige väljal Kaubakood seotud müügilepingul määratud kaup.
13. Sisestage arv väljale Kogus.
    * Veenduge, et sisestate koguse, mis toob netosumma seotud müügilepingu väärtuse alt.  
    * Pange tähele, et müügitellimus on lepinguga seotud, kokkulepitud allahindluse protsent on tellimuse reale rakendatud.  
14. Klõpsake käsku Värskenda rida.
15. Klõpsake valikut Seotud.
    * Lisatud lepingu lehel on kuvatud selle lepingu ID ja tingimused, millest rida on väljastatud.  
16. Sulgege leht.
17. Klõpsake toimingupaanil valikut Üldine.
18. Klõpsake valikut Manustatud müügileping.
19. Laiendage jaotis Rea üksikasjad.
20. Klõpsake vahekaarti Täitmine.
    * Täitmise vahekaardil on kõigi selle kohustusega seotud müügitellimuse ridade kokkuvõte ja nende täitmise olek ning summa või kogus, mida pole veel väljastatud.   
21. Sulgege leht.
22. Sulgege leht.
23. Sulgege leht.

## <a name="apply-sales-agreement-in-the-order-process"></a>Müügilepingu rakendamine tellimuse protsessis
1. Avage Müük ja turundus > Müügitellimused > Kõik müügitellimused.
2. Klõpsake valikut Uus.
3. Klõpsake väljal Kliendi konto otsingu avamiseks ripploendi nuppu.
4. Otsige loendist üles ja valige müügilepingus määratud klient.
5. Klõpsake loendis valitud real olevat linki.
6. Laiendage jaotist Üldine.
7. Klõpsake väljal Müügilepingu ID otsingu avamiseks ripploendi nuppu.
8. Klõpsake loendis valitud real olevat linki.
9. Klõpsake nuppu Jah.
10. Klõpsake nuppu OK.
11. Märkige loendis valitud rida.
12. Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.
13. Tippige või valige väljal Kaubakood seotud müügilepingul määratud kaup.
14. Klõpsake loendis valitud real olevat linki.
15. Klõpsake nuppu Salvesta.
16. Klõpsake toimingupaanil valikut Komplekteerimine ja pakkimine.
17. Klõpsake valikut Saatelehe sisestamine.
18. Laiendage jaotis Parameetrid.
19. Valige väljal Sisestamine suvand Jah.
20. Klõpsake nuppu OK.
21. Klõpsake nuppu OK.
22. Klõpsake toimingupaanil valikut Üldine.
23. Klõpsake valikut Manustatud müügileping.
24. Klõpsake vahekaarti Täitmine.


