---
title: Varude saadavuse kontrollimine
description: "See protseduur näitab, kuidas kontrollida vaba kaubavaru ja füüsilist vaba kaubavaru kindla kaubakoodi puhul."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 62338fe11c30781f264e626fad835a2ba9dca837
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="check-the-availability-of-stock"></a>Varude saadavuse kontrollimine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas kontrollida vaba kaubavaru ja füüsilist vaba kaubavaru kindla kaubakoodi puhul. Samuti näitab see, kuidas hankida kaubaga seotud tarneteavet. Füüsiline vaba kaubavaru on vaba kaubavaru, mis on saadaval – s.t see on ostetud, vastu võetud ja registreeritud. Vaba kaubavaru sisaldab saadaolevat vaba kaubavaru, kuid ka varusid, mis on tellitud ja mida oodatakse, aga mida pole veel vastu võetud või registreeritud. Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades. USMF-i kasutamisel saate kasutada kuvatavaid näidisväärtusi. Neid ülesandeid täidab üldjuhul laotöötaja.


## <a name="check-on-hand-inventory-for-an-item"></a>Kauba vaba kaubavaru kontrollimine
1. Avage Laohaldus > Päringud ja aruanded > Vaba kaubavaru.
2. Valige kaubakoodi rida.
    * Vaba kaubavaru päringute esitamiseks kaubakoodi alusel valige rida, kus tabel on seatud vabale kaubavarule ja väli on seatud kaubakoodile.  
3. Valige väljal Kriteeriumid kaup, mille puhul soovite päringu esitada.
    * Ettevõtte USMF demoandmete kasutamisel võite valida väärtuse M9201.  
4. Klõpsake nuppu OK.
5. Klõpsake valikut Dimensioonid.
    * Vahekaart Dimensioonid võimaldab valida, kui palju üksikasju soovite vaba kaubavaru kohta vaadata. Kui teil on vaja reserveerimisega seotud andmeid, peate kuvama kõik täiustatud laotoimingute (WHS) protsesse kasutavate kaupade varude dimensioonid.  
6. Klõpsake nuppu OK.
7. Klõpsake toimingupaanil suvandit Seotud teave.
    * Kui seda ei kuvata, võib teil olla vaja toimingupaani täiendavate suvandite nägemiseks klõpsata kolmikpunkti nuppu (...).  
8. Klõpsake suvandit Tarne ülevaade.
    * Vahekaart Tarne ülevaade pakub tarneteavet kindla kauba, nagu laoseisu koguse, täitmisaja ja hankijateabe kohta.  
9. Laiendage jaotist Laoseis.
10. Laiendage jaotist Hankijad.
11. Sulgege leht.
12. Sulgege leht.

## <a name="check-physical-on-hand-inventory"></a>Füüsilise vaba kaubavaru kontrollimine
1. Avage Laohaldus > Päringud ja aruanded > Füüsiline vaba kaubavaru.
2. Sisestage väärtus väljale Kaubakood.
    * Saate kasutada välju Sait ja Ladu kaupade loendi filtrimiseks.  
3. Värskendage lehte.
4. Klõpsake suvandit Dimensioonide kuvamine.
    * Vahekaart Dimensioonide kuvamine võimaldab teil valida, kui palju üksikasju soovite vaba kaubavaru kohta vaadata.  
5. Klõpsake nuppu OK.
6. Sulgege leht.

## <a name="check-on-hand-inventory-by-location"></a>Vaba kaubavaru kontrollimine asukoha järgi
1. Avage Laohaldus > Päringud ja aruanded > Vaba kaubavaru asukoha järgi.
2. Sisestage väärtus väljale Ladu.
    * Ettevõtte USMF demoandmete kasutamisel saate kasutada suvandit 51.  
3. Värskendage lehte.
4. Klõpsake suvandit Dimensioonide kuvamine.
5. Klõpsake nuppu OK.
6. Sulgege leht.

