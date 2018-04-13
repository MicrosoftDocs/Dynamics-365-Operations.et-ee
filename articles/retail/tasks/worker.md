--- 
title: " Töötaja konfigureerimine"
description: "See protseduur näitab, kuidas konfigureerida jaemüügi töötajat müügiesindajana, kellel on õigus komisjonitasule kassa müügilt."
author: jblucher
manager: AnnBe
ms.date: 02/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 27b075cf1152f16fc4726b224e877eacb2f2572c
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---
# <a name="configure-a-worker"></a> Töötaja konfigureerimine

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

See protseduur näitab, kuidas konfigureerida jaemüügi töötajat müügiesindajana, kellel on õigus komisjonitasule kassa müügilt. Protseduur kasutab demoettevõtte USRT andmeid.


## <a name="create-a-commission-sales-group-for-the-worker"></a>Komisjonimüügi grupi loomine töötajale
1. Tehke valik Müük ja turundus > Komisjonitasud > Müügigrupid.
    * Töötajad saab määrata vähemalt ühte müügigruppi. Kassas saate valida kaupluse aadressiraamatust mis tahes töötajaid sisaldava müügigrupi.  
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Grupp.
4. Sisestage väärtus väljale Nimi.
5. Klõpsake nuppu Salvesta.
6. Klõpsake toimingupaanil valikut Üldine.
7. Klõpsake valikut Müügiesindaja.
    * Müügigrupp võib sisaldada mitut töötajat. Komisjonitasud saab töötajate vahel jagada selle põhjal, kuidas komisjonitasu jagamise määratlete.  
8. Sisestage või valige väärtus väljal Nimi.
9. Sisestage number väljale Komisjonitasu osa.
10. Klõpsake nuppu Salvesta.
11. Sulgege leht.
12. Sulgege leht.

## <a name="assign-the-workers-default-sales-group"></a>Töötajatele müügi vaikegrupi määramine
1. Avage Jaemüük ja kaubandus > Töötajad > Töötajad.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
4. Klõpsake vahekaarti Jaemüük.
    * Töötaja saab määrata müügi vaikegruppi. Müügi vaikegrupp lisatakse kassas automaatselt müügiridadele, kui see valik on kaupluse funktsiooniprofiilis lubatud.  
5. Klõpsake nuppu Redigeeri.
6. Valige või sisestage väärtus väljal Vaikegrupp.
7. Klõpsake nuppu Salvesta.


