---
title: " Töötaja konfigureerimine"
description: See protseduur näitab, kuidas konfigureerida töötajat müügiesindajana, kellel on õigus komisjonitasule kassa müügilt.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
ms.openlocfilehash: 8bbd3899da8e289dcf82fabc0fd21370655f38e0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276043"
---
# <a name="configure-a-worker"></a> Töötaja konfigureerimine

[!include [banner](../includes/banner.md)]

See protseduur näitab, kuidas konfigureerida töötajat müügiesindajana, kellel on õigus komisjonitasule kassa müügilt. Protseduur kasutab demoettevõtte USRT andmeid.


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
1. Avage Jaemüük ja kaubandus > Töövõtjad > Töötajad.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake loendis valitud real olevat linki.
4. Klõpsake vahekaarti Kaubandus.
    * Töötaja saab määrata müügi vaikegruppi. Müügi vaikegrupp lisatakse kassas automaatselt müügiridadele, kui see valik on kaupluse funktsiooniprofiilis lubatud.  
5. Klõpsake nuppu Redigeeri.
6. Valige või sisestage väärtus väljal Vaikegrupp.
7. Klõpsake nuppu Salvesta.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
