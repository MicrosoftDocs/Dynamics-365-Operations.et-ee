---
title: Ruudustiku võimalused
description: Selles teemas kirjeldatakse ruudustiku juhtelemendi mitmeid võimsaid funktsioone. Nende võimaluste kasutamiseks tuleb uus ruudustikufunktsioon lubada.
author: jasongre
manager: AnnBe
ms.date: 01/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: b49d7823f48bcc9cdbb56b87d5fa72d46ddfa15c
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019731"
---
# <a name="grid-capabilites"></a>Ruudustiku võimalused

[!include [banner](../includes/banner.md)]

Uus ruudustiku juhtelement pakub mitmeid kasulikke ja võimsaid võimalusi, mida saab kasutada kasutaja tootlikkuse suurendamiseks, teie andmetest huvitavate vaadete loomiseks ja sisukate ülevaadete hankimiseks andmete jaoks. Selles artiklis tutvustatakse järgmisi võimalusi. 

-  Summade arvutamine
-  Andmete rühmitamine
-  Süsteemist eespool tippimine
-  Matemaatiliste avaldiste hindamine 

## <a name="calculating-totals"></a>Summade arvutamine
Rakendustes Finance and Operations on kasutajatel võimalik ruudustiku numbriveergude allosas näha kogusummasid. Need kogusummad kuvatakse ruudustiku allosas jaluse jaotises. 

### <a name="showing-the-grid-footer"></a>Ruudustiku jaluse kuvamine
Rakenduse Finance and Operations igas tabeliruudustikus on ruudustiku allosas jaluse ala, mis näitab kuvatud andmetega seotud väärtuslikku teavet. See teave sisaldab järgmist. 
-  Valitud ridade arv tabelis (kui on valitud rohkem kui üks kirje)
-  Konfigureeritud numbriveergude allosas olevad kogusummad
-  Andmekogumi ridade arv 

See jalus on vaikimisi peidetud, kuid seda saab hõlpsasti sisse lülitada. Ruudustiku jaluse kuvamiseks paremklõpsake ruudustiku veeru päist ja valige suvand **Kuva jalus**. Kui jalus on teatud ruudustiku puhul sisse lülitatud, jäetakse see säte meelde, kuni kasutaja otsustab jaluse peita. Seda saab teha, paremklõpsates veeru päises ja valides käsu **Peida jalus**.  Pange tähele, et toimingu **Kuva jalus / peida jalus** paigutust plaanitakse edasistes värskendustes muuta. 

### <a name="specifying-columns-with-totals"></a>Veergude määramine kogusummade abil
Praegu ei konfigureerita kogusummade vaikimisi kuvamiseks ühtegi veergu. Selle asemel loetakse seda ühekordse häälestuse toiminguks, mis on sarnane veergude laiuste kohandamisega ruudustikes. Kui olete määranud, et soovite näha veeru kogusummasid, kuvatakse teile seda sätet järgmisel lehekülastusel.  

Veeru konfigureerimiseks kogusumma kuvamiseks on kaks võimalust. 
1.  Paremklõpsake veergu, mille kogusummat soovite näha ja valige **Selle veeru kogusumma**. Selle toiminguga tehakse kolm asja. Esiteks teeb see jaluse nähtavaks. Teiseks salvestab see teie eelistuse selle veeru kogusumma nägemiseks. Kolmandaks käivitab see tegevus selle ja kõigi teiste varem konfigureeritud veergude kogusummade kalkulatsiooni kogusummade nägemiseks. Kogusumma kuvamiseks kuluv aeg on otseselt seotud teie summeeritava andmekogumi suurusega.  

2.  Kui jalus on näidatud, saate teise võimalusena teid huvitava veeru allosas jalusealas klõpsata nuppu **Kuva kogusumma**. Kui konfigureeritud veerge pole, kuvatakse kõigi arvuveergude jaoks nupp **Kuva kogusumma**. Kui kogusummade jaoks on konfigureeritud vähemalt üks veerg, on nupud **Kuva kokku** saadaval ainult hõljumisel või fookuses hoidmisel. See tegevus lihtsalt salvestab teie eelistuse, et soovite tulevastel külastustel näha selle veeru kogusummat, ja seda olekut näitab kriips, mis kuvatakse jaluses veerus (või kui andmekogum on piisavalt väike, siis kuvatakse kohe kogusumma).

Kui teete vea ega soovi enam kogusummat kindlas veerus näha, paremklõpsake veergu ja valige käsk **Peida kogusumma** või selle veeru jaluses nupp **Peida kogusumma**. See eelistus salvestatakse ka tulevastele lehekülastuste jaoks. 

### <a name="calculating-totals"></a>Summade arvutamine
Kui avate lehe, mille jalus on nähtav ja veerud on kogusummade jaoks juba konfigureeritud, võivad kogusummad olla jaluses kuvatud, kuid see ei pruugi nii olla. Käitumine oleneb leheküljel oleva andmekogumi suurusest. Kui andmekogum on piisavalt väike, kuvatakse kogusummad automaatselt koos andmekogumi ridade arvuga. Kui kogusummade jaoks konfigureeritud veergude all jaluses on kriipsud, siis on andmekogum süsteemi jaoks liiga suur, et kogusummasid kohe kuvada. Seetõttu on kogusummade arvutamiseks vaja selget toimingut. Selleks klõpsake jaluses nuppu **Arvuta** või paremklõpsake veerul, mida soovite kokku arvutada, ja valige käsk **Selle veeru kogusumma**.  

Kui arvutamine võtab liiga kaua aega, saate toimingu tühistada, klõpsates nuppu **Tühista**. Mõnikord on andmekogum kogusummade arvutamiseks siiski liiga suur (selle piiri kehtestab teie organisatsioon) ja teil palutakse andmeid rohkem filtreerida.

Kogusummasid värskendatakse automaatselt, kui uuendate, kustutate või loote andmekogumi ridu.  

## <a name="grouping-data"></a>Andmete rühmitamine
Ärikasutajatel on sageli vaja teha andmete ad-hoc-analüüsi. Üks võimalus selle tegemiseks on eksportida andmeid Microsoft Excelisse ja kasutada liigendtabeleid, kuid ruutvõrgustiku võimalus **Rühmitamine** võimaldab kasutajatel oma andmeid põnevatel viisidel rakendustes Finance and Operations korraldada. Kuna see funktsioon laiendab funktsiooni **Kogusummad**, võimaldab **Rühmitamine** teil saada ka sisukaid ülevaateid oma andmetest, pakkudes vahesummasid grupi tasandil.

Selle funktsiooni kasutamiseks paremklõpsake veergu, mille alusel soovite rühmitada, ja valige käsk **Rühmita selle veeru järgi**. See tegevus sordib andmed valitud veeru alusel, lisab uue grupi veeru järgi ruudustiku algusse ja lisab iga grupi algusesse päise read. Need päise read annavad iga grupi kohta järgmist teavet. 
-  Grupi andmete väärtus 
-  Veeru silt. See on eriti kasulik, kui toetatud on rühmitamise mitu taset.  
-  Selles grupis olevate andmeridade arv
-  Kogusummade kuvamiseks konfigureeritud veergude vahesummad

Kui [Salvestatud vaated](saved-views.md) on lubatud, saab selle rühmitamise isikupärastamisena järgmiseks lehekülastuseks salvestada, et saada kiirjuurdepääs.  

Kui valite käsu **Rühmita selle veeru alusel** mõnes teises veerus, asendatakse algne rühmitamine, kuna 10.0.9/platvormi värskenduses 33 on toetatud ainult rühmitamise tase.

Rühmitamise tagasivõtmiseks ruudustikus paremklõpsake rühmitataval veerul ja valige käsk **Tühista rühmitamine**.  


## <a name="evaluating-math-expressions"></a>Matemaatiliste avaldiste hindamine
Selle asemel et teha arvutus süsteemivälises rakenduses, saab kasutaja tootlikkuse tõstmiseks matemaatilise valemi ruudustiku numbrilahtritesse sisestada. Näiteks saate sisestada **=15\*4** ja väljalt lahkuda. Süsteem hindab avaldist ja salvestab väljale väärtuse 60.

Selleks et süsteem tuvastaks avaldise väärtuse, käivitage väärtus võrdusmärgiga (**=**). Lisateavet toetatud tehtemärkide ja süntaksi kohta vt teemast [Toetatud matemaatilised sümbolid](http://redhivesoftware.github.io/math-expression-evaluator/#supported-maths-symbols).  
