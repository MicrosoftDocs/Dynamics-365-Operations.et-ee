---
title: Kasutajate määramine turberollidesse
description: Rakendustele Finance and Operations juurdepääsuks peavad kasutajatele olema määratud turberollid.
author: Peakerbl
manager: AnnBe
ms.date: 05/06/2020
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
ms.openlocfilehash: f0421ad6c932f2c91de51169bda6c98f53d3bc65
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346441"
---
# <a name="assign-users-to-security-roles"></a>Kasutajate määramine turberollidesse

[!include [banner](../../includes/banner.md)]

Finance and Operations-i rakendustes tavalistest võimalustest enama kasutamiseks tuleb määrata kasutajatele turberoll. Saate määrata kasutajatele rolle automaatselt, tuginedes reeglitele ja äriteabele, välistada kasutajaid automaatsest rollide määramisest või lisada kasutajatele käsitsi rolle.

## <a name="automatically-assign-users-to-roles"></a>Kasutajate automaatsel rollidesse määramine
See protseduur selgitab, kuidas süsteemiadministraatorid saavad automaatselt määrata kasutajatele rolle äriandmete alusel. 
1. Avage **Navigeerimispaan > Moodulid > Süsteemihaldus > Turvalisus > Kasutajate rollidesse määramine**.
2. Tehke puustruktuuris valik Raamatupidaja. Valige roll, millele soovite reegli konfigureerida. Selles näites tehle valik Raamatupidaja. 
3. Dialoogimenüü avamiseks valige käsk **Lisage reegel**.
4. Otsige **Vali päring** loendist ja valige soovitud kirje. Valige päring, mida selle reegli puhul kasutada.  
5. Klõpsake loendis **Liikmesuse reegli nimi** valitud rea linki.
6. Valige **Päringu redigeerimine**. Redigeerige vajaduse korral päringut.  
7. Valige nupp **OK**.
8. Valige **Käivita automaatne rollide määramine**.
9. Avage **Navigeerimispaan > Moodulid > Süsteemihaldus > Kasutajad > Kasutajad** (ideaalis eraldi brauseri vahekaardil).
10. Vaadake üle erinevatele kasutajatele määratud rollid ja veenduge, et rollide määramise päring oleks õige. Kohandage ja käivitage vajaduse korral uuesti.

## <a name="exclude-users-from-automatic-role-assignment"></a>Kasutajate välistamine automaatsest rollimäärangust
1. Sulgege leht.
2. Avage **Navigeerimispaan > Moodulid > Süsteemihaldus > Turvalisus > Kasutajate rollidesse määramine**.
3. Tehke puustruktuuris valik Raamatupidaja. Valige roll. Selles näites tehke valik Raamatupidaja.  
4. Valige menüüs **Rollile määratud kasutajad** suvand **Määra käsitsi / välista kasutajad**.
5. Märkige loendis **Määra kasutajad rollidesse või välista rollidest** valitud rida. Valige kasutaja.  
6. Valige paanil **Toimingupaan** suvand **Välista rollist**.
7. Valige **Välista rollist** valitud kasutajate rollist välistamiseks. Erandite eemaldamiseks valige kasutajad, kelle puhul soovite erandid eemaldada, ja klõpsake seejärel käsku **Lähtesta olek**. Kui eemaldate välistamise, lähtestades kasutaja olek, määratakse kasutaja roll automaatselt. Kuid kasutajale ei määrata kohe rolli ega välistate rolli, kui oleku lähtestate. Selle asemel määratakse kasutajale roll või temalt eemaldatakse roll järgmisel korral, kui käitatakse automaatse rollimäärangu reeglit.  

## <a name="manually-assign-users-to-roles"></a>Kasutajate käsitsi rollidesse määramine
Administraator peab käsitsi turberollidesse määratud kasutajad ka käsitsi eemaldama. Automaatse rollide määramise reeglid neid kasutajaid rollidest ei eemalda.

1. Avage **Navigeerimispaan > Moodulid > Süsteemihaldus > Turvalisus > Kasutajate rollidesse määramine**.
2. Valige puus roll ja menüüs **Rollile määratud kasutajad** suvand **Määra käsitsi / välista kasutajad**.
4. Jaotises **Kasutajate rolli määramine või eemaldamine** on kasutajad, kellele ei ole rolli määratud, loetletud nii, et suvandi **Määrangurežiim** väärtus on **Puudub**. Valige üks või mitu kasutajat, kellele tuleb roll määrata.
5. Valige suvandis **Toimingupaan** valik **Määra rollile**. Suvandis **Määrangurežiim** uuendatakse väärtuseks **Käsitsi** ja kasutajatele on nüüd määratud uus roll.
