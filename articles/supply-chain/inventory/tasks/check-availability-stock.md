---
title: Varude saadavuse kontrollimine
description: See protseduur näitab, kuidas kontrollida vaba kaubavaru ja füüsilist vaba kaubavaru kindla kaubakoodi puhul.
author: ShylaThompson
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand, InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 894c153761dc29e3d5d9fc22900d96a50ae33b6d5db92623118e229a9aedafe4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758636"
---
# <a name="check-the-availability-of-stock"></a>Varude saadavuse kontrollimine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas kontrollida vaba kaubavaru ja füüsilist vaba kaubavaru kindla kaubakoodi puhul. Samuti näitab see, kuidas hankida kaubaga seotud tarneteavet. Füüsiline vaba kaubavaru on vaba kaubavaru, mis on saadaval – st see on ostetud, vastu võetud ja registreeritud. Vaba kaubavaru sisaldab saadaolevat vaba kaubavaru, kuid ka varusid, mis on tellitud ja mida oodatakse, aga mida pole veel vastu võetud või registreeritud. Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades. USMF-i kasutamisel saate kasutada kuvatavaid näidisväärtusi. Neid ülesandeid täidab üldjuhul laotöötaja.


## <a name="check-on-hand-inventory-for-an-item"></a>Kauba vaba kaubavaru kontrollimine
1. Avage **Navigeerimisriba > Moodulid > Varude haldus > Päringud ja aruanded > Vaba kaubavaru**.
2. Valige rida **Kaubakood**. Vaba kaubavaru päringute esitamiseks kaubakoodi alusel valige rida, kus tabel on seatud **Vabal kaubavarule** ja väli on seatud **Kauba** koodile.
3. Valige väljal **Kriteeriumid** kaup, mille puhul soovite päringu esitada. Ettevõtte USMF demoandmete kasutamisel võite valida väärtuse M9201.  
4. Klõpsake valikut **OK**.
5. Klõpsake **Toimingupaanil** valikut **Dimensioonid**. Vahekaart **Dimensioonid** võimaldab valida, kui palju üksikasju soovite vaba kaubavaru kohta vaadata. Kui teil on vaja reserveerimisega seotud andmeid, peate kuvama kõik täiustatud laotoimingute (WMS) protsesse kasutavate kaupade varude dimensioonid.
6. Klõpsake valikut **OK**.
7. Klõpsake **Toimingupaanil** suvandit **Seotud teave**. Kui seda valikut ei kuvata, võib teil olla vaja toimingupaani täiendavate suvandite nägemiseks klõpsata kolmikpunkti nuppu (...).
8. Klõpsake suvandit **Tarne ülevaade**. Vahekaart **Tarne ülevaade** pakub tarneteavet kindla kauba, nagu laoseisu koguse, täitmisaja ja hankijateabe kohta.  
9. Laiendage jaotist **Laoseis**.
10. Laiendage jaotist **Hankijad**.
11. Sulgege leht.
12. Sulgege leht.

## <a name="check-physical-on-hand-inventory"></a>Füüsilise vaba kaubavaru kontrollimine
1. Avage **Navigeerimisriba > Moodulid > Laohaldus > Päringud ja aruanded > Füüsiline vaba kaubavaru**.
2. Sisestage väärtus väljale **Kaubakood**. Saate kasutada välju Sait ja Ladu kaupade loendi filtrimiseks. 
3. Värskendage lehte.
4. Klõpsake **Toimingupaanil** valikut **Kuva dimensioonid**. Vahekaart Dimensioonide kuvamine võimaldab teil valida, kui palju üksikasju soovite vaba kaubavaru kohta vaadata.
5. Klõpsake valikut **OK**.
6. Sulgege leht.

## <a name="check-on-hand-inventory-by-location"></a>Vaba kaubavaru kontrollimine asukoha järgi
1. Avage **Navigeerimisriba > Moodulid > Laohaldus > Päringud ja aruanded > Kaubavaru asukoha järgi**.
2. Sisestage väärtus väljale **Ladu**. Ettevõtte USMF demoandmete kasutamisel saate kasutada suvandit 51.  
3. Värskendage lehte.
4. Klõpsake suvandit **Dimensioonide kuvamine.**
5. Klõpsake valikut **OK**.
6. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]