---
title: Tasakaalustuse konfigureerimine
description: Kuidas ja millal kanded tasakaalustatakse, võib olla keeruline teema, nii et on oluline, et mõistate ja määratlete õigesti oma ärinõuetele vastavad parameetrid. Selles teemas kirjeldatakse parameetreid, mida kasutatakse nii ostu- kui ka müügireskontro tasakaalustamiseks.
author: kweekley
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14601
ms.assetid: 6b61e08c-aa8b-40c0-b904-9bca4e8096e7
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 094b8876b3b10b6dcbc0ce399a1a9915271459ed
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188368"
---
# <a name="configure-settlement"></a>Tasakaalustuse konfigureerimine

[!include [banner](../includes/banner.md)]

Kuidas ja millal kanded tasakaalustatakse, võib olla keeruline teema, nii et on oluline, et mõistate ja määratlete õigesti oma ärinõuetele vastavad parameetrid. Selles teemas kirjeldatakse parameetreid, mida kasutatakse nii ostu- kui ka müügireskontro tasakaalustamiseks. 

Järgmised parameetrid mõjutavad, kuidas tasakaalustusi Microsoft Dynamics 365 Finance'is töödeldakse. Tasakaalustus on arve makse või kreeditarvega tasakaalustamise protsess. Need parameetrid asuvad ala **Tasakaalustus** lehtedel **Müügireskontro parameetrid** ja **Ostureskontro parameetrid**.

- **Automaatne tasakaalustus** – määrake see suvand valikule **Jah**, kui kanne tuleks tasakaalustada teiste avatud kannetega automaatselt kande sisestamisel. Kui see suvand on seatud valikule **Ei**, saavad kasutajad kandeid käsitsi tasakaalustada maksete sisestamisel või hiljem, kasutades lehte **Kannete tasakaalustamine**.
- **Skonto haldamine** – määrake, kuidas [skontot arve ülemaksmisel käsitletakse](cash-discount-handling-overpayments.md). Ülemakse puhul saab skontot vähendada, käsitleda erinevusena või jätta selle hankija või kliendi kontole.
  -   **Määramata** – skonto summat vähendatakse ülemakse summa võrra. Seda kasutatakse alati, olenemata sellest, kas ülemakse summa on suurem või väiksem kui summa, mis on sisestatud väljale **Suurim üle- või alamakse**.
  -   **Kindel** – ülemakse summa sisestatakse kas skonto erinevuse pearaamatukontole või jäetakse saldona kliendi või hankija kontole. Kindel käitumine oleneb sellest, kas ülemakse summa on 0,00 ja väljale **Suurim üle- või alamakse** sisestatud summa vahel või kas ülemakse summa on suurem kui summa väljal **Suurim üle- või alamakse**.
- **Suurim sendierinevus** – sisestage tasakaalustatud kannete suurim lubatud sendierinevus. Kui sendierinevus on võrdne sellel väljal määratud sendierinevusega või sellest väiksem, sisestatakse erinevus lehel **Automaatsete kannete kontod** määratud sendierinevuse pearaamatukontole.
- **Suurim üle- või alamakse** – sisestage üle- ja alamakse puhul aktsepteeritav summa. Üle- või alamaksetelt maksu arvutamiseks klõpsake lehel **Pearaamatu parameetrid** suvandit **Käibemaks** ja seejärel valige suvand **Üle- või alamaksete käibemaks**.
  -   Kui üle- või alamakse tulemuseks on sendierinevus, mis on väljal **Suurim sendierinevus** määratletud erinevusest väiksem, sisestatakse sendierinevuse summa sendierinevuse kontole.
  -   Kui üle- või alamakse tulemuseks on sendierinevus, mis on väljal **Suurim sendierinevus** määratletud erinevusest suurem, sisestatakse sendierinevuse summa erinevuse kontole, mis on sisestustüübi **Kliendi skonto** või **Hankija skonto** puhul valitud lehel **Automaatsete kannete kontod**.
- **Arvuta skontod osamaksete jaoks** – määrake see suvand valikule **Jah**, et lubada osamaksete skontode automaatne arvutamine.
  -   Selle suvandi mõju oleneb välja **Kasuta skontot** väärtusest lehel **Kannete tasakaalustamine**. Kui see suvand on seatud valikule **Jah**, võetakse allahindlus, kui välja **Kasuta skontot** väärtuseks on seatud **Tavaline**. Kui välja **Kasuta skontot** väärtuseks on seatud **Alati**, võetakse skonto alati, olenemata selle välja seadistusest. Kui välja **Kasuta skontot** väärtuseks on seatud **Mitte kunagi**, ei võeta skontot mitte kunagi, olenemata selle välja seadistusest.
  -   Kui see suvand on seatud valikule **Jah** ja kasutaja muudab välja **Tasakaalustatav summa** väärtust lehel **Kannete tasakaalustamine** , arvutatakse allahindlus automaatselt ja kuvatakse vaikekirjena väljal **Skonto summa võtmiseks**.
  -   Kui see suvand on seatud valikule **Ei** ja kasutaja muudab välja **Tasakaalustatav summa** väärtust lehel **Kannete tasakaalustamine**, on vaikekirjeks väljal **Skonto summa võtmiseks** **0** (null).
- **Arvuta skontod kreeditarvete jaoks** – määrake see suvand valikule **Jah** kreeditarvete skonto automaatseks arvutamiseks. Müügireskontros on kreeditarve kanne negatiivne kanne, millel on väärtus väljal **Arve** lehel **Vabas vormis arve** või tagastus lehel **Müügitellimus**.
  - Selle suvandi mõju oleneb välja <strong>Kasuta skontot</strong> väärtusest lehel <strong>Kannete tasakaalustamine</strong>. Kui see suvand on seatud valikule <strong>Jah</strong>, võetakse allahindlus, kui välja *<strong><em>Kasuta skontot</em></strong>* väärtuseks on seatud <strong>Tavaline</strong>. Kui välja *<strong><em>Kasuta skontot</em></strong>* väärtuseks on seatud <strong>Alati</strong>, võetakse skonto alati, olenemata selle välja seadistusest. Kui välja *<strong><em>Kasuta skontot</em></strong>* väärtuseks on seatud <strong>Mitte kunagi</strong>, ei võeta skontot mitte kunagi, olenemata selle välja seadistusest.
  - Kui see suvand on määratud valikule **Jah** ja kreeditarve on märgitud lehel **Kannete tasakaalustamine**, arvutatakse allahindlus automaatselt ja kuvatakse vaikekirjena väljal **Skonto summa võtmiseks**.
  - Kui see suvand on määratud valikule **Ei** ja kreeditarve on märgitud lehele **Kannete tasakaalustamine**, on vaikekirjeks väljal **Skonto summa võtmiseks** **0** (null).

- **Allahindluse vastaskontod (ainult ostureskontro)** – määratlege vaikimisi skonto pearaamatukonto, mida tuleks kasutada skontode raamatupidamiskirje puhul.
  -   **Kasuta hankija allahindluste jaoks põhikontot** – skonto sisestatakse põhikontole, mis on määratletud lehel **Skonto seadistus**.
  -   **Kontod arve real** – skonto sisestatakse algse arve pearaamatukontodele.
- **Märgi read vabas vormis arvetel ja viivisearvetel (ainult osturestkontro)** – määrake see suvand valikule **Jah** nupu **Märgi arve read** lubamiseks lehtedel **Kliendimaksete sisestamine**, **Makse töölehekanne** ja **Kannete tasakaalustamine**. See nupp võimaldab kasutajatel märkida tasakaalustuse üksikuid ridu.
- **Tasakaalustuse prioritiseerimine (ainult ostureskontro)** – määrake see suvand valikule **Jah** nupu **Märgi prioriteedi alusel** lubamiseks lehtedel **Kliendimaksete sisestamine** ja **Kannete tasakaalustamine**. See nupp võimaldab kasutajatel määrata eelnevalt määratud tasakaalustuse tellimuse kannetele.  Pärast tasakaalustuse tellimuse rakendamist kandele saab tellimust ja makse eraldamist enne sisestamist muuta.
- **Kasuta automaatseteks tasakaalustusteks prioriteeti** – määrake see suvand valikule **Jah** määratletud tähtsusjärjestuse kasutamiseks kannete automaatsel tasakaalustamisel. See väli on saadaval ainult juhul, kui suvandid **Tasakaalustuse prioritiseerimine** ja **Automaatne tasakaalustus** on seatud valikule **Jah**.

## <a name="fixed-dimensions-on-accounts-receivableaccounts-payable-main-accounts"></a>Müügireskontro/ostureskontro põhikontode fikseeritud dimensioonid

Kui müügireskontro/ostureskontro põhikontol kasutatakse fikseeritud dimensioone, sisestab tasakaalustusprotsess täiendavad konto kirjed ja kaks täiendavat hankijakannet. Tasakaalustus võrdleb arvel ja maksel olevat müügireskontro/ostureskontro pearaamatukontot.  Kui makse ja tasakaalustus lõpetatakse samal ajal, nagu tavapäraselt juhtub, siis ei sisestata makse raamatupidamiskirjet pearaamatusse enne, kui tasakaalustamisprotsess on samuti lõpetanud. Töötlemissündmuste järjekorra tõttu ei saa tasakaalustus tuvastada müügireskontro/ostureskontro pearaamatukontot makse raamatupidamiskirjest. Tasakaalustus rekonstrueerib, mis pearaamatukonto makse jaoks olema peaks. See on probleem, kui müügireskontro/ostureskontro põhikonto jaoks kasutatakse fikseeritud dimensiooni.

Pearaamatukonto rekonstrueerimiseks võetakse müügireskontro/ostureskontro põhikonto sisestusprofiililt ja finantsdimensioonid võetakse makse hankija kande kirjest, nagu määratletud makse töölehel. Fikseeritud dimensioonid ei sisestata vaikimisi makse töölehtedele, vaid kantakse põhikontole sisestamisprotsessi viimases etapis. Seetõttu ei ole fikseeritud dimensiooni väärtust tõenäoliselt hankija kandel, kui see pole just vaikimisi sisestatud teisest allikast, näiteks hankijalt. Rekonstrueeritud konto ei sisalda fikseeritud dimensiooni. Tasakaalustustöötlus tuvastab, et vaja on luua korrigeeriv sisestus, kuna seda ei teinud fikseeritud dimensiooni väärtusega ja rekonstrueeritud makse kontoga sisestatud arve.  Tasakaalustus jätkab korrigeeriva sisestuse sisestamisega ning viimaseks etapiks on fikseeritud dimensiooni rakendamine. Fikseeritud dimensioon lisatakse korrigeerivale sisestusele ning sisestatakse sama pearaamatukonto deebeti ja kreeditiga. Tasakaalustus ei saa eelmist raamatupidamiskirjet taastada.

Selleks, et vältida täiendavate raamatupidamiskirjete ning deebeti ja kreediti samale pearaamatukontole lisamist, kaaluge oma ettevõtte vajaduste kohaselt järgmisi lahendusi. 

-   Organisatsioonid kasutavad sageli fikseeritud dimensioone, et täita mittevajalikke finantsdimensioone nullidega. Nii on tavapäraselt bilansikontode puhul, näiteks müügireskontrod/ostureskontrod. Konto struktuure saab kasutada tavaliselt nullidega täidetud finantsdimensioonide jälgimise välistamiseks.  Saate finantsdimensiooni bilansikontode jaoks eemaldada, kõrvaldades sellega vajaduse fikseeritud dimensioonide kasutamise järele.
-   Kui teie organisatsioon nõuab müügireskontro/ostureskontro põhikonto jaoks fikseeritud dimensioone, siis proovige leida viis, kuidas fikseeritud dimensioon vaikimisi maksele sisestada, nii et fikseeritud dimensiooni väärtus on salvestatud makse hankija kandel. See võimaldab süsteemil rekonstrueerida müügireskontro/ostureskontro põhikonto nii, et fikseeritud dimensiooni väärtused oleks hõlmatud. Fikseeritud dimensiooni väärtust saab määratleda vaikeväärtuseks hankijate jaoks või makse töölehe nimel.
