---
title: Ostu väljalaskeorderi loomine ostulepingu põhjal
description: See protseduur selgitab, kuidas kasutada ostulepingut ostutellimuse loomisel.
author: mkirknel
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee0c40dfc3c820343c7054238cc2da47e8203d59
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426199"
---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a>Ostu väljalaskeorderi loomine ostulepingu põhjal

[!include [banner](../../includes/banner.md)]

See protseduur selgitab, kuidas kasutada ostulepingut ostutellimuse loomisel. Ostutellimuse loomisel tuleb rakendada ostulepingut, kuna see sisaldab üldtingimusi, mis tuleb kopeerida ostutellimuse päisesse. Seda ülesannet täidab üldjuhul ostuagent. Juhendi eeltingimusena peab teil olema kehtiv ostuleping koos toote koguse kohustusega hankija ja kaupade kohta. Sama protseduuri saab kasutada, kui teil on ostuleping, millel on muud tüüpi kohustusi. Saate selle juhendi käitada demoettevõtte USMF andmetega. Kui kasutate USMF-i, saate esmalt käivitada juhendi „Ostulepingu loomine”, et seadistada selle juhendi jaoks vajalikud eeltingimused.


## <a name="create-a-purchase-order"></a>Ostutellimuse loomine
1. Paanil **Navigeerimispaan** avage **Tööruumid > Ostutellimuse ettevalmistus**. 
2. Klõpsake **Uus ostutellimus**.
3. Klõpsake väljal **Hankija konto** otsingu avamiseks ripploendi nuppu.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake loendis valitud real olevat linki.
6. Suurendage vahekaarti **Üldine**.
7. Väljal **Ostuleping** klõpsake rippmenüü nuppu, et avada otsing. Siin loetletakse kõik hankija puhul saadaolevad lepped. Leidke kehtiv lepe, mida soovite kasutada.  
8. Klõpsake loendis valitud real olevat linki.
9. Klõpsake nuppu **Jah**.
10. Klõpsake valikut **OK**.

## <a name="add-a-line"></a>Rea lisamine
1. Sisestage väärtus väljale **Kaubakood**. Kui kohustusel on kindlad varud või asukoha dimensioonid, peate leppe kasutamiseks sisestama sama väärtuse ostutellimuse reale.  
2. Klõpsake väljal **Sait** otsingu avamiseks ripploendi nuppu. Tegevuskoht võib olla juba täidetud vaikeväärtusega tellimuselt või hankijalt. Sellisel juhul jätke see etapp vahele.  
3. Otsige loendist ja valige soovitud kirje.
4. Klõpsake loendis valitud real olevat linki.
5. Sisestage arv väljale **Kogus**. Kontrollige, kas hind on kohustusest kopeeritud.  

## <a name="look-up-the-commitment"></a>Kohustuse otsimine
1. Klõpsake nuppu **Värskenda rida**.
2. Klõpsake nuppu **Manustatud**. Siin saate hankida ostulepingu üksikasjad. Näiteks saate vaadata hinda ning seda, kas hind ja allahindlus on fikseeritud, mis tähendab, et kui muudate ostutellimusel hinna või allahindluse muutmisel muule väärtusele kui on kohustusel, eemaldab süsteem lingi, nii et ostutellimuse rida ei täida kohustust. Näete ka seda, kas suvand Maksimaalne on jõustatud on valitud, mis tähendab, et kohustusel olevat kogust ei saa ületada, summeerides kõik kohustust täitvad ostud.  
3. Sulgege leht.

## <a name="look-up-the-purchase-agreement"></a>Ostulepingu otsimine
1. Paanil **Toimingupaan** klõpsake **Üldine**.
2. Klõpsake **Ostutellimus**.
3. Sulgege leht.
4. Sulgege leht.

