---
title: Kasutajate määramine turberollidesse
description: Finance and Operationsi rakendustele juurde pääsemiseks tuleb määrata kasutajatele turberoll.
author: ChrisGarty
manager: AnnBe
ms.date: 09/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4daecc1acd589cd1656402244e5325382a407e7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180963"
---
# <a name="assign-users-to-security-roles"></a>Kasutajate määramine turberollidesse

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tavalistest võimalustest enama kasutamiseks tuleb määrata kasutajatele turberoll. See protseduur selgitab, kuidas süsteemiadministraatorid saavad automaatselt määrata kasutajatele rolle äriandmete alusel. 

## <a name="automatically-assign-users-to-roles"></a>Kasutajate automaatsel rollidesse määramine
1. Avage **Navigeerimispaan > Moodulid > Süsteemihaldus > Turvalisus > Kasutajate rollidesse määramine**.
2. Tehke puustruktuuris valik Raamatupidaja. Valige roll, millele soovite reegli konfigureerida. Selles näites tehle valik Raamatupidaja. 
3. Klõpsake suvandit **Lisa reegel** rippdialoogi avamiseks.
4. Otsige **Vali päring** loendist ja valige soovitud kirje. Valige päring, mida selle reegli puhul kasutada.  
5. Klõpsake loendis **Liikmesuse reegli nimi** valitud rea linki.
6. Klõpsake **Redigeeri päringut**. Redigeerige vajaduse korral päringut.  
7. Klõpsake valikut **OK**.

## <a name="exclude-users-from-automatic-role-assignment"></a>Kasutajate välistamine automaatsest rollimäärangust
1. Sulgege leht.
2. Avage **Navigeerimispaan > Moodulid > Süsteemihaldus > Turvalisus > Kasutajate rollidesse määramine**.
3. Tehke puustruktuuris valik Raamatupidaja. Valige roll. Selles näites tehke valik Raamatupidaja.  
4. Valige menüüs **Rollile määratud kasutajad** suvand **Määra käsitsi / välista kasutajad**.
5. Märkige loendis **Määra kasutajad rollidesse või välista rollidest** valitud rida. Valige kasutaja.  
6. Valige paanil **Toimingupaan** suvand **Välista rollist**.
    
    Klõpsake suvandit **Välista rollist** valitud kasutajate rollist välistamiseks. Erandite eemaldamiseks valige kasutajad, kelle puhul soovite erandid eemaldada, ja klõpsake seejärel käsku **Lähtesta olek**. Kui eemaldate välistamise, lähtestades kasutaja olek, määratakse kasutaja roll uuesti automaatselt. Kuid kasutajale ei määrata kohe rolli ega välistate rolli, kui oleku lähtestate. Selle asemel määratakse kasutajale roll või temalt eemaldatakse roll järgmisel korral, kui käitatakse automaatse rollimäärangu reeglit.  
