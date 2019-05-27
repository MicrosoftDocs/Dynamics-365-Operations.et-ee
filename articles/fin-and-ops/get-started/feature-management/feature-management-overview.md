---
title: Funktsioonihalduse ülevaade
description: See teema kirjeldab funktsioonihaldust ja kuidas seda kasutada.
author: mikefalkner
manager: AnnBe
ms.date: 04/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: e75e42926db22d4fccda86c755b12d9d121a9c0e
ms.sourcegitcommit: be447fc81bc874982bc0185fcb4d87d99bd742c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538683"
---
# <a name="feature-management-overview"></a>Funktsioonihalduse ülevaade

[!include[banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Igale Microsoft Dynamics 365 for Finance and Operationsi väljalaskele lisatakse funktsioone ja nende uuendusi. Funktsioonihalduse kogemus pakub tööruumi, kus saate vaadata igale väljalaskele lisatud funktsioonide loendit. Vaikimisi on uued funktsioonid välja lülitatud. Saate kasutada tööruumi funktsioonide sisselülitamiseks ja nende dokumentatsiooni vaatamiseks.

## <a name="the-feature-management-workspace"></a>Funktsioonihalduse tööruum

Saate avada **Funktsioonihalduse** tööruumi, valides armatuurlaual vastava paani. Näete lehte, kus kuvatakse funktsioonide loend kõigi väljalasete jaoks, mida funktsioohalduse kogemus toetab. Aja jooksul parandab Microsoft funktsioonihalduse kogemust, et see sisaldaks lisafunktsioone funktsioonide haldamiseks.

Funktsioonide loend sisaldab järgmist teavet.

- **Funktsiooni nimi** – lisatud funktsiooni kirjeldus.
- **Lubatud olek** – sümbol näitab, kas funktsioon on lubatud (märge), pole lubatud (tühi), on plaanitud lubamiseks (kell) või on kohustuslikult lubatud (lukk). Siin kuvatavat sätet kasutatakse kõigi juriidiliste isikute puhul. Pidage meeles, et isegi kui funktsioon on sisse lülitatud, kontrollib seda ikkagi turve. Seetõttu on funktsioon saadaval ainult neile kasutajatele, kellel on sellele juurdepääs, mis põhineb nende turberollil. See on saadaval ainult juriidilistele isikutele, millele kasutajal on juurdepääs.
- **Kuupäeva lubamine** – kuupäev, mil funktsioon lülitati sisse või lülitatakse sisse, kui kuupäev on tulevane kuupäev.
- **Funktsioon lisatud** – kuupäev, mil funktsioon lisati teie keskkonda. See kuupäev sisestatakse automaatselt, kui värskendate oma keskkonda igakuiste väljaannete tsüklite ajal.
- **Moodul** – moodul, mida uus funktsioon mõjutab.

Kui valite funktsiooni, kuvatakse lisateave üksikasjade paanil funktsioonide loendist paremal. Paani ülaosas näete funktsiooni nime, funktsiooni lisamise kuupäeva, funktsiooni poolt mõjutatud moodulit ja linki **Lisateave**. Valige see link funktsiooni dokumentatsiooni vaatamiseks. Kui dokumentatsioon ei ole saadaval, suunatakse teid ajutisele lehele. Üksikasjade paanil on ka väli **Kommentaarid**, kus saate lisada oma kommentaare funktsiooni kohta.

Tööruum **Funktsioonihaldus** sisaldab ka mitut vahekaarti funktsioonide loendiga. 
- **Uus** – näitab kõiki funktsioone, mis on lisatud alates viimasest igakuisest uuendusest. Kui olete mõne igakuise värskenduse vahele jätnud, siis sisaldab see kõiki uusi funktsioone pärast viimast uuendamist. Uusimad funktsioonid kuvatakse loendi ülaosas. Uute funktsioonide koguarvu näidatakse ka paanil lehe ülaosas.
- **Pole lubatud** – kuvatakse kõik funktsioonid, mis pole lubatud. Uusimad funktsioonid kuvatakse loendi ülaosas. Uute funktsioonide koguarvu näidatakse ka paanil lehe ülaosas.
- **Plaanitud** – kuvatakse kõik funktsioonid, mis on plaanitud tulevasel kuupäeval lubada. Kõige varasema plaanitud kuupäevaga funktsioonid kuvatakse loendi ülaosas. Uute funktsioonide koguarvu näidatakse ka paanil lehe ülaosas.
- **Kõik** – kuvatakse kõik funktsioonid. Uusimad funktsioonid kuvatakse loendi ülaosas.


## <a name="enable-a-feature"></a>Funktsiooni lubamine

Kui funktsioon ei ole lubatud, kuvatakse üksikasjade paanil nupp **Luba**. Selle nupu abil saate funktsiooni lubada.

1. Valige funktsioon, mida soovite lubada, ja seejärel valige üksikasjade paanil **Luba**.
2. Kuvatakse liugur, kus saate määrata kuupäeva, millal funktsioon peab olema lubatud. Vaikimisi on selleks kuupäevaks määratud praegune kuupäev.
3. Funktsiooni lubamiseks valige **Luba**.

Pärast funktsioonide lubamist ei saa mõnda neist enam keelata. Kui funktsiooni, mida proovite lubada, ei saa keelata, kuvatakse hoiatus. Saate valida **Tühista** toimingu tühistamiseks ning jätta funktsiooni keelatuks. Kui aga valite **Luba** ja lubate selle funktsiooni, ei saa te seda hiljem keelata.

Kui funktsioon on lubatud, kuvatakse teade üksikasjade paani lingi **Lisateave** all. See teade kas ütleb, et funktsioon lubati või osutab, et funktsioon lubatakse tulevikus. Kui kasutate tulevast kuupäeva, kuvatakse funktsioon loendis **Plaanitud**. See teade ilmub iga kord, kui valite selle funktsiooni funktsiooni loendist. Tulevikus plaanitud funktsioonid lubatakse keskööl pakktöötluse käigus, mis põhineb ajavööndil, mida esindab süsteemi kuupäev. 

## <a name="reschedule-a-feature"></a>Funktsiooni uuesti plaanimine

Kui funktsioon ei ole tulevikus lubatud, kuvatakse üksikasjade paanil nupp **Uuesti plaanimine**. Selle nupu abil saate muuta **Luba kuupäev** teiseks kuupäevaks.

1. Valige plaanitud funktsioon, mida soovite uuesti plaanida, ja seejärel valige üksikasjade paanil **Uuesti plaanimine**.
2. Kuvatakse liugur, kus saate määrata kuupäeva, millal funktsioon peab olema lubatud. 
3. Valige **Luba**, et funktsiooni uuesti plaanida, või **Keela** plaanimise tühistamiseks.

## <a name="disable-a-feature"></a>Funktsiooni keelamine

Kui funktsioon on juba lubatud, kuvatakse üksikasjade paanil nupp **Keela**. Selle nupu abil saate funktsiooni keelata. Nupp **Keela** ei ole saadaval, kui funktsiooni ei saa keelata pärast selle lubamist.

- Valige funktsioon, mida soovite välja lülitada, ja seejärel valige üksikasjade paanil **Keela**.

- Funktsioon on keelatud ja kuupäev tühjendatakse.

Kui funktsioon on keelatud, kuvatakse teade üksikasjade paani lingi **Lisateave** all. See teade täpsustab, et funktsioon ei ole veel lubatud ja kuvatakse loendis **Pole lubatud**. Teade ilmub iga kord, kui valite selle funktsiooni funktsioonide loendist.

## <a name="features-that-must-be-enabled"></a>Funktsioonid, mis peavad olema lubatud

Võidakse lisada kriitiline funktsioon, mis tuleb uuendamisel automaatselt lubada. See lubatakse automaatselt **Luba kuupäeval**. Teade kuvatakse üksikasjade paanil lingi **Lisateave** all. Selles teates märgitakse, et funktsioon lubati või lubatakse automaatselt **Luba kuupäeval**. See ilmub iga kord, kui valite selle funktsiooni funktsioonide loendist.

## <a name="assigning-roles"></a>Rollide määramine

Tööruumi **Funktsioonihaldus** saavad avada süsteemiadministraatorid ja kasutajad, kes on määratud funktsioonihalduri või funktsiooni vaataja rolli, mis loodi funktsioonihalduse kogemuse toetamiseks. Funktsioonihalduri rollis kasutajad saavad mis tahes funktsioone sisse või välja lülitada. Nad võivad ka värskendada funktsiooni kommentaaride jaotist. Funktsiooni vaataja rollis kasutajad saavad ainult vaadata tööruumi **Funktsioonihaldus**. Nad ei saa funktsioone sisse või välja lülitada.

Funktsioonihalduri roll ja funktsiooni vaataja roll ei alista kasutaja kehtivat turvet. Rollid kontrollivad ainult juurdepääsu funktsioonide lubamisele. See ei võimalda juurdepääsu funktsioonidele enestele.

## <a name="using-feature-management-to-enable-isv-features-or-custom-features"></a>Funktsioonihalduse kasutamine ISV-funktsioonide või kohandatud funktsioonide lubamiseks

Funktsioonihalduse protsess ei ole praegu saadaval ISV-funktsioonide või kohandatud funktsioonide jaoks. Lisame funktsioonihalduse parandamiseks lisafunktsioone ja, kui need täiustused on lõpule viidud, avame funktsioonihalduse kõigile funktsioonidele ja anname täpsed juhised, kuidas värskendada oma funktsiooni selle kasutamiseks.

## <a name="feature-management-and-flighting"></a>Funktsioonihaldus ja eelväljaanded

Funktsioonihaldus võimaldab teil juhtida igas väljaandes saadetud funktsioone. Eelväljaanne võimaldab Microsoft Teamsil valja anda funktsioone piiratud arvule klientidele, et funktsioone saaks katsetada ja kontrollida kõiki kliente mõjutamata. Funktsioonihaldus ei reguleeri ühtegi eelväljaantud funktsiooni.
