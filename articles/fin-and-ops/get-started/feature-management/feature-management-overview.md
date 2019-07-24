---
title: Funktsioonihalduse ülevaade
description: See teema kirjeldab funktsioonihaldust ja kuidas seda kasutada.
author: mikefalkner
manager: AnnBe
ms.date: 06/14/2019
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
ms.openlocfilehash: d6aea8651c00b975cf158492e38bb147e908bc56
ms.sourcegitcommit: 672c94704e9a2b0ec7ee3c111d4ceb1bb8597969
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/14/2019
ms.locfileid: "1632049"
---
# <a name="feature-management-overview"></a>Funktsioonihalduse ülevaade

[!include [banner](../../includes/banner.md)]

Igale Microsoft Dynamics 365 for Finance and Operationsi väljalaskele lisatakse funktsioone ja nende uuendusi. Funktsioonihalduse kogemus pakub tööruumi, kus saate vaadata igale väljalaskele lisatud funktsioonide loendit. Vaikimisi on uued funktsioonid välja lülitatud. Saate kasutada tööruumi funktsioonide sisselülitamiseks ja nende dokumentatsiooni vaatamiseks.

## <a name="the-feature-management-workspace"></a>Funktsioonihalduse tööruum

Saate avada **Funktsioonihalduse** tööruumi, valides armatuurlaual vastava paani. Näete lehte, kus kuvatakse funktsioonide loend kõigi väljalasete jaoks, mida funktsioohalduse kogemus toetab. Aja jooksul parandab Microsoft funktsioonihalduse kogemust, et see sisaldaks lisafunktsioone funktsioonide haldamiseks.

Funktsioonide loend sisaldab järgmist teavet.

- **Funktsiooni nimi** – lisatud funktsiooni kirjeldus.
- **Lubatud olek** – sümbol näitab, kas funktsioon on sisse lülitatud (märge), poel sisse lülitatud (tühi), on plaanitud sisse lülitamiseks (kell) või on kohustuslikult sisse lülitatud (lukk). Siin kuvatavat sätet kasutatakse kõigi juriidiliste isikute puhul. Pidage meeles, et isegi kui funktsioon on sisse lülitatud, kontrollib seda ikkagi turve. Seetõttu on funktsioon saadaval ainult neile kasutajatele, kellel on sellele juurdepääs, mis põhineb nende turberollil. See on saadaval ainult juriidilistele isikutele, millele kasutajal on juurdepääs.
- **Luba kuupäeval** – kuupäev, millal funktsioon sisse lülitatud või on sisse lülitamiseks plaanitud.
- **Funktsioon lisatud** – kuupäev, mil funktsioon lisati teie keskkonda. See kuupäev sisestatakse automaatselt, kui värskendate oma keskkonda igakuiste väljaannete tsüklite ajal.
- **Moodul** – moodul, mida uus funktsioon mõjutab.

Kui valite funktsiooni, kuvatakse lisateave üksikasjade paanil funktsioonide loendist paremal. Paani ülaosas näete funktsiooni nime, funktsiooni lisamise kuupäeva, funktsiooni poolt mõjutatud moodulit ja linki **Lisateave**. Valige see link funktsiooni dokumentatsiooni vaatamiseks. Kui dokumentatsioon ei ole saadaval, suunatakse teid ajutisele lehele. Üksikasjade paanil on ka väli **Kommentaarid**, kus saate lisada oma kommentaare funktsiooni kohta.

Tööruumis **Funktsioonihaldus** on ka mitu vahekaarti, mis igaüks kuvavad funktsioonide loendi.

- **Uus** – see vahekaart näitab kõiki funktsioone, mis on lisatud alates viimasest igakuisest uuendusest. Kui olete mõne igakuise uuenduse vahele jätnud, kuvab vahekaart kõik uued funktsioonid, mis on lisatud alates viimasest korrast, kui uuendasite. Uusimad funktsioonid kuvatakse loendi ülaosas. Uute funktsioonide koguarvu näidatakse ka paanil lehe ülaosas.
- **Pole lubatud** – see vahekaart kuvab kõik funktsioonid, mida pole sisse lülitatud. Uusimad funktsioonid kuvatakse loendi ülaosas. Uute sisse lülitamata funktsioonide koguarvu näidatakse ka paanil lehe ülaosas.
- **Plaanitud** – sellel vahekaardil kuvatakse kõik funktsioonid, mis on plaanitud tulevikus sisse lülitada. Kõige varasema plaanitud kuupäevaga funktsioonid kuvatakse loendi ülaosas. Uute graafikus olevate funktsioonide koguarvu näidatakse ka paanil lehe ülaosas.
- **Kõik** – sellel vahekaardil kuvatakse kõik funktsioonid. Uusimad funktsioonid kuvatakse loendi ülaosas.

## <a name="turn-on-a-feature"></a>Funktsiooni sisselülitamine

Kui funktsioon ei ole sisse lülitatud, kuvatakse üksikasjade paanil nupp **Luba kohe**. Selle nupu abil saate funktsiooni sisse lülitada.

- Valige funktsioon, mida soovite sisse lülitada, ja seejärel valige üksikasjade paanil nupp **Luba kohe**. Funktsioon lülitatakse sisse.

Mõnda funktsiooni ei saa pärast sisse lülitamist välja lülitada. Kui funktsiooni, mida proovite sisse lülitada, ei saa välja lülitada, kuvatakse hoiatus. Saate valida nupu **Tühista** toimingu tühistamiseks ja jätta funktsiooni väljalülitatuks. Kui aga valite nupu **Luba** funktsiooni sisselülitamiseks, ei saa te seda hiljem välja lülitada.

Kui funktsioon on sisse lülitatud, kuvatakse teade üksikasjade paani lingi **Lisateave** all. See teade kas ütleb, et funktsioon lülitati sisse, või näitab kuupäeva, millal on funktsioon plaanitud sisse lülitada. See ilmub iga kord, kui valite selle funktsiooni funktsioonide loendist.

Funktsioonid, mis on plaanitud tulevikus sisse lülitada, kuvatakse vahekaardil **Plaanitud**. Pakktöötlus lülitab need määratud kuupäeval keskööl sisse, lähtudes süsteemi kuupäevaga tähistatud ajavööndist.

## <a name="reschedule-a-feature"></a>Funktsiooni uuesti plaanimine

Kui funktsiooni ei ole plaanis tulevikus sisse lülitada, kuvatakse üksikasjade paanil nupp **Plaani**. Selle nupu abil saate muuta suvandi **Luba kuupäeval** väärtuse teiseks kuupäevaks.

1. Valige uuesti plaanimiseks plaanitud funktsioon ja seejärel valige üksikasjade paanil nupp **Plaani**.
2. Kuvatavas dialoogiboksis väljas **Luba kuupäeval** määrake uus kuupäev, millal tuleb funktsioon sisse lülitada.
3. Valige **Luba**, et funktsiooni uuesti plaanida, või **Keela** plaanimise tühistamiseks.

## <a name="turn-off-a-feature"></a>Funktsiooni väljalülitamine

Kui funktsioon on juba sisse lülitatud, kuvatakse üksikasjade paanil nupp **Keela**. Selle nupu abil saate funktsiooni välja lülitada. Nupp **Keela** ei ole saadaval, kui funktsiooni ei saa välja lülitada pärast selle sisse lülitamist.

- Valige välja lülitamiseks funktsioon ja seejärel valige üksikasjade paanil nupp **Keela**. Funktsioon lülitatakse välja ja väli **Luba kuupäeval** tühjendatakse.

Kui funktsioon on välja lülitatud, kuvatakse teade üksikasjade paani lingi **Lisateave** all. See teade ütleb, et funktsioon pole veel sisse lülitatud. See ilmub iga kord, kui valite selle funktsiooni funktsioonide loendist. Funktsioonid, mida pole sisse lülitatud, kuvatakse vahekaardil **Pole lubatud**.

## <a name="features-that-must-be-turned-on"></a>Funktsioonid, mis peavad olema sisse lülitatud

Mõnikord lisatakse kriitiline funktsioon, mis tuleb uuendamisel automaatselt sisse lülitada. Need funktsioonid lülitatakse sisse automaatselt väljas **Luba kuupäeval** määratud kuupäeval. Nende funktsioonide kohta kuvatakse teade üksikasjade paani lingi **Lisateave** all. See teade kas ütleb, et funktsioon lülitati sisse, või näitab kuupäeva, millal funktsioon sisse lülitatakse. See ilmub iga kord, kui valite selle funktsiooni funktsioonide loendist.

## <a name="turn-on-all-features-automatically"></a>Kõikide funktsioonide automaatselt sisselülitamine

Vaikimisi lülitatakse kõik teie keskkonda lisatavad funktsioonid välja, kui need pole kohustuslikud funktsioonid. Kuid kui soovite kõiki uusi funktsioone automaatselt sisse lülitada, saate kasutada ripploendit tööruumi nime all, et muuta, mis juhtub uute funktsioonide lisamisel.

- Valige suvand **Kõik uued funktsioonid lubatakse vaikimisi**, et kõik uued funktsioonid teie keskkonda lisamisel automaatselt sisse lülitada.
- Valige suvand **Kõik uued funktsioonid keelatakse vaikimisi**, et kõik uued funktsioonid teie keskkonda lisamisel automaatselt välja lülitada.

## <a name="assigning-roles"></a>Rollide määramine

Tööruumi **Funktsioonihaldus** saavad avada süsteemiadministraatorid ja ka kasutajad, kes on määratud funktsioonihalduri või funktsiooni vaataja rolli. Need kaks rolli loodi funktsioonihalduse kogemuse toetamiseks. Funktsioonihalduri rollis kasutajad saavad mis tahes funktsioone sisse või välja lülitada. Nad võivad ka värskendada funktsiooni välja **Kommentaarid**. Funktsiooni vaataja rollis kasutajad saavad ainult vaadata tööruumi **Funktsioonihaldus**. Nad ei saa funktsioone sisse või välja lülitada.

Funktsioonihalduri roll ja funktsiooni vaataja roll ei alista kasutaja kehtivat turvet. Nad kontrollivad lihtsalt seda, kas kasutaja saab funktsioone sisse ja välja lülitada. Need ei anna juurdepääsu funktsioonidele enestele.

## <a name="features-that-use-configuration-keys"></a>Konfiguratsioonivõtmeid kasutavad funktsioonid

Kui funktsioon kasutab konfiguratsioonivõtit, aga konfiguratsioonivõti ei ole sisse lülitatud, ei kuva tööruum **Funktsioonihaldus** funktsiooni saadaolevate funktsioonide loendis. Kui olete konfiguratsioonivõtme sisse lülitanud, peate uuendama funktsioonide loendit, kasutades menüü-üksust **Kontrolli uuendusi**. Funktsioon kuvatakse seejärel funktsioonide loendis.

Kui lülitate konfiguratsioonivõtme välja, ei eemaldata funktsiooni funktsioonide loendist.

## <a name="data-entities"></a>Andmeüksused

Andmeüksusega nimega **Funktsioonihaldus** saate eksportida funktsioonihalduse sätteid ühest keskkonnast ja importida need teise keskkonda. See üksus uuendab ainult olemasolevaid funktsioone. Üksuse äriloogika aitab ka tagada seda, et pärast importimist rakendatakse samad reeglid, mida kasutatakse tööruumis **Funktsioonihaldus**. Näiteks ei saa alistada kohustusliku funktsiooni sätet, eemaldades importimise ajal kuupäeva.

Järgmistest näidetes kirjeldatakse, mis juhtub, kui kasutate andmete importimiseks üksust **Funktsioonihaldus**.

- Kui muudate välja **Lubatud** väärtusele **Jah**, lülitatakse funktsioon sisse ja välja **Luba kuupäeval** väärtuseks määratakse praegune kuupäev.
- Kui muudate välja **Lubatud** väärtusele **Ei** või jätate välja **Luba kuupäeval** tühjaks, lülitatakse funktsioon välja ja väli **Luba kuupäeval** tühjendatakse. Välja ei saa lülitada kohustuslikke funktsioone või funktsiooni, mida pole võimalik välja lülitada pärast selle sisse lülitamist.
- Kui muudate välja **Luba kuupäeval** väärtuseks tulevase kuupäeva, plaanitakse funktsioon sellele kuupäevale.
- Kui muudate välja **Lubatud** väärtusele **Jah** ja muudate välja **Luba kuupäeval** väärtuseks tulevase kuupäeva, plaanitakse funktsioon sellele kuupäevale. 
- Kui muudate välja **Lubatud** väärtusele **Ei**, aga muudate ka välja **Luba kuupäeval** väärtuseks tulevase kuupäeva, plaanitakse funktsioon sellele kuupäevale.
- Kui funktsioon lülitatakse sisse ja lisate välja **Luba kuupäeval**, mis on määratud tulevasele kuupäevale, jääb funktsioon sisse lülitatuks. Funktsiooni uuesti plaanimiseks peate muutma välja **Lubatud** väärtusele **Ei**.

## <a name="feature-management-and-flighting"></a>Funktsioonihaldus ja eelväljaanded

Funktsioonihaldusega saate juhtida igas väljaandes saadetud funktsioone. Eelväljaandega saab Microsoft Teams välja anda funktsioone piiratud arvule klientidele, et neid funktsioone saaks katsetada ja kontrollida kõiki kliente mõjutamata. Funktsioonihaldus ei reguleeri ühtegi eelväljaantud funktsiooni.

## <a name="using-feature-management-to-turn-on-isv-features-or-custom-features"></a>Funktsioonihalduse kasutamine ISV-funktsioonide või kohandatud funktsioonide sisselülitamiseks

Funktsioonihaldus pole praegu saadaval sõltumatute tarkvaramüüjate (ISV-d) funktsioonide ja kohandatud funktsioonide jaoks. Kuid Microsoft lisab rohkem funktsioone funktsioonihalduse parandamiseks. Kui need parandused on tehtud, muudab Microsoft funktsioonihalduse saadavaks kõikidele uutele funktsioonidele ja annab juhised funktsioonide uuendamiseks nii, et saaksite seda kasutada.
