--- 
title: "Kasutajate määramine turberollidesse"
description: "Rakendusele Microsoft Dynamics 365 for Finance and Operations, Enterprise edition tuleb määrata kasutajatele turberoll."
author: maertenm
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 551048af26f46d334c562d1968963aed262a5e03
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="assign-users-to-security-roles"></a>Kasutajate määramine turberollidesse

[!include[task guide banner](../../includes/task-guide-banner.md)]

Rakendusele Microsoft Dynamics 365 for Finance and Operations, Enterprise edition tuleb määrata kasutajatele turberoll. See protseduur selgitab, kuidas süsteemiadministraatorid saavad määrata kasutajatele automaatselt rolle äriandmete alusel. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="automatically-assign-users-to-roles"></a>Kasutajate automaatsel rollidesse määramine
1. Minge jaotisesse Süsteemihaldus > Turve > Kasutajate rollidesse määramine.
2. Tehke puustruktuuris valik Raamatupidaja.
    * Valige roll, millele soovite reegli konfigureerida. Selles näites tehle valik Raamatupidaja.  
3. Klõpsake suvandit Lisa reegel rippdialoogi avamiseks.
4. Otsige loendist ja valige soovitud kirje.
    * Valige päring, mida selle reegli puhul kasutada.  
5. Klõpsake loendis valitud real olevat linki.
6. Klõpsake suvandit Redigeeri päringut.
    * Redigeerige vajaduse korral päringut.  
7. Klõpsake nuppu OK.

## <a name="exclude-users-from-automatic-role-assignment"></a>Kasutajate välistamine automaatsest rollimäärangust
1. Sulgege leht.
2. Minge jaotisesse Süsteemihaldus > Turve > Kasutajate rollidesse määramine.
3. Tehke puustruktuuris valik Raamatupidaja.
    * Valige roll. Selles näites tehke valik Raamatupidaja.  
4. Klõpsake suvandit Kasutajate käsitsi määramine/välistamine.
5. Märkige loendis valitud rida.
    * Valige kasutaja.  
6. Klõpsake suvandit Välista rollist.
    * Klõpsake suvandit Välista rollist valitud kasutajate rollist välistamiseks. Erandite eemaldamiseks valige kasutajad, kelle puhul soovite erandid eemaldada, ja klõpsake seejärel käsku Lähtesta olek. Kui eemaldate välistamise, lähtestades kasutaja olek, määratakse kasutaja roll uuesti automaatselt. Kuid kasutajale ei määrata kohe rolli ega välistate rolli, kui oleku lähtestate. Selle asemel määratakse kasutajale roll või temalt eemaldatakse roll järgmisel korral, kui käitatakse automaatse rollimäärangu reeglit.  


