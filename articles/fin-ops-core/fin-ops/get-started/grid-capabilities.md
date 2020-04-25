---
title: Ruudustiku võimalused
description: Selles teemas kirjeldatakse ruudustiku juhtelemendi mitmeid võimsaid funktsioone. Nende võimaluste kasutamiseks tuleb uus ruudustikufunktsioon lubada.
author: jasongre
manager: AnnBe
ms.date: 04/10/2020
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
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 0fd0e15ea88e9f5f34d8dff82606a8d26616a16d
ms.sourcegitcommit: cd8a28be0acf31c547db1b8f6703dd4b0f62940c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2020
ms.locfileid: "3260456"
---
# <a name="grid-capabilities"></a>Ruudustiku võimalused

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Uus ruudustiku juhtelement pakub mitmeid kasulikke ja võimsaid võimalusi, mida saab kasutada kasutaja tootlikkuse suurendamiseks, teie andmetest huvitavate vaadete loomiseks ja sisukate ülevaadete hankimiseks andmete jaoks. Selles artiklis tutvustatakse järgmisi võimalusi. 

-  Summade arvutamine
-  Andmete rühmitamine
-  Süsteemist eespool tippimine
-  Matemaatiliste avaldiste hindamine 

## <a name="calculating-totals"></a>Summade arvutamine
Rakendustes Finance and Operations on kasutajatel võimalik ruudustiku numbriveergude allosas näha kogusummasid. Need kogusummad kuvatakse ruudustiku allosas jaluse jaotises. 

### <a name="showing-the-grid-footer"></a>Ruudustiku jaluse kuvamine
Finance and Operationsi rakendustes on igas tabeliruudustikus allosas jaluse ala. Jalus näitab olulist teavet, mis on seotud ruudustikus kuvatavate andmetega. Siin on mõned näited sellest teabest.

- Valitud ridade arv tabelis (kui on valitud rohkem kui üks kirje)
- Konfigureeritud arvveergude allosas olevad kogusummad
- Andmekogumi ridade arv 

See jalus on vaikimisi peidetud, kuid seda saab hõlpsasti sisse lülitada. Ruudustiku jaluse kuvamiseks paremklõpsake ruudustiku veeru päist ja valige suvand **Kuva jalus**. Kui jalus on teatud ruudustiku puhul sisse lülitatud, jäetakse see säte meelde, kuni kasutaja otsustab jaluse peita. Seda saab teha, paremklõpsates veeru päises ja valides käsu **Peida jalus**.  Pange tähele, et toimingu **Kuva jalus / peida jalus** paigutust plaanitakse edasistes värskendustes muuta. 

### <a name="specifying-columns-with-totals"></a>Veergude määramine kogusummade abil
Praegu ei konfigureerita kogusummade vaikimisi kuvamiseks ühtegi veergu. Selle asemel loetakse seda ühekordse häälestuse toiminguks, mis on sarnane veergude laiuste kohandamisega ruudustikes. Kui olete määranud, et soovite näha veeru kogusummasid, kuvatakse teile seda sätet järgmisel lehekülastusel.  

Veeru konfigureerimiseks kogusumma kuvamiseks on kaks võimalust. 

- Paremklõpsake veergu, mille kogusummat soovite näha, ja valige seejärel suvand **Selle veeru kogusumma**. See tegevus põhjustab kolme sündmuse toimumist.

    1. Jalus muutub nähtavaks. 
    2. Teie eelistus selle veeru kogusumma nägemiseks salvestatakse. 
    3. Käivitatakse kogusummade arvutus selle veeru ja mis tahes teiste veergude jaoks, mille kogusummad konfigureerisite. Kogusumma kuvamiseks vajalik aeg sõltub andmekogumi suurusest, mille summeerite.

- Kui jalus on nähtav, valige veeru, mille kogusummat soovite näha, allosas jaluse alas suvandit **Kuva kogusumma**. Kui konfigureeritud veerge pole, on kõigi arvveergude jaoks saadaval nupp **Kuva kogusumma**. 

    Pärast seda, kui vähemalt üks veerg on kogusummade jaoks konfigureeritud, on nupud **Kuva kogusumma** saadaval ainult hõljumisel või fookustamisel. Suvandi **Kuva kogusumma** valimise tegevus ainult salvestab teie eelistused selle veeru kogusumma nägemiseks, nii et eelistus rakendatakse lehe tulevaste külastuste ajal. Jaluses näitab seda olekut veerus ilmuv kriips. (Teie võimalusena kui andmekomplekt on piisavalt väike, kuvatakse kogusumma kohe.)

Kui teete vea ega soovi enam kogusummat kindlas veerus näha, paremklõpsake veergu ja valige käsk **Peida kogusumma** või selle veeru jaluses nupp **Peida kogusumma**. See eelistus salvestatakse ka tulevastele lehekülastuste jaoks. 

### <a name="calculating-totals"></a>Summade arvutamine
Kui avate lehe, mille jalus on nähtav ja veerud on kogusummade jaoks juba konfigureeritud, võivad kogusummad olla jaluses kuvatud, kuid see ei pruugi nii olla. Käitumine oleneb leheküljel oleva andmekogumi suurusest. Kui andmekogum on piisavalt väike, kuvatakse kogusummad automaatselt koos andmekogumi ridade arvuga. Kui kogusummade jaoks konfigureeritud veergude all jaluses on kriipsud, siis on andmekogum süsteemi jaoks liiga suur, et kogusummasid kohe kuvada. Seetõttu on kogusummade arvutamiseks vaja selget toimingut. Selleks klõpsake jaluses nuppu **Arvuta** või paremklõpsake veerul, mida soovite kokku arvutada, ja valige käsk **Selle veeru kogusumma**.  

Kui arvutamine võtab liiga kaua aega, saate toimingu tühistada, klõpsates nuppu **Tühista**. Mõnikord on andmekogum kogusummade arvutamiseks siiski liiga suur (selle piiri kehtestab teie organisatsioon) ja teil palutakse andmeid rohkem filtreerida.

Kogusummasid värskendatakse automaatselt, kui uuendate, kustutate või loote andmekogumi ridu.  

## <a name="grouping-data"></a>Andmete rühmitamine
Ärikasutajatel on sageli vaja teha andmete ad-hoc-analüüsi. Üks võimalus selle tegemiseks on eksportida andmeid Microsoft Excelisse ja kasutada liigendtabeleid, kuid ruutvõrgustiku võimalus **Rühmitamine** võimaldab kasutajatel oma andmeid põnevatel viisidel rakendustes Finance and Operations korraldada. Kuna see funktsioon laiendab funktsiooni **Kogusummad**, võimaldab **Rühmitamine** teil saada ka sisukaid ülevaateid oma andmetest, pakkudes vahesummasid grupi tasandil.

Selle funktsiooni kasutamiseks paremklõpsake veergu, mille alusel soovite rühmitada, ja valige käsk **Rühmita selle veeru järgi**. See tegevus sordib andmed valitud veeru alusel, lisab uue grupi veeru järgi ruudustiku algusse ja lisab iga grupi algusesse päise read. Need päise read annavad iga grupi kohta järgmist teavet. 
-  Grupi andmete väärtus 
-  Veeru silt (see teave on eriti kasulik pärast seda, kui toetatud on rühmitamise mitu taset.)
-  Selles grupis olevate andmeridade arv
-  Kogusummade kuvamiseks konfigureeritud veergude vahesummad

Kui [Salvestatud vaated](saved-views.md) on lubatud, saab selle rühmitamise isikupärastamisena järgmiseks lehekülastuseks salvestada, et saada kiirjuurdepääs.  

Kui valite käsu **Rühmita selle veeru alusel** mõnes teises veerus, asendatakse algne rühmitamine, kuna versioonis 10.0.9 platvormivärskendusega 33 on toetatud ainult üks rühmitamise tase.

Rühmitamise tagasivõtmiseks ruudustikus paremklõpsake rühmitataval veerul ja valige käsk **Tühista rühmitamine**.  


## <a name="evaluating-math-expressions"></a>Matemaatiliste avaldiste hindamine
Tootlikkuse tõstmiseks saavad kasutajad sisestada ruudustiku numbrilahtritesse matemaatilisi valemeid. Nad ei pea tegema arvutust süsteemivälises rakenduses. Näiteks kui sisestate **=15\*4** ja vajutate siis väljalt välja liikumiseks **tabeldusklahvi**, hindab süsteem avaldist ja salvestab välja jaoks väärtuse **60**.

Selleks et süsteem tuvastaks avaldise väärtuse, käivitage väärtus võrdusmärgiga (**=**). Lisateavet toetatud tehtemärkide ja süntaksi kohta vt teemast [Toetatud matemaatilised sümbolid](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Kuidas lubada uut ruudustiku juhtelementi oma keskkonnas? 

**10.0.9 / platvormivärskendus 33 ja hilisem** Funktsioon **Uus ruudustiku juhtelement** on kõikides keskkondades saadaval otse funktsioonihalduses. Sarnaselt teistele avaliku eelvaate funktsioonidele kehtib selle funktsiooni tootmisse lubamisele [täiendav kasutustingimuste leping](https://go.microsoft.com/fwlink/?linkid=2105274).  

**10.0.8 / platvormiuuendus 32 ja 10.0.7 / platvormiuuendus 31** Funktsiooni **Uus ruudustiku juhtelement** saab lubada 1. taseme (arendamine/testimine) ja 2. taseme (liivakast) keskkondades, et pakkuda täiendavat testimist ja kujundusmuudatusi, järgides alltoodud juhiseid.

1.  **Luba lend**: Käivitage järgmine SQL-lause: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLIReactGridEnableFeature', 1, 0, 5637144576);`

2. **Lähtesta IIS**, et tühjendada staatilise eelväljaande vahemälu. 

3.  **Leia funktsioon**: avage tööruum **Funktsiooni haldus**. Kui funktsiooni **Uus ruudustiku juhtelement** ei kuvata kõigi funktsioonide loendis, tehke valik **Otsi värskendusi**.   

4.  **Luba funktsioon**: leidke funktsioon **Uus ruudustiku juhtelement** funktsioonide loendist ja valige üksikasjade paanilt suvand **Luba nüüd**. Pidage meeles, et brauseri värskendamine on nõutav. 

Kõik järgmised kasutajaseansid algavad lubatud uue ruudustiku juhtelemendiga.
