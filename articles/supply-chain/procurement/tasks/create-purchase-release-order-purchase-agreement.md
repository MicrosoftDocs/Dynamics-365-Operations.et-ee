---
title: Ostutellimuse loomisel rakendage ostulepingut
description: See protseduur selgitab, kuidas kasutada ostulepingut ostutellimuse loomisel.
author: Henrikan
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 130524dc8e0c8724e35bf13c6b250ab721383711
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570365"
---
# <a name="apply-a-purchase-agreement-when-creating-a-purchase-order"></a>Ostutellimuse loomisel rakendage ostulepingut

[!include [banner](../../includes/banner.md)]

See protseduur selgitab, kuidas kasutada ostulepingut ostutellimuse loomisel. Ostutellimuse loomisel tuleb rakendada ostulepingut, kuna see sisaldab üldtingimusi, mis tuleb kopeerida ostutellimuse päisesse. Seda ülesannet täidab üldjuhul ostuagent. Juhendi eeltingimusena peab teil olema kehtiv ostuleping koos toote koguse kohustusega hankija ja kaupade kohta. Sama protseduuri saab kasutada, kui teil on ostuleping, millel on muud tüüpi kohustusi.

## <a name="create-a-purchase-order"></a>Ostutellimuse loomine

1. Minge **Tootmine ja hankimine \> Tööruumid \> Ostutellimuste ettevalmistus**.
1. Toimingupaanil valige **Uus ostutellimus**.
1. Avaneb dialoogiaken **Loo ostutellimus**. Valige **Hankija konto**. Kontrollige ja korrigeerige teisi aadressivälju vastavalt vajadusele.
1. Suurendage vahekaarti **Üldine**.
1. Väljal **Ostuleping** leidke ja valige tegelik leping, mida soovite kasutada. Siin loetletakse kõik hankija puhul saadaolevad lepped.  
1. Valige **Jah**.
1. Valige nupp **OK**.

## <a name="add-a-line"></a>Lisa rida

1. Sisestage väärtus väljale **Kaubakood**. Kui kohustusel on kindlad varud või asukoha dimensioonid, peate leppe kasutamiseks sisestama sama väärtuse ostutellimuse reale.
1. Valige väljal **Sait** otsingu avamiseks ripploendi nuppu. Tegevuskoht võib olla juba täidetud vaikeväärtusega tellimuselt või hankijalt. Sellisel juhul jätke see etapp vahele.  
1. Otsige loendist ja valige soovitud kirje.
1. Valige loendis link valitud reas.
1. Sisestage arv väljale **Kogus**. Kontrollige, kas hind on kohustusest kopeeritud.  

## <a name="look-up-the-commitment"></a>Kohustuse otsimine

1. Tehke valik **Värskenda liini**.
1. Valige **Manustatud**. Siin saate hankida ostulepingu üksikasjad. Näiteks saate vaadata hinda ning seda, kas hind ja allahindlus on fikseeritud, mis tähendab, et kui muudate ostutellimusel hinna või allahindluse muutmisel muule väärtusele kui on kohustusel, eemaldab süsteem lingi, nii et ostutellimuse rida ei täida kohustust. Näete ka seda, kas suvand Maksimaalne on jõustatud on valitud, mis tähendab, et kohustusel olevat kogust ei saa ületada, summeerides kõik kohustust täitvad ostud.  
1. Sulgege leht.

## <a name="look-up-the-purchase-agreement"></a>Ostulepingu otsimine

1. Valige **Toimingupaanil** suvand **Üldine**.
1. Valige **Ostuleping**.
1. Sulgege leht.
1. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]