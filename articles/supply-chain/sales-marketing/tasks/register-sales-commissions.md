--- 
title: "Müügi komisjonitasude registreerimine"
description: "See protseduur selgitab müügi komisjonitasude arvutamist ja registreerimist."
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 5535f1627526b97ddc9ca2c210db4e332782d656
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="register-sales-commissions"></a>Müügi komisjonitasude registreerimine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur selgitab müügi komisjonitasude arvutamist ja registreerimist. Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega. Enne selle juhendi avamist käivitage juhend „Müügi komisjonitasu reeglite seadistamine” veendumaks, et teil on kõik vajalikud komisjonitasu arvutused seadistatud.

Märkige üles komisjonitasu töötlemiseks valitud kliendi ja kauba koodid ning kasutage neid, kui teil palutakse selles juhendis luua müügitellimus.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Müügiisikule komisjonitasu kvalifitseeriva müügitellimuse arveldamine
1. Avage Müük ja turundus > Müügitellimused > Kõik müügitellimused.
2. Klõpsake valikut Uus.
3. Klõpsake väljal Kliendi konto otsingu avamiseks ripploendi nuppu.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake loendis valitud real olevat linki.
6. Klõpsake nuppu OK.
7. Klõpsake toimingupaanil valikut Suvandid.
8. Klõpsake suvandit Muuda vaadet.
9. Klõpsake suvandit Päisevaade.
10. Laiendage jaotist Seadistus.
    * Väljal Müügigrupp olev väärtus tähistab gruppi koos ühe või mitme sellele määratud müügiesindajaga. Grupis olevad inimesed on need, kes saavad tellimuse arveldamisel komisjonitasu eelmääratletud määrade ja jaotuse järgi.   Väärtus kopeeritakse kliendikaardilt, kuid seda saab soovi korral muuta.  Müügigrupp kopeeritakse ka müügitellimuse reale. Saate seda muuta, nii et see võib päise ja/või ridade vahel erineda.  
    * Välja Komisjonitasu grupp väärtus tähistab gruppi, mille olete loonud ühe või mitme kliendi jaoks komisjonitasude jälgimise eesmärgil.   Väärtus kopeeritakse kliendikaardilt, kuid seda saab soovi korral muuta.   
11. Klõpsake toimingupaanil valikut Suvandid.
12. Klõpsake suvandit Muuda vaadet.
13. Klõpsake suvandit Reavaade.
14. Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.
15. Valige loendist komisjonitasude jaoks seadistatud kaup. 
16. Sisestage arv väljale Kogus.
    * Märkige üles rea netosumma. See tähistab müügitulu, mis siintoodud näites on komisjonitasu arvutamise aluseks.  
17. Klõpsake nuppu Salvesta.
18. Klõpsake toimingupaanil valikut Arve.
19. Klõpsake valikut Arve.
20. Laiendage jaotis Parameetrid.
21. Valige väljal Kogus väärtus Kõik.
22. Valige väljal Sisestamine suvand Jah.
23. Klõpsake nuppu OK.
24. Klõpsake nuppu OK.
    * Kande sisestamiseks võib kuluda ligikaudu minut. Oodake, kuni töötlemine on lõpule jõudnud, ja ärge lehte sulgege.  

## <a name="review-the-registered-sales-commissions"></a>Registreeritud müügi komisjonitasude ülevaatamine
1. Klõpsake toimingupaanil valikut Arve.
2. Klõpsake valikut Arve.
3. Klõpsake toimingupaanil valikut Arve.
4. Klõpsake suvandit Komisjonitasu kanded.
    * Vahekaardil Ülevaade kuvatakse read, mis tähistavad arveldatud müügitellimusega seostatud müügiesindajatele makstavaid komisjonitasu summasid. Vaadakem üksikasjad üle.     
    * Kui kasutasite komisjonitasu müügigrupi seadistamiseks juhendit „Müügi komisjonitasu reeglite seadistamine”, saab müügi komisjonitasu kaks müügiisikut ja komisjonitasu jaotatakse nende vahel võrdselt.  
    * Selle näite puhul arvutatakse komisjonitasu kogusumma protsendina müügitulust (tellimuserea netosummast).   
5. Sulgege leht.
6. Klõpsake suvandit Kanne.
    * Saate üle vaadata komisjonitasu summade kandeid, mis on sisestatud eelmääratletud komisjonitasu kulukontodele ja komisjonitasu ostureskontrotele.  


