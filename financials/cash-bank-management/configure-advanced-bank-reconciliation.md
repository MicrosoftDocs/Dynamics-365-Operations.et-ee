---
title: "Pangakonto täpsema vastavusseviimise ülevaade"
description: "Täiustatud pangakonto sobitamise saate importida elektroonilise pangakonto väljavõtted ja automaatselt viia vastavusse Microsofti Dynamics 365 toiminguteks.  See artikkel selgitab vastavusseviimise seadistusprotsesse."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: c2fc9e858f61d7d0122393bbf306ba64ac3659b8
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Pangakonto täpsema vastavusseviimise ülevaade

Täiustatud pangakonto sobitamise saate importida elektroonilise pangakonto väljavõtted ja automaatselt viia vastavusse Microsofti Dynamics 365 toiminguteks.  See artikkel selgitab vastavusseviimise seadistusprotsesse.  

On tuleb seadistada enne funktsiooni Täpsem panga vastavusseviimise tükkide arvuga. Panga väljavõtte impordi häälestamise kohta lisateabe saamiseks vt [seadistada panga väljavõtte import protsess](set-up-advanced-bank-reconciliation-import-process.md).  Nõuetele moodustatud lõpetamine, on toodud allpool.

## <a name="transaction-codes"></a>Kandekoodid
Kosmosesse lennutamise saate kasutada pangakonto sobitamise Kokkulangevuse alased eeskirjad.  Kosmosesse lennutamise aitab ainult sama tüüpi tehingute Dynamics 365 operatsioonide ja pangakonto väljavõtte.  Selleks, et seda tüüpi sobitamine, peate esmalt määratleda pangatehingute Dynamics 365 toiminguteks kasutada tüübid, siis nende puhul vastendada kasutada teie panga poolt tehingu koodiga.  Kandetüübid Dynamics 365 toimingute pangatehingute määratletud ning **panga kandetüübi** lehel.  See on ka määratleda põhikontole, et kasutada selle tehingu tüübiga seotud postitusi. 

Kui oma Dynamics 365 toimingute Pank tehingu koodid on määratletud, siis vastendada need elektroonilise pangakonto väljavõtted kasutatavaid kandekoode.  Kaardistamise protsess on tehtud kasutades on **tehingu vastendamine** lehel.  Iga pangakonto puhul täidetakse eraldi tehingu vastendamine.

## <a name="matching-rules-and-matching-rule-sets"></a>Vastendusreeglid ja vastendusreeglite kogumid
Leevendamiste abil saate määratleda kriteeriumid operatsioonide pangatehingute Dynamics 365 ja pangaväljavõtte tehingute automaatne viimine.  Seati leevendamiste tehakse **Kokkulangevuse alased eeskirjad vastavusse viimine** lehel.  Lisateabe saamiseks vaadake [loodud pangakonto sobitamise Kokkulangevuse alased eeskirjad](set-up-bank-reconciliation-matching-rules.md). 

Vastavaid reegel sätestab kasutatakse vastavaid eeskirju, mis käivitatakse järjest Panga vastavusseviimine protsessi ajal rühma.  Vastavaid reegel sätestab on konfigureeritud selle **sobitamine reeglistiku leppimise** lehel.

## <a name="cash-and-bank-management-parameters"></a>Sularaha- ja pangahalduse parameetrid
Mitmeid parameetreid on iseloomulikud arenenud Panga vastavusseviimine protsessi kohta on **raha ja pangakontod parameetrid** lehel.  Selle **Näita väljavõtte rea summa deebet/kreedit** muudetakse summade kohta ning **panga väljavõtte** lehel.  Kui see suvand on valitud, näidatakse eraldi deebet ja krediidi veergudena panga väljavõtte kannete kogusummat.  Kui pole valitud, kuvatakse panga väljavõtte kannete summade summa veergude puhul sobiv märk. 

Lehel parameetrid seada valideerimise suvandid alistada eeskirjad vastavusse seatud Valikud.  Näiteks ei saa käsitsi või automaatselt vastavad dokumendid ületada seatud parameetrite lehe kuupäeva.  Ka, kui võimalus **kontrollida tehingu tüüp kaardistamine** on valitud, peab tehinguliikide jaotatud operatsioonide pangakande Dynamics 365 ja pangaväljavõtte tehingu selleks kandeid käsitsi või automaatselt sobitada. 

Samuti peate konfigureerima vajalikud Numbriseeriad selle **raha ja pangakontod parameetrid** lehel.  Kohta ning **Numbriseeriad** vahekaardil, määratud numbriseeria koodid laadida **ID, aruande-ID, sobitamine ID ja panga vastavusseviimise** viited.

## <a name="bank-account-reconciliation-options"></a>Pangakonto vastavusseviimise valikud
Peate esmalt lubama täiustatud pangakonto sobitamise jaoks.  Täiendavad suvandid on saadaval ka **pangakontole** lehekülg kui arenenud panga vastavusseviimise funktsioon on lubatud. 

**Kasutamise pangaväljavõtted kui elektrooniliste maksete ülehelistamine** funktsionaalsust ühendab panga vastavusseviimise funktsioonid elektrooniliste maksete staatused.  Kui see on lubatud, pangadokument luuakse automaatselt elektroonilise makse olek on seatud **saadetud**.  Lisaks elektrooniline staatus ajakohastada **saadetud** et **saadud** pärast makse sobib vastavusse viidud ja sisestatud. 

Selle **pangakonto nimi avaldused** väli on nimi, mida kasutatakse pangakonto kohta elektroonilise pangakonto väljavõtted.  Seda nime kasutatakse, milliseid kandeid importida pangakonto väljavõttelt, mis võivad sisaldada teavet mitut pangakontot määramisel. 

Võimalus **pärast importimist sobitamine** näidatakse automaatselt kinnitada pangaväljavõtte, luua uus pangakonto sobitamise ja töölehe ja käivitage vaikimisi vastavuses olevad reeglistiku.  See funktsioon automatiseerib protsessi kuni kandeid, mis tuleb käsitsi kokku sobitada.  Pangakonto seade Vaikimisi importimisel.


