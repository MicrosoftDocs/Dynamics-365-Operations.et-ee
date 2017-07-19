---
title: "Pangakonto täpsema vastavusseviimise ülevaade"
description: "Pangakonto täpsema vastavusseviimise abil saate importida elektroonilisi pangaväljavõtteid ja neid Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis automaatselt pangakannetega vastavusse viia.  See artikkel selgitab vastavusseviimise seadistusprotsesse."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 89f895a9de9fa9863459ae6261b8c429d559d482
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017

---

# <a name="advanced-bank-reconciliation-overview"></a>Pangakonto täpsema vastavusseviimise ülevaade

[!include[banner](../includes/banner.md)]


Pangakonto täpsema vastavusseviimise abil saate importida elektroonilisi pangaväljavõtteid ja neid Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis automaatselt pangakannetega vastavusse viia.  See artikkel selgitab vastavusseviimise seadistusprotsesse.  

Enne pangakonto täpsema vastavusseviimise funktsiooni kasutamist tuleb seadistada mitmed parameetrid. Lisateavet pangaväljavõtte importimise seadistamise kohta vt teemast [Pangaväljavõtte impordiprotsessi seadistamine](set-up-advanced-bank-reconciliation-import-process.md).  Vastavusseviimise protsessi seadistamise nõudeid on üksikasjalikult kirjeldatud allpool.

## <a name="transaction-codes"></a>Kandekoodid
Kandekoode saab kasutada osana pangakonto vastavusseviimise vastendusreeglitest.  Kandekoodid aitavad vastendada Finance and Operationsi ja teie pangaväljavõtte vahel sama tüüpi kanded.  Seda tüüpi vastendamiseks peate esmalt määratlema Finance and Operationsist tehtavate pangakannete jaoks kasutatavad kandetüübid ja seejärel vastendama need tüübid teie panga kasutatavate väljavõtte kandekoodidega.  Finance and Operationsi pangakannete kandekoodid määratletakse lehel **Pankakande tüüp**.  See on ka koht, kus saate määratleda kõnealuse kandetüübiga seostatud sisestuste jaoks kasutatava meilikonto. 

Kui teie Finance and Operationsi pangakandekoodid on määratletud, vastendage need oma elektroonilistel pangaväljavõtetel kasutatavate kandekoodidega.  Vastendamine toimub lehel **Kandekoodide vastendamine**.  Kandekoodide vastendamine tuleb teha iga pangakonto puhul eraldi.

## <a name="matching-rules-and-matching-rule-sets"></a>Vastendusreeglid ja vastendusreeglite kogumid
Vastendusreeglid võimaldavad määratleda Finance and Operationsi pangakannete ja pangaväljavõtte kannete vahelisel automaatse vastavusseviimise kriteeriumid.  Vastendusreeglid saate määratleda lehel **Vastavusseviimise vastendusreeglid**.  Lisateavet vt teemast [Panga vastavusseviimise vastendusreeglite seadistamine](set-up-bank-reconciliation-matching-rules.md). 

Vastendusreeglistikuga määratletakse vastendusreeglite grupp, mis käivitatakse järjest pangakonto vastavusseviimise protsessi käigus.  Vastendusreeglistiku saate konfigureerida lehel **Vastavusseviimise vastendusreeglistikud**.

## <a name="cash-and-bank-management-parameters"></a>Sularaha- ja pangahalduse parameetrid
Lehel **Sularaha- ja pangahalduse parameetrid** leiate mitmed pangakonto täpsema vastavusseviimise protsessile kohased parameetrid.  Valik **Kuva väljavõtterea summa deebetis/kreeditis** muudab summade vaadet lehel **Pangaväljavõte**.  Selle valiku korral kuvatakse pangaväljavõtte kandesummad eraldi deebeti- ja kreeditiveergudes.  Kui seda suvandit ei valita, kuvatakse pangaväljavõtte kandesummad üksiku summa veerus koos vastava märgiga. 

Parameetrite lehel määratud kontrollimisvalikud alistavad vastendusreeglites määratud valikud.  Näiteks ei saa te käsitsi ega automaatselt vastendada dokumente, mis jäävad parameetrite lehel määratud kuupäevavahemikust väljapoole.  Samuti, kui on tehtud valik **Kontrolli kandetüübi vastendust**, tuleb kandetüübid Finance and Operationsi pangakannete ja pangaväljavõtte kannete vahel vastendada, et kandeid saaks käsitsi või automaatselt vastendada. 

Peale selle peate konfigureerima lehel **Sularaha- ja pangahalduse parameetrid** vajalikud numbriseeriad.  Määrake vahekaardil **Numbriseeriad** numbriseeriate koodid **Allalaadimise ID, Väljavõtte ID, Vastavusseviimise ID ja Pangakonto vastavusseviimise** viidetele.

## <a name="bank-account-reconciliation-options"></a>Pangakonto vastavusseviimise valikud
Esmalt peate lubama pangakonto täpsema vastavusseviimise pangakonto puhul.  Lehel **Pangakonto** on saadaval mitu lisavalikut, kui funktsioon Pangakonto täpsem vastavusseviimine on lubatud. 

Funktsioon **Kasuta pangaväljavõtteid elektroonilise makse kinnitusena** integreerib pangakonto vastavusseviimise funktsiooni elektrooniliste maksete olekutega.  Kui see on lubatud, luuakse pangadokument automaatselt, kui elektroonilise makse olek on **Saadetud**.  Peale selle värskendatakse elektroonilise makse olek väärtuselt **Saadetud** väärtusele **Vastu võetud**, kui makse on vastendatud, vastavusse viidud ja sisestatud. 

Väli **Pangakonto nimi väljavõtetel** on nimi, mida kasutatakse teie elektroonilistel pangaväljavõtetel pangakonto kohta.  Seda nime kasutatakse määramisel, milliseid kandeid importida pangakonto puhul väljavõttest, milles võivad olla mitme pangakonto andmed. 

Valik **Vii vastavusse pärast importimist** kontrollib automaatselt pangaväljavõtet, loob uue pangakonto vastavusseviimise ja töölehe ning käivitab vaike-vastendamisreeglistiku.  See funktsioon automatiseerib protsessi kuni punktini, kus tehingud tuleb käsitsi vastendada.  Säte pangakontol muutub importimisel vaikesätteks.




