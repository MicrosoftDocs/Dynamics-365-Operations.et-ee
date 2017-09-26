---
title: Tasakaalustuse konfigureerimine
description: "Kuidas ja millal kanded tasakaalustatakse, võib olla keeruline teema, nii et on oluline, et mõistate ja määratlete õigesti oma ärinõuetele vastavad parameetrid. Selles artiklis kirjeldatakse parameetreid, mida kasutatakse nii ostu- kui ka müügireskontro tasakaalustamiseks."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 059513de66827aa3a839b9eb06973ec4c1549f73
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017

---

# <a name="configure-settlement"></a>Tasakaalustuse konfigureerimine

[!include[banner](../includes/banner.md)]


Kuidas ja millal kanded tasakaalustatakse, võib olla keeruline teema, nii et on oluline, et mõistate ja määratlete õigesti oma ärinõuetele vastavad parameetrid. Selles artiklis kirjeldatakse parameetreid, mida kasutatakse nii ostu- kui ka müügireskontro tasakaalustamiseks. 

Järgmised parameetrid mõjutavad, kuidas tasakaalustusi Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis töödeldakse. Tasakaalustus on arve makse või kreeditarvega tasakaalustamise protsess. Need parameetrid asuvad ala **Tasakaalustus** lehtedel **Müügireskontro parameetrid** ja **Ostureskontro parameetrid**.

-   **Automaatne tasakaalustus** – määrake see suvand valikule **Jah**, kui kanne tuleks tasakaalustada teiste avatud kannetega automaatselt kande sisestamisel. Kui see suvand on seatud valikule **Ei**, saavad kasutajad kandeid käsitsi tasakaalustada maksete sisestamisel või hiljem, kasutades lehte **Kannete tasakaalustamine**.
-   **Skonto haldamine** – määrake, kuidas [skontot arve ülemaksmisel käsitletakse](cash-discount-handling-overpayments.md). Ülemakse puhul saab skontot vähendada, käsitleda erinevusena või jätta selle hankija või kliendi kontole.
    -   **Määramata** – skonto summat vähendatakse ülemakse summa võrra. Seda kasutatakse alati, olenemata sellest, kas ülemakse summa on suurem või väiksem kui summa, mis on sisestatud väljale **Suurim üle- või alamakse**.
    -   **Kindel** – ülemakse summa sisestatakse kas skonto erinevuse pearaamatukontole või jäetakse saldona kliendi või hankija kontole. Kindel käitumine oleneb sellest, kas ülemakse summa on 0,00 ja väljale **Suurim üle- või alamakse** sisestatud summa vahel või kas ülemakse summa on suurem kui summa väljal **Suurim üle- või alamakse**.
-   **Suurim sendierinevus** – sisestage tasakaalustatud kannete suurim lubatud sendierinevus. Kui sendierinevus on võrdne sellel väljal määratud sendierinevusega või sellest väiksem, sisestatakse erinevus lehel **Automaatsete kannete kontod** määratud sendierinevuse pearaamatukontole.
-   **Suurim üle- või alamakse** – sisestage üle- ja alamakse puhul aktsepteeritav summa. Üle- või alamaksetelt maksu arvutamiseks klõpsake lehel **Pearaamatu parameetrid** suvandit **Käibemaks** ja seejärel valige suvand **Üle- või alamaksete käibemaks**.
    -   Kui üle- või alamakse tulemuseks on sendierinevus, mis on väljal **Suurim sendierinevus** määratletud erinevusest väiksem, sisestatakse sendierinevuse summa sendierinevuse kontole.
    -   Kui üle- või alamakse tulemuseks on sendierinevus, mis on väljal **Suurim sendierinevus** määratletud erinevusest suurem, sisestatakse sendierinevuse summa erinevuse kontole, mis on sisestustüübi **Kliendi skonto** või **Hankija skonto** puhul valitud lehel **Automaatsete kannete kontod**.
-   **Arvuta skontod osamaksete jaoks** – määrake see suvand valikule **Jah**, et lubada osamaksete skontode automaatne arvutamine.
    -   Selle suvandi mõju oleneb välja **Kasuta skontot** väärtusest lehel **Kannete tasakaalustamine**. Kui see suvand on seatud valikule **Jah**, võetakse allahindlus, kui välja **Kasuta skontot** väärtuseks on seatud **Tavaline**. Kui välja **Kasuta skontot** väärtuseks on seatud **Alati**, võetakse skonto alati, olenemata selle välja seadistusest. Kui välja **Kasuta skontot** väärtuseks on seatud **Mitte kunagi**, ei võeta skontot mitte kunagi, olenemata selle välja seadistusest.
    -   Kui see suvand on seatud valikule **Jah** ja kasutaja muudab välja **Tasakaalustatav summa** väärtust lehel **Kannete tasakaalustamine** , arvutatakse allahindlus automaatselt ja kuvatakse vaikekirjena väljal **Skonto summa võtmiseks**.
    -   Kui see suvand on seatud valikule **Ei** ja kasutaja muudab välja **Tasakaalustatav summa** väärtust lehel **Kannete tasakaalustamine**, on vaikekirjeks väljal **Skonto summa võtmiseks** **0** (null).
-   **Arvuta skontod kreeditarvete jaoks** – määrake see suvand valikule **Jah** kreeditarvete skonto automaatseks arvutamiseks. Müügireskontros on kreeditarve kanne negatiivne kanne, millel on väärtus väljal **Arve** lehel **Vabas vormis arve** või tagastus lehel **Müügitellimus**.
    -   Selle suvandi mõju oleneb välja **Kasuta skontot** väärtusest lehel **Kannete tasakaalustamine**. Kui see suvand on seatud valikule **Jah**, võetakse allahindlus, kui välja ****Kasuta skontot**** väärtuseks on seatud **Tavaline**. Kui välja ****Kasuta skontot**** väärtuseks on seatud **Alati**, võetakse skonto alati, olenemata selle välja seadistusest. Kui välja ****Kasuta skontot**** väärtuseks on seatud **Mitte kunagi**, ei võeta skontot mitte kunagi, olenemata selle välja seadistusest.
    -   Kui see suvand on määratud valikule **Jah** ja kreeditarve on märgitud lehel **Kannete tasakaalustamine**, arvutatakse allahindlus automaatselt ja kuvatakse vaikekirjena väljal **Skonto summa võtmiseks**.
    -   Kui see suvand on määratud valikule **Ei** ja kreeditarve on märgitud lehele **Kannete tasakaalustamine**, on vaikekirjeks väljal **Skonto summa võtmiseks** **0** (null).
-   **Allahindluse vastaskontod (ainult ostureskontro)** – määratlege vaikimisi skonto pearaamatukonto, mida tuleks kasutada skontode raamatupidamiskirje puhul.
    -   **Kasuta hankija allahindluste jaoks põhikontot** – skonto sisestatakse põhikontole, mis on määratletud lehel **Skonto seadistus**.
    -   **Kontod arve real** – skonto sisestatakse algse arve pearaamatukontodele.
-   **Märgi read vabas vormis arvetel ja viivisearvetel (ainult osturestkontro)** – määrake see suvand valikule **Jah** nupu **Märgi arve read** lubamiseks lehtedel **Kliendimaksete sisestamine**, **Makse töölehekanne** ja **Kannete tasakaalustamine**. See nupp võimaldab kasutajatel märkida tasakaalustuse üksikuid ridu.
-   **Tasakaalustuse prioritiseerimine (ainult ostureskontro)** – määrake see suvand valikule **Jah** nupu **Märgi prioriteedi alusel** lubamiseks lehtedel **Kliendimaksete sisestamine** ja **Kannete tasakaalustamine**. See nupp võimaldab kasutajatel määrata eelnevalt määratud tasakaalustuse tellimuse kannetele.  Pärast tasakaalustuse tellimuse rakendamist kandele saab tellimust ja makse eraldamist enne sisestamist muuta.
-   **Kasuta automaatseteks tasakaalustusteks prioriteeti** – määrake see suvand valikule **Jah** määratletud tähtsusjärjestuse kasutamiseks kannete automaatsel tasakaalustamisel. See väli on saadaval ainult juhul, kui suvandid **Tasakaalustuse prioritiseerimine** ja **Automaatne tasakaalustus** on seatud valikule **Jah**.





