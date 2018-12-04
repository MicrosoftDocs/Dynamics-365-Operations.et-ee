--- 
title: "Ostu väljalaskeorderi loomine ostutellimuse koostamisel"
description: See protseduur selgitab, kuidas kasutada ostulepingut ostutellimuse loomisel.
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 194d811da09c746167bd9489ce39ae6a6f810ec0
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-release-order-when-creating-the-purchase-order"></a>Ostu väljalaskeorderi loomine ostutellimuse koostamisel

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur selgitab, kuidas kasutada ostulepingut ostutellimuse loomisel. Ostutellimuse loomisel tuleb rakendada ostulepingut, kuna see sisaldab üldtingimusi, mis tuleb kopeerida ostutellimuse päisesse. Seda ülesannet täidab üldjuhul ostuagent. Juhendi eeltingimusena peab teil olema kehtiv ostuleping koos toote koguse kohustusega hankija ja kaupade kohta. Sama protseduuri saab kasutada, kui teil on ostuleping, millel on muud tüüpi kohustusi. Saate selle juhendi käitada demoettevõtte USMF andmetega. Kui kasutate USMF-i, saate esmalt käivitada juhendi „Ostulepingu loomine”, et seadistada selle juhendi jaoks vajalikud eeltingimused.


## <a name="create-a-purchase-order"></a>Ostutellimuse loomine
1. Avage ostutellimuse ettevalmistamise tööruum.
2. Klõpsake suvandit Uus ostutellimus.
3. Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake loendis valitud real olevat linki.
6. Lülitage jaotise Üldine laiendamist.
7. Klõpsake väljal Ostuleping otsingu avamiseks ripploendi nuppu.
    * Siin loetletakse kõik hankija puhul saadaolevad lepped. Leidke kehtiv lepe, mida soovite kasutada.  
8. Klõpsake loendis valitud real olevat linki.
9. Klõpsake nuppu Jah.
10. Klõpsake nuppu OK.

## <a name="add-a-line"></a>Rea lisamine
1. Sisestage väärtus väljale Kaubakood.
    * Kui kohustusel on kindlad varud või asukoha dimensioonid, peate leppe kasutamiseks sisestama sama väärtuse ostutellimuse reale.  
2. Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.
    * Tegevuskoht võib olla juba täidetud vaikeväärtusega tellimuselt või hankijalt. Sellisel juhul jätke see etapp vahele.  
3. Otsige loendist ja valige soovitud kirje.
4. Klõpsake loendis valitud real olevat linki.
5. Sisestage arv väljale Kogus.
    * Kontrollige, kas hind on kohustusest kopeeritud.  

## <a name="look-up-the-commitment"></a>Kohustuse otsimine
1. Klõpsake käsku Värskenda rida.
2. Klõpsake valikut Seotud.
    * Siin saate hankida ostulepingu üksikasjad. Näiteks saate vaadata hinda ning seda, kas hind ja allahindlus on fikseeritud, mis tähendab, et kui muudate ostutellimusel hinna või allahindluse muutmisel muule väärtusele kui on kohustusel, eemaldab süsteem lingi, nii et ostutellimuse rida ei täida kohustust. Näete ka seda, kas suvand Maksimaalne on jõustatud on valitud, mis tähendab, et kohustusel olevat kogust ei saa ületada, summeerides kõik kohustust täitvad ostud.  
3. Sulgege leht.

## <a name="look-up-the-purchase-agreement"></a>Ostulepingu otsimine
1. Klõpsake toimingupaanil valikut Üldine.
2. Klõpsake suvandit Ostuleping.
3. Sulgege leht.
4. Sulgege leht.


