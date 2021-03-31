---
title: EUR-00015 KM ID seadistamine
description: See protseduur selgitab KM ID registreerimise eeltingimusi, nt registreerimistüübi seadistamist ja selle määramist registreerimiskategooriale.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxRegistrationType, TaxRegistrationTypeCreate, TaxRegistrationLegislationTypes
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c4a05cd22a50396b1767fea387be46305210763
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227917"
---
# <a name="eur-00015-set-up-vat-id"></a>EUR-00015 KM ID seadistamine

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]