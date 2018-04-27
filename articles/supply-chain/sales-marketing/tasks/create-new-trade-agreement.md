--- 
title: Uue kaubandusleppe loomine
description: "See protseduur näitab, kuidas luua kaubanduslepet, kus saate registreerida uue toote müügihinna, mille olete kindla kliendiga kokku leppinud."
author: omulvad
manager: AnnBe
ms.date: 11/11/2016
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
ms.openlocfilehash: 1eb7a945243387f85ec5f38cc3b969d8d030ff25
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-new-trade-agreement"></a>Uue kaubandusleppe loomine

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas luua kaubanduslepet, kus saate registreerida uue toote müügihinna, mille olete kindla kliendiga kokku leppinud. Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega. Kui kasutate oma andmeid, peate enne selle juhendi käivitamist veenduma, et oleks olemas kaubandusleppe tööleht, kus suvandi Vaikeseos sätteks on valitud Hind (müük).


## <a name="create-and-post-a-new-trade-agreement-journal"></a>Uue kaubandusleppe töölehe loomine ja sisestamine
1. Avage Müük ja turundus > Hinnad ja allahindlused > Kaubandusleppe töölehed.
2. Klõpsake valikut Uus.
3. Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.
4. Otsige loendist ja valige soovitud kirje.
5. Klõpsake loendis valitud real olevat linki.
6. Klõpsake valikut Read.
7. Valige väljal Konto kood suvand Tabel.
    * Selles näites värskendate hinda teatud kliendi puhul, mis tähendab, et peate valima suvandi Tabel. Kui värskendasite toote hinnakirja, siis valige suvand Kõik, et uus hind kehtiks kõikide klientide jaoks. Kui määrasite erinevatele kliendisektoritele erinevad hinnad, siis valige suvand Grupp. Suvandi Grupp valimiseks peate seadistama kliendi hinnagrupid.  
8. Klõpsake väljal Konto valik otsingu avamiseks ripploendi nuppu.
9. Otsige loendist ja valige soovitud kirje.
10. Valige väljal Kaubakood suvand Tabel.
    * Kui sisestate kaubandusleppe, mille tüüp on Hind (müük), peate valima kaubakoodi väljal ainult suvandi Tabel. Põhjuseks on see, et hind on absoluutväärtus ning ei saa olla kõigi toodete või tootegrupi puhul olla sama.  
11. Klõpsake väljal Kauba seos otsingu avamiseks ripploendi nuppu.
12. Valige loendist toode, mille soovite leppesse kaasata.
    * Märkige üles, millise toote valisite.  
13. Klõpsake loendis valitud real olevat linki.
14. Sisestage miinimumkogus väljale Alates.
    * Kui klient peab tellima miinimumkoguse, enne kui kvalifitseerub uue hinna saamiseks, peate määrama selle koguse siin.  
    * Sisestage väärtus väljale Kuni, et määrata maksimaalne kogus, üle mille leppe hind ei kehti. Kui pakute hindu ja allahindlusi mitme kogusekatkestuse põhjal, määrake iga koguserühm miinimum- ja maksimumkoguse paarina vastavalt väljadel Alates ja Kuni.  
15. Sisestage hind väljale Summa valuutas.
16. Sisestage väljale Alates kuupäev, millest alates see lepe kehtib.
17. Klõpsake nuppu Salvesta.
18. Klõpsake suvandit Kinnita.
19. Klõpsake suvandit Kinnita valitud read.
20. Klõpsake nuppu OK.
21. Klõpsake valikut Sisesta.
22. Klõpsake nuppu OK.

## <a name="view-trade-agreements-for-a-product"></a>Toote kaubanduslepete kuvamine
1. Avage Tooteteabe haldus > Tooted > Väljastatud tooted.
2. Leidke ja valige loendist toode, mille hinda äsja värskendasite.
3. Klõpsake toimingupaanil suvandit Müük.
4. Klõpsake suvandit Kuva kaubanduslepped.
    * Vaadake üle äsjaloodud hinna kaubandusleppe üksikasjad.    
5. Sulgege leht.


