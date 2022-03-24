---
title: Kaalutud keskmise kuupäev koos kaasa füüsilise väärtuse ja märkimisega
description: Kaalutud keskmine kuupäev on kaalutud keskmise põhimõttel põhinev laomudel, milles laos olevaid kaupu hinnatakse lattu sissetulevate kaupade keskmise väärtuse järgi iga lao sulgemisperioodi päeva lõikes.
author: AndersGirke
ms.date: 03/04/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28991
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3cf2206863d891eceb9c65ff879da3f9f72032b1
ms.sourcegitcommit: fcded93fc6c27768a24a3d3dc5cc35e1b4eff22b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/07/2022
ms.locfileid: "8391997"
---
# <a name="weighted-average-date-with-include-physical-value-and-marking"></a>Kaalutud keskmise kuupäev koos kaasa füüsilise väärtuse ja märkimisega

[!include [banner](../includes/banner.md)]

*Kaalutud keskmine kuupäev* on laomudel, mis põhineb keskmisel, mis arvutatakse iga komponendi (kauba kande) korrutamisel teguriga (omahind), mis kajastab selle tähtsust (kogust) perioodi igal päeval. See tähendab, et see laomudel määrab väljaminekkannete kulu, põhinedes iga päev saadud kõigi varude keskmisel väärtusel, pluss mis tahes vabal kaubavarul alates eelmisest päevast.

Kui käitate lao sulgemist, kasutades kaalutud keskmise kuupäeva laomudelit, saab tasakaalustuse loomiseks kasutada kahte meetodit. Tavaliselt tasakaalustatakse kõik sissetulekud virtuaalse väljaminek, mis hoiab kogu vastuvõetud kogust ja väärtust. Sel virtuaalsel väljaminel on vastav virtuaalne sissetulek, millelt väljaminek tasakaalustatakse. Sel viisil on kõigil väljaminek igal päeval sama keskmine kulu. Virtuaalset väljaminek ja virtuaalne sissetulek on virtuaalne ülekanne. Seda virtuaalset ülekannet nimetatakse kaalutud *keskmise lao sulgemise ülekandeks*. Seetõttu tuntakse seda tasakaalustusmeetodit kaalutud keskmise *summeeritud tasakaalustusena*. Ainult ühe kviitungi puhul saab kõik väljaminek selle kaudu tasakaalustada ning virtuaalset ülekannet ei looda. Seda tasakaalustusmeetodit nimetatakse otseseks *tasakaalustamiseks*. Kõiki laoseisus ladusid, mis on vabad pärast lao sulgemist, arvutatakse kaalutud keskmise järgi alates eelmise perioodi viimasest päevast ja kaasatakse järgmise perioodi kaalutud keskmise kuupäeva arvutamisse.

Kaalutud keskmise kuupäeva põhimõtte saate alistada laokannete märkimisega nii, et konkreetse kauba sissetulek tasakaalustatakse konkreetse väljaminek. Kui kasutate kaalutud keskmise kuupäeva laomudelit tasakaalustuste loomiseks ja kaupade väärtuse korrigeerimiseks vastavalt kaalutud keskmise kuupäeva põhimõttele, on vajalik perioodiline lao sulgemine. Lao sulgemiseni väärtussaatakse väljaminek jooksva keskmiseni, kui toimusid füüsilised ja finantsilist uuendused. Kui te ei kasuta märkimist, arvutatakse füüsilise või finantsilise uuendamise ajal jooksev keskmine.

Kaalutud keskmise kuupäeva laokulu arvutamise meetod arvutatakse järgmise valemi abil iga päev:

*Kulu* = \[(*Qb*<sub>*·*</sub> × *Pb*<sub>*·*</sub>) + &#x2211;<sub>*n*</sub>(*Qn*<sub>*·*</sub> × *Pn*<sub>*·*</sub>)\] ÷ (*Qb*<sub>*·*</sub> + &#x2211;<sub>*nQn)*</sub>*·*<sub>*·*</sub>

- *Q* = Kande kogus
- *P* = kande hind

Teiste sõnadega võrdub kaalutud keskmine kulu algkoguse ja alghinna ning iga sissetulekukoguse ja sissetulekuhinna summa ning algkoguse ja sissetulekukoguste summa vahel.

Lao sulgemise ajal tehakse kalkulatsioon iga päev sulgemisperioodi jooksul.

> [!NOTE]
> Lisateavet tasakaalustuste kohta vt Lao [sulgemine](inventory-close.md).

Järgmised näited näitavad kaalutud keskmise kuupäeva mõju viie konfiguratsiooniga:

- kaalutud keskmise kuupäeva otsene tasakaalustus valikut **Kaasa füüsiline väärtus** kasutamata;
- kaalutud keskmise kuupäeva summeeritud tasakaalustus valikut **Kaasa füüsiline väärtus** kasutamata;
- kaalutud keskmise kuupäeva otsene tasakaalustus valikut **Kaasa füüsiline väärtus** kasutades;
- kaalutud keskmise kuupäeva summeeritud tasakaalustus valikut **Kaasa füüsiline väärtus** kasutades;
- kaalutud keskmine kuupäev märkimist kasutades.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Kaalutud keskmise kuupäeva otsene tasakaalustus valikut Kaasa füüsiline väärtus kasutamata

Otsese tasakaalustamise põhimõte loob tasakaalustuse sissetulekute ja väljaminekte vahel vahetult, loomata täiendavaid laokandeid. Süsteem kasutab seda otsest tasakaalustamise põhimõtet järgmistes olukordades:

- Perioodi on sisestatud üks sissetulek ja üks või mitu väljamist.
- Perioodi on sisestatud ainult väljaminekud ja varud sisaldavad vabu kaupu eelmisest sulgemisest.

Selles näites tühjendatakse **väljastatud** toote kauba **mudeligrupi** lehel märkeruut Kaasa füüsiline väärtus. Järgnev diagramm näitab järgmisi kandeid:

**1. päev.**

- 1a. Lao füüsiline sissetulek kogusele 10 hinnaga 10,00 USD tükk.
- 1b. Lao finantsiline sissetulek kogusele 10 hinnaga 10,00 USD tükk.
- 2a. Lao füüsiline sissetulek kogusele 10 hinnaga 20,00 USD tükk.
- 3a. Lao füüsiline väljastus, kogus 1, omahind USD 10.00 (finantsiliselt sisestatud kannete jooksev keskmine).
- 3b. Lao finantsiliselt väljaminev kogus 1 omahinnaga USD 10.00 (finantsiliselt sisestatud kannete jooksev keskmine).

**2. päev.**

- 4a. Lao füüsiline sissetulek kogusele 1 hinnaga 25,00 USD tükk.
- 5a. Lao füüsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 5b. Lao finantsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 6a. Lao finantsiliselt väljaminev kogus 1 hinnaga USD 20.00 (finantsiliselt sisestatud kannete jooksev keskmine).

**3. päev**

- 7\. Teostatakse lao sulgemine. Kaalutud keskmise kuupäeva meetodi alusel kasutab süsteem otsese tasakaalustuse meetodit 30. detsembril (12/30), sest 12.30-st värskendatakse finantsiliselt ainult üks sissetulek. Selles näites luuakse kannete 1b ja 3b vahel üks tasakaalustus. Korrigeeritakse USD 10.00 3b väärtus kuni 20,00. 31. detsembril (12/31) ei korrigeerita ega tasakaalustata, kuna 12.31. detsembril ei ole finantsiliselt värskendatud väljaminekuid.

Järgnev diagramm näitab seda **kannete seeriat ja kaalutud keskmise laomudeli kasutamise efektisid ja otsese tasakaalustuse põhimõtet valikuta Kaasa füüsiline** väärtus.

![Kaalutud keskmise kuupäeva otsene tasakaalustus ilma füüsilise väärtuse valikut kaasamata.](media/weighted-average-date-direct-settlement-without-include-physical-value.png)

**Diagrammi võti:**

- Laokandeid tähistavad vertikaalsed nooled.
- Füüsilisi kandeid esindavad lühemad helehallid nooled.
- Finantskandeid esindavad pikemad mustad nooled.
- Sissetulekuid laovarudesse esindavad vertikaalsed nooled telje kohal.
- Väljaminek laovarudest on esindatud vertikaalnooltega telje all.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Kuupäevad on eraldatud musta vertikaaljoontega. Kuupäevad on märgitud diagrammi allosas.
- Lao sulgemisi tähistab punased vertikaalsed kriipsjoonelised read.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Kaalutud keskmise kuupäeva summeeritud tasakaalustus valikut Kaasa füüsiline väärtus kasutamata

Kui perioodis on mitu sissetulekut, kasutab kaalutud keskmine kuupäev summeeritud tasakaalustuse põhimõtet, kus kõik ühe päeva sissetulekud *summeeritakse kandesse, mille nimi on kaalutud keskmine lao sulgemine*. Kõik päeva sissetulekud tasakaalustatakse vastloodud laokande väljaminek. Kõik päeva väljaminek tasakaalustatakse uue laokande sissetulekuga. Kui pärast lao sulgemist on vaba kaubavaru jääkväärtus, kaasatakse vaba kaubavaru väärtus kaalutud keskmise lao sulgemiskannete sissetulekukandesse.

Järgnev diagramm näitab järgmisi kandeid:

**1. päev.**

- 1a. Lao füüsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
- 1b. Lao finantsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
- 2a. Lao füüsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
- 2b. Lao finantsiline sissetulek kogusele 1 hinnaga 22,00 USD tükk.
- 3a. Lao füüsiline väljastus, kogus 1, omahind USD 16.00 (finantsiliselt sisestatud kannete jooksev keskmine).
- 3b. Lao finantsiliselt väljaminev kogus 1 omahinnaga USD 16.00 (finantsiliselt sisestatud kannete jooksev keskmine).

**2. päev.**

- 4a. Lao füüsiline sissetulek kogusele 1 hinnaga 25,00 USD tükk.
- 5a. Lao füüsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 5b. Lao finantsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 6a. Lao füüsiline väljastus, kogus 1 omahinnaga USD 23.00 (finantsiliselt sisestatud kannete jooksev keskmine).

**3. päev**

- 7\. Teostatakse lao sulgemine.
- 7a. Kaalutud keskmise lao sulgemise kande finantsiline väljaminek luuakse kõigi lao finantsivate sissetulekute tasakaalustuste summeerimiseks.

    - Kanne 1b tasakaalustatakse kogusele 1 tasakaalustatud summaga USD 10.00.
    - Kanne 2b tasakaalustatakse kogusele 1 tasakaalustatud summaga USD 22.00.
    - Kanne 7a luuakse kogusele 2 tasakaalustatud summaga USD 32.00. See kanne tasakaalustab kahe selle perioodi jooksul finantsiliselt uuendatud sissetulekukande summa.

- 7b. Kaalutud keskmise lao sulgemise kande finantssissetulek luuakse finantsiliselt sisestatud väljaminekul tasakaalustamiseks.

    - Kanne 3b tasakaalustatakse kogusele 1 tasakaalustatud USD 16.00. Seda kannet ei korrigeerita, kuna see on finantsiliselt sisestatud kannete kaalutud keskmine 1. detsembril (12.12.).
    - Kanne 7b luuakse kogusele 2 rahalise summaga USD 32.00 ja tasakaalustatud summaga USD 16.00 vastaskandele 3b. See kanne tasakaalustab ühe väljaminekukande summa, mis on perioodi jooksul finantsiliselt uuendatud. Kanne jääb avatuks, sest vaba kaubavaru on veel üks.

Järgmine diagramm näitab seda kannete seeriat ja kaalutud keskmise laomudeli kasutamise efektisid ja summeeritud tasakaalustuse põhimõtet, **kuid ilma valikut Kaasa füüsiline** väärtus kasutades.

![Kaalutud keskmise kuupäeva summeeritud tasakaalustus ilma füüsilise väärtuse kaasamise valikuta.](media/weighted-average-date-summarized-settlement-without-include-physical-value.png)

**Diagrammi võti:**

- Laokandeid tähistavad vertikaalsed nooled.
- Füüsilisi kandeid esindavad lühemad helehallid nooled.
- Finantskandeid esindavad pikemad mustad nooled.
- Sissetulekuid laovarudesse esindavad vertikaalsed nooled telje kohal.
- Väljaminek laovarudest on esindatud vertikaalnooltega telje all.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Kuupäevad on eraldatud musta vertikaaljoontega. Kuupäevad on märgitud diagrammi allosas.
- Lao sulgemisi tähistab punased vertikaalsed kriipsjoonelised read.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Kaalutud keskmise kuupäeva otsene tasakaalustus valikut Kaasa füüsiline väärtus kasutades

Toote praeguses versioonis töötab suvand **Kaasa** füüsiline väärtus kaalutud keskmise kuupäeva laomudeliga varasemast versioonist erinevalt. Kui valite **kauba mudeligrupi** **lehel** märkeruudu Kaasa füüsiline väärtus, kasutab süsteem eeldatava omahinna või jooksva keskmise arvutamisel füüsiliselt värskendatud sissetulekuid. Väljaminekud sisestatakse sellel perioodi jooksul eeldataval omahinnal põhinedes. Lao sulgemise jooksul arvestatakse kaalutud keskmise arvutamisel ainult finantsiliselt värskendatud sissetulekuid.

Järgnev diagramm näitab järgmisi kandeid:

**1. päev.**

- 1a. Lao füüsiline sissetulek kogusele 10 hinnaga 10,00 USD tükk.
- 1b. Lao finantsiline sissetulek kogusele 10 hinnaga 10,00 USD tükk.
- 2a. Lao füüsiline sissetulek kogusele 10 hinnaga 20,00 USD tükk.
- 3a. Lao füüsiline väljastus, kogus 1 omahinnaga USD 15.00 (füüsiliselt ja finantsiliselt sisestatud kannete jooksev keskmine).
- 3b. Lao finantsiline väljaminev kogus 1 omahinnaga USD 15.00 (füüsiliselt ja finantsiliselt sisestatud kannete jooksev keskmine).

**2. päev.**

- 4a. Lao füüsiline sissetulek kogusele 1 hinnaga 25,00 USD tükk.
- 5a. Lao füüsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 5b. Lao finantsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 6a. Lao füüsiline väljastus kogusele 1 hinnaga USD 21.25 (füüsiliselt ja finantsiliselt sisestatud kannete jooksev keskmine).

**3. päev**

- 7\. Teostatakse lao sulgemine. Kaalutud keskmise kuupäeva meetodi alusel kasutab süsteem otsese tasakaalustuse meetodit 30. detsembril (12/30), sest 12.30-st värskendatakse finantsiliselt ainult üks sissetulek. Selles näites luuakse kannete 1b ja 3b vahel üks tasakaalustus. Väljaminek pole 30.12.12 tehtud. 31. detsembril (12/31) ei korrigeerita ega tasakaalustata, kuna 12.31. ei ole finantsiliselt värskendatud väljaminekuid.

Järgnev diagramm näitab seda kannete seeriat ja kaalutud keskmise laomudeli kasutamise efektisid ja otsese tasakaalustuse põhimõtet valikuga **Kaasa füüsiline** väärtus.

![Kaalutud keskmise otsene tasakaalustus koos kaasa füüsilise väärtusega.](media/weighted-average-date-direct-settlement-with-include-physical-value.png)

**Diagrammi võti:**

- Laokandeid tähistavad vertikaalsed nooled.
- Füüsilisi kandeid esindavad lühemad helehallid nooled.
- Finantskandeid esindavad pikemad mustad nooled.
- Sissetulekuid laovarudesse esindavad vertikaalsed nooled telje kohal.
- Väljaminek laovarudest on esindatud vertikaalnooltega telje all.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Kuupäevad on eraldatud musta vertikaaljoontega. Kuupäevad on märgitud diagrammi allosas.
- Lao sulgemisi tähistab punased vertikaalsed kriipsjoonelised read.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Kaalutud keskmise kuupäeva summeeritud tasakaalustus valikut Kaasa füüsiline väärtus kasutades

Toote praeguses versioonis töötab suvand Kaasa **füüsiline väärtus** kaalutud keskmisega teistmoodi, kui see töötas varasemates versioonides. Kui valite **kauba mudeligrupi** **lehel** märkeruudu Kaasa füüsiline väärtus, kasutab süsteem eeldatava omahinna või jooksva keskmise arvutamisel füüsiliselt värskendatud sissetulekuid. Väljaminekud sisestatakse sellel perioodi jooksul eeldataval omahinnal põhinedes. Lao sulgemise jooksul arvestatakse kaalutud keskmise arvutamisel ainult finantsiliselt värskendatud sissetulekuid. Kui kasutate kaalutud keskmise lao mudelit, soovitame teha igakuist lao sulgemist. Selles näites kaalutud keskmise kuupäeva summeeritud tasakaalustuse puhul on laomudel märgitud füüsilist väärtust kaasama.

Järgnev diagramm näitab järgmisi kandeid:

**1. päev.**

- 1a. Lao füüsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
- 1b. Lao finantsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
- 2a. Lao füüsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
- 2b. Lao finantsiline sissetulek kogusele 1 hinnaga 22,00 USD tükk.
- 3a. Lao füüsiline väljastus, kogus 1 omahinnaga USD 16.00 (füüsiliselt ja finantsiliselt sisestatud kannete jooksev keskmine).
- 3b. Lao finantsiline väljaminev kogus 1 omahinnaga USD 16.00 (füüsiliselt ja finantsiliselt sisestatud kannete jooksev keskmine).

**2. päev.**

- 4a. Lao füüsiline sissetulek kogusele 1 hinnaga 25,00 USD tükk.
- 5a. Lao füüsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 5b. Lao finantsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 6a. Lao füüsiline väljastus, kogus 1 omahinnaga USD 23.67 (füüsiliselt ja finantsiliselt sisestatud kannete jooksev keskmine).

**3. päev**

- 7\. Teostatakse lao sulgemine.
- 7a. Kaalutud keskmise lao sulgemise kande finantsiline väljaminek luuakse kõigi lao finantsivate sissetulekute tasakaalustuste summeerimiseks.

    - Kanne 1b tasakaalustatakse kogusele 1 tasakaalustatud summaga USD 10.00.
    - Kanne 2b tasakaalustatakse kogusele 1 tasakaalustatud summaga USD 22.00.
    - Kanne 7a luuakse kogusele 2 tasakaalustatud summaga USD 32.00. See kanne tasakaalustab kahe selle perioodi jooksul finantsiliselt uuendatud sissetulekukande summa.

- 7b. Kaalutud keskmise lao sulgemise kande finantssissetulek luuakse finantsiliselt sisestatud väljaminekul tasakaalustamiseks.

    - Kanne 3b tasakaalustatakse kogusele 1 tasakaalustatud USD 16.00. Seda kannet ei korrigeerita, kuna see on finantsiliselt sisestatud kannete kaalutud keskmine 1. detsembril (12.12.).
    - Kanne 7b luuakse kogusele 2 rahalise summaga USD 32.00 ja tasakaalustatud summaga USD 16.00 vastaskandele 3b. See kanne tasakaalustab ühe väljaminekukande summa, mis on perioodi jooksul finantsiliselt uuendatud. Kanne jääb avatuks, sest vaba kaubavaru on veel üks.

Järgmine diagramm näitab seda kannete seeriat ja kaalutud keskmise laomudeli kasutamise efektisid **ja summeeritud tasakaalustuspõhimõtet valikuta Kaasa füüsiline** väärtus.

![Kaalutud keskmise summeeritud tasakaalustus koos kaasa füüsilise väärtusega.](media/weighted-average-date-summarized-settlement-with-include-physical-value.png)

**Diagrammi võti:**

- Laokandeid tähistavad vertikaalsed nooled.
- Füüsilisi kandeid esindavad lühemad helehallid nooled.
- Finantskandeid esindavad pikemad mustad nooled.
- Sissetulekuid laovarudesse esindavad vertikaalsed nooled telje kohal.
- Väljaminek laovarudest on esindatud vertikaalnooltega telje all.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Kuupäevad on eraldatud musta vertikaaljoontega. Kuupäevad on märgitud diagrammi allosas.
- Lao sulgemisi tähistab punased vertikaalsed kriipsjoonelised read.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

## <a name="weighted-average-date-when-marking-is-used"></a>kaalutud keskmine kuupäev märkimist kasutades.

Märkimine on protsess, mis võimaldab teil väljaminekukande siduda või märkida sissetulekukandega. Märkimine võib toimuda nii enne kui pärast kande sisestamist. Saate kasutada märkimist, kui soovite teada laoseisu täpset hinda kande sisestamise või lao sulgemise ajal.

Näiteks võttis teie klienditeenindus oluliselt kliendilt vastu kiirtellimuse. Kuna tegemist on kiirtellimusega, peate maksma kauba eest rohkem, et oma kliendi taotlust kätte saada. Peate olema kindel, et selle müügitellimuse arve puhul kajastub selle laokauba maksumus marginaalis või müüdud kaupade maksumuses (COGS).

Ostutellimuse sisestamisel saadakse laoseis maksumusega 120,00 USD. Kui müügitellimuse dokument märgitakse ostutellimusele enne saatelehe või arve sisestamist, sisestatakse COGS USD 120.00 kauba praeguse jooksva keskmise kulu asemel. Kui märgistus toimub pärast müügitellimuse saatelehe või arve sisestamist, sisestatakse COGS jooksva keskmise omahinnaga.

Enne lao sulgemist saab neid kahte kannet veel üksteisele märkida.

Kui sissetulekukanne on märgitud väljaminekkandeks, eiratakse kauba kauba mudeligrupile valitud hinna määramise meetodit ja süsteem tasakaalustab need kanded üksteise suhtes.

Väljaminekukande saate sissetulekule märkida enne kande sisestamist. Seda saab teha müügitellimuse realt müügitellimuse üksikasjade **lehel**. Avatud sissetulekukanded kuvatakse lehel **Märkimine**.

Samuti saate pärast kande sisestamist märkida väljastuskande sissetulekule. Väljaminekukande saate märkida või vastendada varude korrigeerimistöölehel sisestatud laokauba avatud sissetulekukandega.

Järgnev diagramm näitab järgmisi kandeid:

**1. päev.**

- 1a. Lao füüsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
- 1b. Lao finantsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
- 2a. Lao füüsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
- 2b. Lao finantsiline sissetulek kogusele 1 hinnaga 22,00 USD tükk.
- 3a. Lao füüsiline väljastus, kogus 1, omahind USD 16.00 (finantsiliselt sisestatud kannete jooksev keskmine).
- 3b. Lao finantsiliselt väljaminev kogus 1 omahinnaga USD 16.00 (finantsiliselt sisestatud kannete jooksev keskmine).
- 3c. <a1/&. Lao finantsine väljaminek kande 3b puhul on märgitud lao finantsiküsimusele kande 2b puhul.

**2. päev.**

- 4a. Lao füüsiline sissetulek kogusele 1 hinnaga 25,00 USD tükk.
- 5a. Lao füüsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 5b. Lao finantsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 6a. Lao füüsiline väljastus, kogus 1 omahinnaga USD 23.00 (finantsiliselt sisestatud kannete jooksev keskmine).

**3. päev**

- 7\. Teostatakse lao sulgemine. Märgitud kanded tasakaalustatakse üksteise suhtes, võttes aluseks märkimise põhimõtte, mis kasutab kaalutud keskmise meetodit. Selles näites tasakaalustatakse kanne 3b kandega 2b ja kande korrigeerimine USD 6.00 3b kandesse 3b, et väärtus USD 22.00. Selles näites pole täiendavaid tasakaalustusi tehtud, sest sulgemine loob tasakaalustusi ainult finantsiliselt uuendatud kannete puhul.

Järgnev diagramm näitab seda kannete seeriat ja kaalutud keskmise laomudeli kasutamise efektid koos märkimisega.

![Kaalutud keskmine märkimisega.](media/weighted-average-date-with-marking.png)

**Diagrammi võti:**

- Laokandeid tähistavad vertikaalsed nooled.
- Füüsilisi kandeid esindavad lühemad helehallid nooled.
- Finantskandeid esindavad pikemad mustad nooled.
- Sissetulekuid laovarudesse esindavad vertikaalsed nooled telje kohal.
- Väljaminek laovarudest on esindatud vertikaalnooltega telje all.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Kuupäevad on eraldatud musta vertikaaljoontega. Kuupäevad on märgitud diagrammi allosas.
- Lao sulgemisi tähistab punased vertikaalsed kriipsjoonelised read.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
