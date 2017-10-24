--- 
title: "Müügitellimuste kinnitamine"
description: "See protseduur näitab, kuidas kinnitada müügitellimusi."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7cab69222c5004e6a62c632a9e85085403434ffd
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="confirm-sales-orders"></a>Müügitellimuste kinnitamine

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas kinnitada müügitellimusi. Teile selgitatakse üksiku tellimuse kinnitamist ja mitme tellimuse korraga kinnitamist. Neid ülesandeid täidab üldjuhul müügitellimuse töötleja. Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades. Enne alustamist veenduge, et sama kliendi jaoks oleks mitu avatud müügitellimust. Kui kasutate USMF-i, saate kasutada klienti US-027.


## <a name="confirm-a-single-sales-order"></a>Üksiku müügitellimuse kinnitamine
1. Avage Müük ja turundus > Müügitellimused > Kõik müügitellimused.
2. Leidke ja valige loendist tellimus, mille soovite kinnitada.
3. Klõpsake müügitellimuse numbris linki valitud tellimuse avamiseks.
4. Klõpsake toimingupaanil suvandit Müük.
5. Klõpsake suvandit Müügitellimuse kinnitamine.
6. Laiendage või ahendage jaotist Parameetrid.
    * Veenduge, et väli Sisestamine: jah oleks aktiivne.  
7. Määrake suvandi Kinnituse printimine sätteks Jah.
    * Väli Krediidilimiidi kontrolli määrab kliendi järelejäänud krediidi arvutamise meetodi. Vaikimisi kopeeritakse see lehelt Müügireskontro parameetrid. Kui soovite kindla müügitellimuse kinnitamisel krediidilimiidi kontrolli vahele jätta, valige suvandi Kontrolli krediidilimiiti sätteks Puudub. Siiski tuleb arvestada, et isegi kui selle välja sätteks on valitud Puudub, tehakse krediidilimiidi kontroll ikkagi, kui kliendi põhiandmetes on valitud suvand Kohustuslik krediidilimiit.  
8. Klõpsake nuppu OK.
9. Klõpsake nuppu Jah.
10. Sulgege leht.
11. Klõpsake toimingupaanil valikut Suvandid.
12. Klõpsake suvandit Muuda vaadet.
13. Klõpsake suvandit Päisevaade.
    * Kui tellimus on kinnitatud, määratakse suvandi Dokumendi olek sätteks Kinnitus.  
14. Klõpsake toimingupaanil suvandit Müük.
15. Klõpsake suvandit Müügitellimuse kinnitus.
16. Sulgege leht.

## <a name="confirm-multiple-sales-orders-at-once"></a>Mitme müügitellimuse korraga kinnitamine
1. Avage Müük ja turundus > Müügitellimused > Tellimuse kinnitus > Müügitellimuse kinnitamine.
2. Klõpsake Vali.
3. Leidke ja valige vahekaardil Vahemik olevast loendist kirje, mis viitab väljale Kliendikonto.
4. Klõpsake väljal Kriteeriumid otsingu avamiseks ripploendi nuppu.
5. Leidke ja valige loendist kliendikonto, millel on mitu tellimust, mida soovite korraga kinnitada.
    * Kui kasutate USMF-i, saate valida konto US-027.  
6. Klõpsake nuppu OK.
    * Vahekaardil Ülevaade kuvatakse loend tellimustest, mis vastavad päringukriteeriumile. Need kaasatakse kinnitusse.  
    * Väli Koondsisestamine määrab parameetri, mille järgi koondatakse mitu tellimust ühte kinnitusdokumenti. Vaikimisi kopeeritakse suvand lehel Müügireskontro parameetrid sättest Koondsisestuse vaikeväärtused.  
7. Valige väljal Koondsisestamine suvand Tellimus.
    * Koondsisestuste loomiseks nõutavad minimaalsed parameetrid on Arvekonto ja Valuuta. See tähendab, et erinevate arvekontode ja erinevate valuutadega koondsisestused pole lubatud. Koondsisestuse parameetrid saab seadistada lehel Koondsisestuste parameetrid, millele pääseb juurde lehelt Müügireskontro parameetrid.  
8. Klõpsake väljal Müügitellimus otsingu avamiseks ripploendi nuppu.
9. Valige loendist tellimuse number, mis peaks olema koondtellimus.
10. Klõpsake suvandit Korralda.
11. Klõpsake nuppu OK.
12. Klõpsake nuppu OK.


