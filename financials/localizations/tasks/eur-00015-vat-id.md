--- 
title: KMK reg-nr seadistamine
description: "See protseduur selgitab KM ID registreerimise eeltingimusi, nt registreerimistüübi seadistamist ja selle määramist registreerimiskategooriale."
author: v-oloski
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: b9db3b66b86f79540145e9da8e2a3dab728b12b8
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-vat-id"></a>KMK reg-nr seadistamine

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur selgitab KM ID registreerimise eeltingimusi, nt registreerimistüübi seadistamist ja selle määramist registreerimiskategooriale. Lisateavet registreerimise ID-de ja registreerimise ID töötlemise kohta, sealhulgas nõutavad eeltingimused, leiate spikriteemast Registreerimise ID-d. 

Siin antud teave kohaldub kõigile Euroopa riikidele/piirkondadele. Ülesande loomisel kasutati demoettevõtte DEMF, mille juriidilise isiku esmaseks aadressiks on Saksamaa, andmeid. See ülesanne on mõeldud süsteemi administraatoritele. See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.

1. Avage Organisatsioonihaldus > Globaalne aadressiraamat > Registreerimistüübid > Registreerimistüübid.
2. Rippdialoogi avamiseks klõpsake valikut Uus.
3. Tippige KM ID väljale Nimi.
4. KM-kood väljal Kirjeldus.
5. Sisestage või valige väärtus DEU väljal Riik/piirkond
6. Tehke väljal Kordumatu valik Jah.
    * Märkige see ruut kontrollimiseks, kas KM ID on kordumatu.  
7. Valige Jah väljal Riigi puhul esmane.
    * Märkige see ruut, kui KM ID peaks kehtima kõigi määratud riigi/regiooni aadresside puhul.  
8. Klõpsake käsku Loo.
9. Klõpsake vahekaarti Lisa.
10. Sisestage või valige väärtus ITA väljal Riik/piirkond
11. Tippige väljale Vorming ###########.
    * Seda tüüpi registreerimisnumbri sisestamisel valitud riigi/piirkonna puhul kontrollitakse registreerimise ID-d selle vormingu suhtes.  
12. Märkige ruut Kordumatu.
    * Märkige see ruut kontrollimiseks, kas KM ID on kordumatu.  
13. Märkige või tühjendage ruut Riigi puhul esmane.
    * Märkige see ruut, kui KM ID peaks kehtima kõigi määratud riigi/regiooni aadresside puhul.  
14. Klõpsake nuppu Salvesta.
15. Avage Organisatsioonihaldus > Globaalne aadressiraamat > Registreerimistüübid > Registreerimiskategooriad.
16. Klõpsake valikut Uus.
17. Sisestage või valige väärtus KM ID, DEU väljal Riik/piirkond
18. Valige väljal Registreerimiskategooria väärtus KM ID.
    * Määrake varem loodud registreerimistüüp eelmääratletud registreerimiskategooriale.  
19. Klõpsake valikut Uus.
20. Sisestage või valige väärtus KM ID, ITA väljal Riik/piirkond
21. Valige väljal Registreerimiskategooria väärtus KM ID.
    * Määrake loodud registreerimistüüp eelmääratletud registreerimiskategooriale.  
22. Klõpsake nuppu Salvesta.


