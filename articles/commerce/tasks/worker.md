---
title: " Töötaja konfigureerimine"
description: See protseduur näitab, kuidas konfigureerida töötajat müügiesindajana, kellel on õigus komisjonitasule kassa müügilt.
author: jblucher
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 43e65de1fda223c2d0503848e7e57936898c1b73
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804061"
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