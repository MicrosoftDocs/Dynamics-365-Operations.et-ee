--- 
title: "Elektrooniline aruandlus. Vormingu täiendamine uue alusversiooni kasutuselevõtuga"
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad hallata elektroonilise aruandluse (ER) vormingu konfiguratsiooni."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 040505f567b9db1a5987e4ada38d46f919440c96
ms.contentlocale: et-ee
ms.lasthandoff: 09/14/2018

---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a>Elektrooniline aruandlus. Vormingu täiendamine uue alusversiooni kasutuselevõtuga

[!include [task guide banner](../../includes/task-guide-banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad hallata elektroonilise aruandluse (ER) vormingu konfiguratsiooni. Selles protseduuris selgitatakse, kuidas saab luua vormingu kohandatud versiooni konfiguratsiooni pakkujalt (CP) saadud vormingu alusel. Selgitatakse ka seda, kuidas võtta kasutusele selle vormingu uus alusversioon.



Nende etappide lõpuleviimiseks peate kõigepealt lõpetama etapid protseduurides „Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” ja „Loodud vormingu kasutamine maksete jaoks elektrooniliste dokumentide loomiseks”. Neid toiminguid saab teha GBSI ettevõttes.


## <a name="select-format-configuration-for-customization"></a>Vormingu konfiguratsiooni valimine kohandamiseks
1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
    * Selles näites on näidisettevõte Litware, Inc. (http://www.litware.com) konfiguratsiooni pakkuja, mis toetab kindla riigi elektrooniliste maksete vormingu konfiguratsioone.    Näidisettevõte Proseware, Inc. (http://www.proseware.com) on selle vormingukonfiguratsiooni tarbija, mida pakub Litware, Inc. Proseware, Inc. kasutab vorminguid selle riigi teatud piirkondades.  
2. Klõpsake valikut Aruandluse konfiguratsioonid.
3. Klõpsake suvandit Näita filtreid.
4. Rakendage järgmised filtrid: sisestage filtri väärtus „BACS (UK fiktiivne)” väljale „Nimi”, kasutades filtri tehtemärki „algab üksusega”,
    * BACS (UK fiktiivne)  
    * Valitud vormingu konfiguratsiooni BACS (UK fiktiivne) omanik on pakkuja Litware, Inc.  
5. Klõpsake suvandit Näita filtreid.
6. Otsige loendist ja valige soovitud kirje.
    * Proseware, Inc. kasutab isikupärastamiseks vormingu versiooni olekuga Lõpule viidud.  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a>Elektroonilise dokumendi kohandatud vormingule uue konfiguratsiooni loomine
    * Proseware, Inc. sai ettevõttelt Litware, Inc vastavalt nende teenusekirjeldusele BACS-i (UK fiktiivne) konfiguratsiooniversiooni 1.1, mis sisaldab algset vormingut elektrooniliste maksedokumentide loomiseks. Proseware, Inc. soovib hakata seda kasutama oma riigi standardina, kuid nõutavad on mõned kohandamised, et toetada teatud piirkondlikke nõudeid. Proseware, Inc. soovib säilitada ka võime täiendada kohandatud vormingut niipea kui selle uus versioon (koos muudatustega uute riigipõhiste nõuete toetamiseks) ettevõttelt Litware, Inc. välja antakse ja soovib täienduse läbi viia võimalikult väikeste kuludega.  Selleks peab Proseware, Inc. looma konfiguratsiooni, kasutades alusena Litware, Inc. konfiguratsiooni BACS (UK fiktiivne).  
1. Sulgege leht.
2. Valige Proseware, Inc, et muuta see aktiivseks pakkujaks.
3. Klõpsake valikut Määra aktiivseks.
4. Klõpsake valikut Aruandluse konfiguratsioonid.
5. Laiendage puustruktuuris suvandit Maksed (lihtsustatud mudel).
6. Tehke puustruktuuris valik 'Maksed (lihtsustatud mudel)\BACS (UK fiktiivne)'.
    * Valige ettevõtte Litware, Inc. pakutav BACS (UK fiktiivne). Proseware, Inc. kasutab väljaannet 1.1 kohandatud versiooni alusena.  
7. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
    * See võimaldab teil luua uut konfiguratsiooni kohandatud maksevormingule.  
8. Sisestage väljale Uus tekst 'Tuleta nimest: BACS (UK fiktiivne), Litware, Inc.'.
    * Valige suvand Tuleta, et kinnitada BACS-i (UK fiktiivne) kasutamine kohandatud versiooni loomise alusena.  
9. Tippige väljale Nimi tekst 'BACS (UK fiktiivne kohandatud)'.
    * BACS (UK fiktiivne kohandatud)  
10. Väljale Kirjeldus tippige „BACS-i hankija makse (UK fiktiivne kohandatud)”.
    * BACS-i hankija makse (UK fiktiivne kohandatud)  
    * Aktiivse konfiguratsiooni pakkuja (Proseware, Inc.) sisestatakse siia automaatselt. See pakkuja saab seda konfiguratsiooni hallata. Muud pakkujad saavad seda konfiguratsiooni kasutada, kuid ei saa seda hallata.  
11. Klõpsake Loo konfiguratsioon.

## <a name="customize-your-format-for-the-electronic-document"></a>Elektroonilise dokumendi jaoks vormingu kohandamine
1. Klõpsake valikut Kujundaja.
2. Klõpsake nuppu Laienda/ahenda.
3. Klõpsake nuppu Laienda/ahenda.
4. Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Pank”.
5. Klõpsake valikut Lisa rippdialoogi avamiseks.
6. Valige puul suvand XML\Element.
7. Sisestage väljale Nimi suvand IBAN.
    * IBAN  
8. Klõpsake nuppu OK.
9. Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Pank\IBAN”.
10. Klõpsake valikut Lisa rippdialoogi avamiseks.
11. Valige puul suvand Tekst\String.
12. Klõpsake nuppu OK.
13. Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Nimi\String”.
14. Sisestage väljale Maksimaalne pikkus väärtus '60'.
15. Klõpsake vahekaarti Vastendus.
16. Laiendage puus sõlme „model”.
17. Laiendage puus sõlme model\Payments.
18. Laiendage puus sõlme model\Payments\Creditor.
19. Laiendage puus sõlme model\Payments\Creditor\Account.
20. Puuvaates valige „mudel\Maksed\Kreeditor\Konto\IBAN”.
21. Puuvaates valige „Xml\Teade\Maksed\Kaup = model.Payments\Hankija\Pank\IBAN\String”.
22. Klõpsake valikut Seo.
23. Klõpsake nuppu Salvesta.

## <a name="validate-the-customized-format"></a>Kohandatud vormingu kinnitamine
1. Klõpsake suvandit Kinnita.
    * Kinnitage kohandatud vormingu paigutus ja andmete vastendamise muudatused veendumaks, et kõik seosed on korras.  
2. Sulgege leht.

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a>Kohandatud vormingu konfiguratsiooni praeguse versiooni oleku muutmine
    * Muutke koostatud vormingu konfiguratsiooni olek suvandilt Mustand suvandile Lõpetatud, et muuta see maksedokumedi loomiseks kättesaadavaks.  
1. Klõpsake valikut Muuda olekut.
    * Pange tähele, et valitud konfiguratsiooni praegune versioon on olekus Mustand.  
2. Klõpsake valikut Valmis.
3. Sisestage väljale Kirjeldus soovitud väärtus.
4. Klõpsake nuppu OK.
5. Otsige loendist ja valige soovitud kirje.
    * Pange tähele, et loodud konfiguratsioon salvestatakse kui lõpetatud versioon 1.1.1. See tähendab, et see on kohandatud BACS-i (UK fiktiivne kohandatud) vormingu 1. versioon, mis põhineb BACS-i (UK fiktiivne) vormingu 1. versioonil, mis põhineb andmemudeli Maksed (lihtsustatud mudel) 1. versioonil.  

## <a name="test-the-customized-format-to-generate-payment-files"></a>Kohandatud vormingu testimine maksefailide loomiseks
    * Viige rakenduse Dynamics 365 for Finance and Operations, Enterprise edition paralleelseansis lõpule protseduur „Loodud vormingu kasutamine maksete jaoks elektrooniliste dokumentide loomiseks”. Valige BACS-i (UK fiktiivne kohandatud) vorming elektroonilise makseviisi parameetrites. Veenduge, et loodud maksefail sisaldab hiljuti kasutusele võetud XML-sõlme IBAN-koodiga vastavalt piirkondlikele nõuetele.  

## <a name="update-the-existing-country-specific-configuration"></a>Olemasoleva riigipõhise konfiguratsiooni värskendamine
    * Litware, Inc. peab värskendama BACS-i (UK fiktiivne) konfiguratsiooni ja kasutusele võtma uued riigipõhised nõuded, et hallata elektroonilise dokumendi vormingut. Hiljem lisatakse see selle konfiguratsiooni uude versiooni, mida pakutakse teenuse tellijatele, sh ettevõttele Proseware, Inc.  
    * Tegelikes teenuse osutamisega seotud protsessides saab Proseware, Inc. importida iga uue BACS-i (UK fiktiivne) väljaande ettevõtte Litware, Inc. konfiguratsioonide LCS-hoidlast. Selles protseduuris simuleerime seda, värskendades BACS-i (UK fiktiivne) teenusepakkuja nimel.  
1. Sulgege leht.
2. Valige pakkuja Litware, Inc.
3. Klõpsake valikut Määra aktiivseks.
4. Klõpsake valikut Aruandluse konfiguratsioonid.
5. Laiendage puustruktuuris suvandit Maksed (lihtsustatud mudel).
6. Tehke puustruktuuris valik 'Maksed (lihtsustatud mudel)\BACS (UK fiktiivne)'.
    * Ettevõtte Litware, Inc omandis mustandversioon pakkuja BACS (UK fiktiivne) on valitud toomaks kaasa muudatusi, et toetada uusi riigipõhiseid nõudeid.  

## <a name="localize-the-base-format-of-the-electronic-document"></a>Elektroonilise dokumendi alusvormingu lokaliseerimine
    * Oletame, et on olemas uued riigipõhised nõuded, mida Litware, Inc. peab täitma: iga makse puhul kreeditori panga SWIFT-koodi väärtus.  - 100 tähemärgi piirang hankija nime tekstipikkusele loomisfailis.  
    * Uued riigipõhised nõuded  
    * Valige soovitud konfiguratsiooni mustandiversioon, et nõutavad muudatused kasutusele võtta.  
1. Klõpsake valikut Kujundaja.
2. Klõpsake nuppu Laienda/ahenda.
3. Klõpsake nuppu Laienda/ahenda.
4. Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Pank”.
5. Klõpsake valikut Lisa rippdialoogi avamiseks.
6. Valige puul suvand XML\Element.
7. Sisestage väljale Nimi suvand SWIFT.
    * SWIFT  
8. Klõpsake nuppu OK.
9. Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Pank\SWIFT”.
10. Klõpsake valikut Lisa rippdialoogi avamiseks.
11. Valige puul suvand Tekst\String.
12. Klõpsake nuppu OK.
13. Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Nimi\String”.
14. Sisestage väljale Maksimaalne pikkus väärtus '100'.
15. Klõpsake vahekaarti Vastendus.
16. Laiendage puus sõlme „model”.
17. Laiendage puus sõlme model\Payments.
18. Laiendage puus sõlme model\Payments\Creditor.
19. Laiendage puus sõlme model\Payments\Creditor\Agent.
20. Puuvaates valige „mudel\Maksed\Kreeditor\Agent\SWIFT”.
21. Puuvaates valige „Xml\Teade\Maksed\Kaup = model.Payments\Hankija\Pank\SWIFT\String”.
22. Klõpsake valikut Seo.
23. Klõpsake nuppu Salvesta.

## <a name="validate-the-localized-format"></a>Lokaliseeritud vormingu kinnitamine
1. Klõpsake suvandit Kinnita.
2. Sulgege leht.

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a>Alusvormingu konfiguratsiooni praeguse versiooni oleku muutmine
    * Muutke värskendatud alusvormingu konfiguratsiooni olek suvandist Mustand suvandiks Lõpetatud, et teha see kättesaadavaks maksedokumentide loomiseks ja sellest tuletatud vormingu konfiguratsioonide värskendusteks.  
1. Klõpsake valikut Muuda olekut.
    * Pange tähele, et valitud konfiguratsiooni praegune versioon on olekus Mustand.  
2. Klõpsake valikut Valmis.
3. Sisestage väljale Kirjeldus soovitud väärtus.
4. Klõpsake nuppu OK.
5. Otsige loendist ja valige soovitud kirje.

## <a name="change-the-base-version-for-the-custom-format-configuration"></a>Kohandatud vormingu konfiguratsiooni alusversiooni muutmine
    * Proseware, Inc. saab teada, et saadaval on BACS-i (UK fiktiivne) konfiguratsiooni uus versioon 1.2, et luua elektroonilisi maksedokumente vastavalt hiljuti teatatud riigipõhistele nõuetele. Proseware, Inc. soovib hakata kasutama seda riigi standardina.  Selleks peab Proseware, Inc. muutma kohandatud konfiguratsiooni BACS-i (UK fiktiivne kohandatud) aluskonfiguratsiooni versiooni. BACS-i (UK fiktiivne) versiooni 1.1 asemel kasutage uut versiooni 1.2.  
1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
2. Valige pakkuja Proseware, Inc, et muuta see aktiivseks.
3. Klõpsake valikut Määra aktiivseks.
4. Klõpsake valikut Aruandluse konfiguratsioonid.
5. Laiendage puustruktuuris suvandit Maksed (lihtsustatud mudel).
6. Laiendage puustruktuuris suvandit 'Payments (simplified model)\BACS (UK fictitious)'.
7. Tehke puustruktuuris valik 'Payments (simplified model)\BACS (UK fictitious)\BACS (UK fictitious custom)'.
    * Valige BACS-i (UK fiktiivne kohandatud) konfiguratsioon, mille omanik on Proseware, Inc.  
    * Kasutage valitud konfiguratsiooni mustandiversiooni, et nõutavad muudatused kasutusele võtta.  
8. Klõpsake nuppu Muuda alust.
    * Valige aluskonfiguratsiooni uus versioon 1.2 konfiguratsiooni värskendamise uueks aluseks.  
9. Klõpsake nuppu OK.
    * Pange tähele, et kohandatud versiooni ja uue alusversiooni liitmisel on avastatud mõned probleemid, mis esindavad mõnd vormingumuudatusi, mida ei saa automaatselt ühendada.  

## <a name="resolve-rebase-conflicts"></a>Aluse muutmise konfliktide lahendamine
1. Klõpsake valikut Kujundaja.
    * Pange tähele, et hankija nime pikkuse piirangu muudatusi ei saa automaatselt lahendada. Seega on see esitatud konfliktide loendis. Iga Värskendus-tüüpi konflikti puhul on saadaval järgmised võimalused: - rakendage eelnevat alusväärtust (ruudustiku ülaosas olev nupp), et tuua sisse eelmise alusversiooni väärtus (meie juhtumi puhul 0);  - rakendage alusväärtust (ruudustiku ülaosas olev nupp), et tuua sisse uue alusversiooni väärtus (meie juhtumi puhul 100);  - Säilitage enda (kohandatud) väärtus (60 meie juhtumis).  Klõpsake suvandit Alusväärtuse rakendamine, et rakendada riigipõhist 100 tähemärgi piirangut hankijate nimepikkuste puhul.  
    * Pange tähele, et ettevõtetel Proseware, Inc. ja Litware Inc. on selle vormingu kohandatud ja kohalikud versioonid, mis kasutavad IBAN- ja SWIFT-koode koos seotud komponentidega, mis liidetakse automaatselt haldusvormingus.  
2. Klõpsake suvandit Alusväärtuse rakendamine.
    * Klõpsake suvandit Alusväärtuse rakendamine, et rakendada riigipõhist 100 tähemärgi piirangut hankijate nimede puhul.  
3. Klõpsake nuppu Salvesta.
    * Vormingu salvestamine eemaldab lahendatud konfliktid konfliktide loendist.  
4. Sulgege leht.

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a>Kohandatud vormingu konfiguratsiooni uue versiooni oleku muutmine
1. Klõpsake valikut Muuda olekut.
    * Muutke värskendatud, kohandatud vormingu konfiguratsiooni olekust Mustand olekule Lõpule viidud. See muudab vormingu konfiguratsiooni maksedokumentide loomiseks kättesaadavaks. Pange tähele, et valitud konfiguratsiooni praegune versioon on olekus Mustand.  
2. Klõpsake valikut Valmis.
3. Sisestage väljale Kirjeldus soovitud väärtus.
4. Klõpsake nuppu OK.
    * Pange tähele, et loodud konfiguratsioon salvestatakse lõpetatud versioonina 1.2.2: alus-BACS-i (UK fiktiivne kohandatud) vormingu versioon 2, mis põhineb alust-BACS-i (UK fiktiivne) vormingu versioonil 2, mis põhineb andmemudeli Maksed (lihtsustatud mudel) versioonil 1.  

## <a name="test-the-customized-format-for-payment-files-generation"></a>Kohandatud vormingu testimine maksefailide loomiseks
    * Viige rakenduse Dynamics 365 for Finance and Operations, Enterprise edition paralleelseansis lõpule protseduur „Loodud vormingu kasutamine maksete jaoks elektrooniliste dokumentide loomiseks”. Valige loodud vorming ‘BACS (UK fiktiivne kohandatud)’ elektroonilise makseviisi parameetrites. Veenduge, et loodud maksefail sisaldab ettevõttes Proseware, Inc. hiljuti kasutusele võetud XML-sõlme IBAN-koodiga vastavalt piirkondlikele nõuetele. Fail peab sisaldama ka hiljuti ettevõtte Litware, Inc. poolt loodud XML-sõlme SWIFT-pangakoodiga vastavalt riigi nõuetele.  


