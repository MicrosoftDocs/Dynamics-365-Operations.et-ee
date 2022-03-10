---
title: Kaalutud keskmine füüsilise väärtuse ja märgistusega
description: Kaalutud keskmine on laomudel, mis põhineb kaalutud keskmise põhimõttel, kus lao väljaminekuid hinnatakse kauba keskmise väärtuse järgi, mis võetakse lattu vastu lao sulgemise perioodil, samuti iga vaba kaubavaru järgi eelmisest perioodist.
author: AndersGirke
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65501
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c124716b70be837573506a738ef2034397f2bda
ms.sourcegitcommit: addae271ddfc5a8b0721c23337f69916153db4cd
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/21/2022
ms.locfileid: "8330222"
---
# <a name="weighted-average-with-physical-value-and-marking"></a>Kaalutud keskmine füüsilise väärtuse ja märgistusega

[!include [banner](../includes/banner.md)]

Kaalutud keskmine on laomudel, mis põhineb iga komponendi (kauba kande) korrutusteguri (omahind) korrutamisel saadud keskmisel, mis kajastab komponendi tähtsust (kogust). Teine võimalus on see, et kaalutud keskmine on laomudel, mis määrab väljaminekukannete kulu, mis põhineb kogu perioodi jooksul vastuvõetud laoväärtusel, pluss mis tahes vabal kaubavarul eelmisest perioodist.

Kui käivitate lao sulgemise kaalutud keskmise laomudeli abil, on tasakaalustuse loomiseks kaks võimalust. Tavaliselt tasakaalustatakse kõik sissetulekud virtuaalse väljaminek, mis hoiab kogu vastuvõetud kogust ja väärtust. Sel virtuaalsel väljaminekul on vastav virtuaalne sissetulek, millest väljaminekud tasakaalustatakse. Sel viisil on kõigil väljaminekutel sama keskmine kulu. Virtuaalset väljaminek ja sissetulek võivad olla virtuaalsed ülekanded, mille nimi on kaalutud *keskmise lao sulgemise ülekanne*. Seda tasakaalustusmeetodit nimetatakse kaalutud *keskmise summeeritud tasakaalustamiseks*. Ainult ühe kviitungi olemasolul saab kõik väljastused selle kaudu tasakaalustada ja virtuaalset ülekannet ei looda. Seda tasakaalustusmeetodit nimetatakse otseseks *tasakaalustamiseks*. Kõiki laoseisus ladusid, mis on vabad pärast lao sulgemist, arvutatakse eelmise perioodi kaalutud keskmise põhjal ja kaasatakse järgmise perioodi kaalutud keskmise arvutamisse.

Kaalutud keskmise põhimõtte saate alistada laokannete märkimisega nii, et konkreetse kauba sissetulek tasakaalustatakse konkreetse väljaminek. Kui kasutate kaalutud keskmise lao mudelit tasakaalustuste loomiseks ja korrigeerite väljaminevate kaupade väärtust vastavalt kaalutud keskmise põhimõttele, on vajalik perioodiline lao sulgemine. Lao sulgemise protsessi käivitamiseni väärtussaatakse väljaminek jooksva keskmiseni, kui toimusid füüsilised ja finantsilist uuendused. Kui te ei kasuta märkimist, arvutatakse füüsilise või finantsilise uuendamise ajal jooksev keskmine.

Kaalutud keskmise lao kulumeetod järgmise valemiga:

- Kaalutud keskmine = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q *n* × P *n*\]) ÷ (Q1 + Q2 + Q *n*)

Q = kande kogus  
P = kande hind

Tasakaalustused on lao sulgemissisestused, mis korrigeerivad väljaminekud sulgemiskuupäeva seisuga õigele kaalutud keskmisele. Järgmised näited selgitavad kaalutud keskmise kasutamise mõju viie erineva konfiguratsiooniga.

- Kaalutud keskmise otsene tasakaalustus valikuta **Kaasa füüsiline** väärtus
- Kaalutud keskmise summeeritud tasakaalustus valikuta **Kaasa füüsiline** väärtus
- Kaalutud keskmise otsene tasakaalustus valikuga **Kaasa füüsiline** väärtus
- Kaalutud keskmise summeeritud tasakaalustus koos valikuga **Kaasa füüsiline** väärtus
- Kaalutud keskmine märkega

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Kaalutud keskmise otsene tasakaalustus valikuta Kaasa füüsiline väärtus

Otsese tasakaalustamise põhimõte loob tasakaalustuse sissetulekute ja väljaminekte vahel vahetult, loomata täiendavaid laokandeid. Süsteem kasutab seda otsest tasakaalustamise põhimõtet järgmistes olukordades:

- Perioodi on sisestatud üks sissetulek ja üks või mitu väljamist.
- Perioodi on sisestatud ainult väljaminekud ja varud sisaldavad vaba kaubavaru kaupu eelmisest sulgemisest.

Selles näites tühjendatakse **väljastatud** toote **kauba mudeligrupi märkeruut** Kaasa füüsiline väärtus. Alloleval joonisel on kuvatud järgmised kanded.

- 1a. Lao füüsiline sissetulek kogusele 10 hinnaga 10,00 USD tükk.
- 1b. Lao finantsiline sissetulek kogusele 10 hinnaga 10,00 USD tükk.
- 2a. Lao füüsiline sissetulek kogusele 10 hinnaga 20,00 USD tükk.
- 3a. Lao füüsiline väljastus, kogus 1, omahind USD 10.00 (finantsiliselt sisestatud kannete jooksev keskmine).
- 3b. Lao finantsiliselt väljaminev kogus 1 omahinnaga USD 10.00 (finantsiliselt sisestatud kannete jooksev keskmine).
- 4a. Lao füüsiline väljastus koguse 1 eest hinnaga USD 10.00 (finantsiliselt sisestatud kannete jooksev keskmine).
- 4b. Lao finantsiliselt väljaminev kogus 1 USD 10.00 hinnaga (finantsiliselt sisestatud kannete jooksev keskmine).
- 5a. Lao füüsiline väljastus koguse 1 eest hinnaga USD 10.00 (finantsiliselt sisestatud kannete jooksev keskmine).
- 6\. Teostatakse lao sulgemine. Kaalutud keskmise meetodi alusel kasutab süsteem otsese tasakaalustuse meetodit, kuna selles perioodis värskendatakse finantsiliselt ainult üks sissetulek. Selles näites luuakse üks tasakaalustus vahemikus 1b ja 3b ning teine vahemikus 1b kuni 4b. Korrigeerimist ei tehtud, kuna jooksev keskmine on sama, mis kaalutud keskmine.

Järgnev diagramm illustreerib seda **kannete seeriat kaalutud keskmise laomudeli valimise mõjudega ja otsese tasakaalustuse põhimõttega valikuta Kaasa füüsiline** väärtus.

![Kaalutud keskmise DS ilma kaasa füüsilise väärtuseta.](media/weighted-average-direct-settlement-without-include-physical-value.png)

**Diagrammi võti**

- Laokandeid tähistavad vertikaalsed nooled.
- Füüsilisi kandeid esindavad lühemad helehallid nooled.
- Finantskandeid esindavad pikemad mustad nooled.
- Sissetulekuid laovarudesse esindavad vertikaalsed nooled telje kohal.
- Väljaminek laovarudest on esindatud vertikaalnooltega telje all.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Iga diagrammi kuupäev on eraldatud mustade vertikaalsete joontega. Kuupäev on märgitud diagrammi allservas.
- Lao sulgemisi tähistab punane vertikaaljoon.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Kaalutud keskmise summeeritud tasakaalustamine valikuta Kaasa füüsiline väärtus

Kui perioodis on mitu sissetulekut, kasutab kaalutud keskmine summeeritud tasakaalustuspõhimõtet, kus kõik sulgemisperioodi sissetulekud *summeeritakse kandesse nimega kaalutud keskmine lao sulgemine*. Kõik perioodi sissetulekud tasakaalustatakse vastloodud laokande väljaminekuga. Kõik perioodi väljaminekud tasakaalustatakse uue laokande sissetulekuga. Kui pärast lao sulgemist on vaba kaubavaru jääkväärtus, kaasatakse vaba kaubavaru väärtus kaalutud keskmise lao sulgemiskannete sissetulekukandesse.

Järgmisi kandeid illustreeritakse järgmisel joonisel:

- 1a. Lao füüsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
- 1b. Lao finantsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
- 2a. Lao füüsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
- 2b. Lao finantsiline sissetulek kogusele 1 hinnaga 22,00 USD tükk.
- 3a. Lao füüsiline väljastus, kogus 1, omahind USD 16.00 (finantsiliselt sisestatud kannete jooksev keskmine).
- 3b. Lao finantsiliselt väljaminev kogus 1 omahinnaga USD 16.00 (finantsiliselt sisestatud kannete jooksev keskmine).
- 4a. Lao füüsiline sissetulek kogusele 1 hinnaga 25,00 USD tükk.
- 5a. Lao füüsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 5b. Lao finantsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 6a. Lao füüsiline väljastus, kogus 1 omahinnaga USD 23.00 (finantsiliselt sisestatud kannete jooksev keskmine).
- 7\. Teostatakse lao sulgemine.
- 7a. Kaalutud keskmise lao sulgemise kande finantsiline väljaminek luuakse kõigi lao finantsivate sissetulekute tasakaalustuste summeerimiseks.
  - Kanne 1b tasakaalustatakse kogusele 1 tasakaalustatud USD 10.00.
  - Kanne 2b tasakaalustatakse kogusele 1 tasakaalustatud USD 22.00.
  - Kanne 5b tasakaalustatakse kogusele 1 tasakaalustatud USD 30.00.
  - Kanne 7a. Luuakse kogusele 3 tasakaalustatud summagaUSD 62.00. See kanne tasakaalustab kolme selle perioodi jooksul finantsiliselt uuendatud sissetulekukande summa.
- 7b. Kaalutud keskmise lao sulgemise kande finantssissetulek luuakse finantsiliselt sisestatud väljaminevate kaupade vastaskandena.
  - Kanne 3b tasakaalustatakse kogusele 1 tasakaalustatud USD 20.67. Seda kannet korrigeeritakse USD 4.67 nii, et selle algväärtus USD 16.00 20,67-ks, mis on perioodi finantsiliselt sisestatud kannete kaalutud keskmine.
  - Kanne 7b. Luuakse kogusele 1 tasakaalustatud summaga, mis on USD 20.67 3b. See kanne tasakaalustab ühe väljaminekukande summa, mis on perioodi jooksul finantsiliselt uuendatud.

Järgnev diagramm illustreerib **seda kannete seeriat kaalutud keskmise laomudeli valimise mõjudega ja summeeritud tasakaalustamise põhimõttega valikuta Kaasa füüsiline** väärtus.

![Kaalutud keskmise SS ilma kaasa füüsiline väärtus](media/weighted-average-summarized-settlement-without-include-physical-value.png)

**Diagrammi võti**

- Laokandeid tähistavad vertikaalsed nooled.
- Füüsilisi kandeid esindavad lühemad helehallid nooled.
- Finantskandeid esindavad pikemad mustad nooled.
- Sissetulekuid laovarudesse esindavad vertikaalsed nooled telje kohal.
- Väljaminek laovarudest on esindatud vertikaalnooltega telje all.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Iga diagrammi kuupäev on eraldatud mustade vertikaalsete joontega. Kuupäev on märgitud diagrammi allservas.
- Lao sulgemisi tähistab punane vertikaaljoon.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Kaalutud keskmise otsene tasakaalustamine valikuga Kaasa füüsiline väärtus

Parameeter Kaasa **füüsiline väärtus töötab** kaalutud keskmise laomudeliga toote varasematest versioonidest erinevalt. Kui valite **kauba jaoks** **suvandi** Kaasa füüsiline väärtus kauba mudeligrupis, kasutab süsteem eeldatava omahinna või jooksva keskmise arvutamisel füüsiliselt värskendatud sissetulekuid. Väljaminekud sisestatakse sellel perioodi jooksul eeldataval omahinnal põhinedes. Lao sulgemise ajal võetakse kaalutud keskmise arvutamisel arvesse ainult finantsiliselt värskendatud sissetulekud.

Järgmisi kandeid illustreeritakse järgmisel joonisel:

- 1a. Lao füüsiline sissetulek kogusele 10 hinnaga 10,00 USD tükk.
- 1b. Lao finantsiline sissetulek kogusele 10 hinnaga 10,00 USD tükk.
- 2a. Lao füüsiline sissetulek kogusele 10 hinnaga 20,00 USD tükk.
- 3a. Lao füüsiline väljastus, kogus 1 omahinnaga USD 15.00 (füüsiliselt ja finantsiliselt sisestatud kannete jooksev keskmine).
- 3b. Lao finantsiline väljaminev kogus 1 omahinnaga USD 15.00 (füüsiliselt ja finantsiliselt sisestatud kannete jooksev keskmine).
- 4a. Lao füüsiline väljastus kogusele 1 hinnaga USD 15.00 (füüsiliselt ja finantsiliselt sisestatud kannete jooksev keskmine).
- 4b. Lao finantsiline väljaminev kogus 1 USD 15.00 hinnaga (füüsiliselt ja finantsiliselt sisestatud kannete jooksev keskmine).
- 5a. Lao füüsiline väljastus kogusele 1 hinnaga USD 15.00 (füüsiliselt ja finantsiliselt sisestatud kannete jooksev keskmine).
- 6\. Teostatakse lao sulgemine. Kaalutud keskmise meetodi alusel kasutab süsteem otsese tasakaalustuse meetodit, kuna selles perioodis värskendatakse finantsiliselt ainult üks sissetulek. Selles näites luuakse üks tasakaalustus vahemikus 1b ja 3b ning teine vahemikus 1b kuni 4b. Kanne 3b ja 4b korrigeeritakse igaüks -5,00 USD-ga, et tuua väärtus USD 10.00.

Järgnev diagramm illustreerib seda kannete seeriat kaalutud keskmise laomudeli valimise mõjudega ja otsese tasakaalustuse põhimõttega valikuga **Kaasa füüsiline** väärtus.

![Kaalutud keskmise päevade arv koos väärtusega Kaasa füüsiline väärtus.](media/weighted-average-direct-settlement-with-include-physical-value.png)

**Diagrammi võti**

- Laokandeid tähistavad vertikaalsed nooled.
- Füüsilisi kandeid esindavad lühemad helehallid nooled.
- Finantskandeid esindavad pikemad mustad nooled.
- Sissetulekuid laovarudesse esindavad vertikaalsed nooled telje kohal.
- Väljaminek laovarudest on esindatud vertikaalnooltega telje all.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Iga diagrammi kuupäev on eraldatud mustade vertikaalsete joontega. Kuupäev on märgitud diagrammi allservas.
- Lao sulgemisi tähistab punane vertikaaljoon.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Kaalutud keskmise summeeritud tasakaalustamine valikuga Kaasa füüsiline väärtus

Parameeter **Kaasa füüsiline väärtus** töötab kaalutud keskmisega varasemast versioonist erinevalt. Märkige kauba **mudeligrupi** lehel kauba füüsilise väärtuse **ruut Kaasa**. Seejärel kasutab süsteem eeldatava kulu hinna või keskmise arvutamisel füüsiliselt värskendatud sissetulekuid. Väljaminekud sisestatakse sellel perioodi jooksul eeldataval omahinnal põhinedes. Lao sulgemise ajal võetakse kaalutud keskmise arvutamisel arvesse ainult finantsiliselt värskendatud sissetulekud. Kui kasutate kaalutud keskmise lao mudelit, soovitame igakuist lao sulgemist. Selles kaalutud keskmise summeeritud tasakaalustamise näites on laomudel märgitud füüsilist väärtust kaasama.

Järgmisi kandeid illustreeritakse järgmisel joonisel:

- 1a. Lao füüsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
- 1b. Lao finantsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
- 2a. Lao füüsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
- 2b. Lao finantsiline sissetulek kogusele 1 hinnaga 22,00 USD tükk.
- 3a. Lao füüsiline väljastus, kogus 1 omahinnaga USD 16.00 (füüsiliselt ja finantsiliselt sisestatud kannete jooksev keskmine).
- 3b. Lao finantsiline väljaminev kogus 1 omahinnaga USD 16.00 (füüsiliselt ja finantsiliselt sisestatud kannete jooksev keskmine).
- 4a. Lao füüsiline sissetulek kogusele 1 hinnaga 25,00 USD tükk.
- 5a. Lao füüsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 5b. Lao finantsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 6a. Lao füüsiline väljastus, kogus 1 omahinnaga USD 23.67 (füüsiliselt ja finantsiliselt sisestatud kannete jooksev keskmine).
- 7\. Teostatakse lao sulgemine.
- 7a. Kaalutud keskmise lao sulgemise kande finantsiline väljaminek luuakse kõigi lao finantsivate sissetulekute tasakaalustuste summeerimiseks.
  - Kanne 1b tasakaalustatakse kogusele 1 tasakaalustatud USD 10.00.
  - Kanne 2b tasakaalustatakse kogusele 1 tasakaalustatud USD 22.00.
  - Kanne 5b tasakaalustatakse kogusele 1 tasakaalustatud USD 30.00.
  - Kanne 7a. Luuakse kogusele 3 tasakaalustatud summagaUSD 62.00.  
- 7b. Kaalutud keskmise lao sulgemise kande finantssissetulek luuakse finantsiliselt suletud väljamineku kannete vastaskandena.
  - Kanne 3b tasakaalustatakse kogusele 1 tasakaalustatud USD 20.67. Seda kannet korrigeeritakse USD 4.67 nii, et selle algväärtus USD 16.00 20,67-ks, mis on perioodi finantsiliselt sisestatud kannete kaalutud keskmine.
  - Kanne 7b. Luuakse kogusele 1 tasakaalustatud summaga, mis on USD 20.67 3b.

Järgnev diagramm illustreerib **seda kannete seeriat kaalutud keskmise laomudeli valimise mõjudega ja summeeritud tasakaalustamise põhimõttega valikuta Kaasa füüsiline** väärtus.

![Kaalutud keskmise SS koos kaasa füüsilise väärtusega.](media/weighted-average-summarized-settlement-with-include-physical-value.png)

**Diagrammi võti**

- Laokandeid tähistavad vertikaalsed nooled.
- Füüsilisi kandeid esindavad lühemad helehallid nooled.
- Finantskandeid esindavad pikemad mustad nooled.
- Sissetulekuid laovarudesse esindavad vertikaalsed nooled telje kohal.
- Väljaminek laovarudest on esindatud vertikaalnooltega telje all.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Iga diagrammi kuupäev on eraldatud mustade vertikaalsete joontega. Kuupäev on märgitud diagrammi allservas.
- Lao sulgemisi tähistab punane vertikaaljoon.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

## <a name="weighted-average-with-marking"></a>Kaalutud keskmine märkega

Märkimine on protsess, mis võimaldab teil väljaminekukande siduda või märkida sissetulekukandega. Märkimine võib toimuda nii enne kui pärast kande sisestamist. Saate kasutada märkimist, kui soovite teada laoseisu täpset hinda kande sisestamise või lao sulgemise ajal.

Näiteks võttis teie klienditeenindus oluliselt kliendilt vastu kiirtellimuse. Kuna see on kiirtellimus, peate maksma kauba eest rohkem, et oma kliendi taotlust kätte saada. Peate olema kindel, et selle müügitellimuse arve puhul kajastuks selle laokauba maksumus varus või tuletusreeglis (COGS).

Ostutellimuse sisestamisel saadakse laoseis maksumusega 120,00 USD. Näiteks märgitakse müügitellimuse dokument ostutellimusele enne saatelehe või arve sisestamist. Sel juhul on COGS kauba praeguse jooksva keskmise asemel 120,00 USA dollarit. Kui müügitellimuse saateleht või arve sisestatakse enne märkimist, sisestatakse COGS jooksva keskmise omahinna juurde.

Enne lao sulgemist saab neid kahte kannet veel üksteisele märkida.

Sissetulekukanne märgitakse väljastuskandele. Seejärel eiratakse kauba kauba mudeligrupi jaoks valitud hinna määramise meetodit ja süsteem tasakaalustab need kanded üksteisega.

Väljaminekukande saate sissetulekule märkida enne kande sisestamist. Seda saate teha müügitellimuse realt lehel **Müügitellimuse üksikasjad**. Avatud sissetulekukanded kuvatakse lehel **Märkimine**.

Saate pärast kande sisestamist märkida väljaminekukande sissetulekule. Väljaminekukande saate märkida või vastendada varude korrigeerimistöölehel sisestatud laokauba avatud sissetulekukandega.

Järgmisi kandeid illustreeritakse järgmisel joonisel:

- 1a. Lao füüsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
- 1b. Lao finantsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
- 2a. Lao füüsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
- 2b. Lao finantsiline sissetulek kogusele 1 hinnaga 22,00 USD tükk.
- 3a. Lao füüsiline väljastus, kogus 1, omahind USD 16.00 (finantsiliselt sisestatud kannete jooksev keskmine).
- 3b. Lao finantsiliselt väljaminev kogus 1 omahinnaga USD 16.00 (finantsiliselt sisestatud kannete jooksev keskmine).
- 3c. <a1/&. 3b varude finants väljastamis on märgitud 2b varude finantsi aastaseks väljaminekuks.
- 4a. Lao füüsiline sissetulek kogusele 1 hinnaga 25,00 USD tükk.
- 5a. Lao füüsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 5b. Lao finantsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 6a. Lao füüsiline väljastus, kogus 1 omahinnaga USD 23.00 (finantsiliselt sisestatud kannete jooksev keskmine).
- 7\. Teostatakse lao sulgemine. Märgitud kanded tasakaalustatakse üksteise suhtes, võttes aluseks märkimise põhimõtte, mis kasutab kaalutud keskmise meetodit. Selles näites tasakaalustatakse 3b 2b-ga ja korrigeerimine USD 6.00 sisestatakse 3b-sse, et väärtus USD 22.00. Selles näites pole täiendavaid tasakaalustusi tehtud, sest sulgemine loob tasakaalustusi ainult finantsiliselt uuendatud kannete puhul.

Järgnev diagramm illustreerib seda kannete seeriat kaalutud keskmise laomudeli valimise efektidega koos märkimisega.

![Kaalutud keskmine märkusega.](media/weighted-average-with-marking.png)

**Diagrammi võti**

- Laokandeid tähistavad vertikaalsed nooled.
- Füüsilisi kandeid esindavad lühemad helehallid nooled.
- Finantskandeid esindavad pikemad mustad nooled.
- Sissetulekuid laovarudesse esindavad vertikaalsed nooled telje kohal.
- Väljaminek laovarudest on esindatud vertikaalnooltega telje all.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Iga diagrammi kuupäev on eraldatud mustade vertikaalsete joontega. Kuupäev on märgitud diagrammi allservas.
- Lao sulgemisi tähistab punane vertikaaljoon.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
