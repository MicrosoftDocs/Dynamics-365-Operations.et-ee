---
title: Kaalutud keskmine füüsilise väärtuse ja märgistusega
description: Kaalutud keskmine on laomudel, mis põhineb kaalutud keskmise põhimõttel, kus lao väljaminekuid hinnatakse kauba keskmise väärtuse järgi, mis võetakse lattu vastu lao sulgemise perioodil, samuti iga vaba kaubavaru järgi eelmisest perioodist.
author: AndersGirke
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65501
ms.assetid: 25041ff0-bafe-484d-a94a-e1772ad43204
ms.search.region: Global
ms.search.industry: Retail
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d94e61384ad2d0880a6d62b963e9a99518a41db1
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571997"
---
# <a name="weighted-average-with-physical-value-and-marking"></a>Kaalutud keskmine füüsilise väärtuse ja märgistusega

[!include [banner](../includes/banner.md)]

Kaalutud keskmine on laomudel, mis põhineb kaalutud keskmise põhimõttel, kus lao väljaminekuid hinnatakse kauba keskmise väärtuse järgi, mis võetakse lattu vastu lao sulgemise perioodil, samuti iga vaba kaubavaru järgi eelmisest perioodist.

Kui käitate laoseisu sulgemist, tasakaalustatakse kõik sissetulekud virtuaalse väljaminekuga, mis hoiab kogu vastuvõetud kogust ja väärtust. Sel virtuaalsel väljaminekul on vastav virtuaalne sissetulek, millest väljaminekud tasakaalustatakse. Sel viisil on kõigil väljaminekutel sama keskmine kulu. Virtuaalset väljaminekut ja sissetulekut võib vaadata kui virtuaalset ülekannet nimega „kaalutud keskmise lao sulgemise ülekanne”.

Ainult ühe kviitungi olemasolul saab kõik väljastused selle kaudu tasakaalustada ja virtuaalset ülekannet ei looda. 

Kaalutud keskmist kasutades saate märkida laokanded nii, et konkreetse kauba sissetulek tasakaalustatakse konkreetse väljaminekuga, selmet kasutada kaalutud keskmise reeglit. 

Soovitame igakuist lao sulgemist, kui kasutate kaalutud keskmise lao mudelit. 

Kaalutud keskmise lao kulumeetod järgmise valemiga:
-   Kaalutud keskmine = (Q1\*P1 + Q2\*P2 + Qn\*Pn) / (Q1 + Q2 + Qn)

Laokanded, jättes välja varude väljaminekud. See hõlmab müügitellimusi, varude töölehti ja tootmistellimusi, mis toimuvad sisestuskuupäeva eeldatava omahinnaga. Seda eeldatavat omahinda nimetatakse ka käitatud keskmine. Lao sulgemise ajal analüüsib süsteem laokandeid eelmistel ja praegustel perioodidel ning määrab, millist järgnevaist sulgemispõhimõtetest tuleb kasutada.
-   Otsene tasakaalustus
-   Summeeritud tasakaalustus

Tasakaalustused on lao sulgemissisestused, mis korrigeerivad väljaminekud sulgemiskuupäeva seisuga õigele kaalutud keskmisele. Järgmised näited selgitavad kaalutud keskmise kasutamise mõju viie erineva konfiguratsiooniga.
-   Kaalutud keskmise otsene tasakaalustamine valikuta Kaasa füüsiline väärtus
-   Kaalutud keskmise summeeritud tasakaalustamine valikuta Kaasa füüsiline väärtus
-   Kaalutud keskmise otsene tasakaalustamine valikuga Kaasa füüsiline väärtus
-   Kaalutud keskmise summeeritud tasakaalustamine valikuga Kaasa füüsiline väärtus
-   Kaalutud keskmine märkega

## <a name="weighted-average-direct-settlement-without-include-physical-value"></a>Kaalutud keskmise otsene tasakaalustus valikuta Kaasa füüsiline väärtus
Otsene tasakaalustamise põhimõte on sama, mida kasutatakse varasemates versioonides kaalutud keskmise arvutamiseks. Süsteem tasakaalustab otseselt sissetulekute ja väljastuste vahel. Süsteem kasutab seda otsest tasakaalustamise põhimõtet teatud konkreetsetes olukordades.
-   Perioodi on sisestatud üks sissetulek ja üks või mitu väljaminekut
-   Perioodi on sisestatud ainult väljaminekud ja varud sisaldavad vabu kaupu eelmisest sulgemisest

Järgmistes lõikudes kirjeldatud stsenaariumis on sisestatud finantsiliselt värskendatud sissetulek ja väljaminek. Lao sulgemise ajal tasakaalustab süsteem sissetuleku otse väljaminekutega ja mis tahes omahinna korrigeerimist pole väljaminekul vaja. Järgmised kanded on kujutatud joonisel.
-   1a. Lao füüsiline sissetulek värskendatud koguse 5 eest hinnaga 10,00 USD-d tk
-   1b. Lao finantsiline sissetulek värskendatud koguse 5 eest hinnaga 10,00 USD-d tk
-   2a. Lao füüsiline väljaminek värskendatud koguse 2 eest hinnaga 10,00 USD-d tk
-   2b. Lao finantsiline väljaminek värskendatud koguse 2 eest hinnaga 10,00 USD-d tk
-   3. Varud suletakse otsese tasakaalustamise meetodit kasutades, et tasakaalustada varude finantsiline sissetulek varude finantsilise väljaminekuga.

Järgmine joonis selgitab seda kannete seeriat laomudeli Kaalutud keskmine kasutamise mõjuga ja otsese tasakaalustuse põhimõttega valikuta Kaasa füüsiline väärtus. 

![Kaalutud keskmise otsene tasakaalustus füüsilise väärtuse kaasamise valikuta.](./media/weightedaveragedirectsettlementwithoutincludephysicalvalue.gif) 

**Diagrammi võti**
- Laokandeid tähistavad vertikaalsed nooled.
- Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
- Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
- Iga vertikaalse noole kohal (või all) on laokande väärtus määratletud vormingus Quantity@Unitprice.
- Sulgudega ümbritsetud laokande väärtus näitab, et laokanne on füüsiliselt laovarudesse sisestatud.
- Ilma sulgudeta laokande väärtus näitab, et laokanne on rahaliselt laovarudesse sisestatud.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste jada ajajoonel.
- Lao sulgemisi tähistab punane vertikaaljoon ja silt Lao sulgemine.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste katkendjoontega, mis suunduvad diagonaalselt sissetulekust väljaminekuni.

## <a name="weighted-average-summarized-settlement-without-the-include-physical-value-option"></a>Kaalutud keskmise summeeritud tasakaalustamine valikuta Kaasa füüsiline väärtus
Kaalutud keskmine kasutab tasakaalustamise põhimõtet, et kõik sulgemisperioodi jäävad sissetulekud koondatakse kandesse, mida nimetatakse kaalutud keskmise lao sulgemisse. Kõik perioodi sissetulekud tasakaalustatakse äsja loodud laoülekande kande väljaminekuga. Kõik perioodi kaubad tasakaalustatakse äsja loodud laoülekande kande sissetulekuga. Kui vaba kaubavaru on pärast lao sulgemist plussis, summeeritakse vaba kaubavaru ja laoväärtus uuel laoülekande kandel (sissetulek). Kui vaba kaubavaru on pärast lao sulgemist miinuses, siis on vaba kaubavaru ja laoväärtus üksikute, veel lõplikult tasakaalustamata kaupade summa. Allnäidatud stsenaariumis on mitmed finantsiliselt värskendatud sissetulekud ja üks väljaminek sisestatud. 

Lao sulgemise jooksul loob ja sisestab süsteem summeeritud laoülekande kande tasakaalustamaks kõik perioodi sissetulekud summeeritud laoülekande väljaminekukandes. Kõik perioodiks sisestatud väljaminekud tasakaalustatakse summeeritud laoülekande sissetulekukandega. Kaalutud keskmiseks on arvutatud 15,00 USD-d. Väljaminek sisestati algselt eeldatava omahinnaga 14,67 USA dollarit. Seetõttu luuakse ja sisestatakse väljaminekul negatiivne korrigeerimine 0,33 USA dollarit. Lao sulgemiskuupäevast on vaba kaubavaru 3 tk väärtusega 45,00 USD-d. 

Järgmisi kandeid illustreeritakse alloleval pildil:
-   1a. Lao füüsiline sissetulek värskendatud kogusele 2 hinnaga 11,00 USD tükk.
-   1b. Lao finantsiline sissetulek värskendatud kogusele 2 hinnaga 14,00 USD tükk.
-   2a. Lao füüsiline sissetulek värskendatud kogusele 1 hinnaga 12,00 USD tükk.
-   2b. Lao finantsiline sissetulek värskendatud koguse 1 eest hinnaga 16,00 USD-d tk.
-   3a. Lao füüsiline väljaminek värskendatud koguse 1 eest hinnaga 14,67 USD-d tk (käitatud keskmine).
-   3b. Lao finantsiline väljaminek värskendatud koguse 1 eest hinnaga 14,67 USD-d tk (käitatud keskmine).
-   4a. Lao füüsiline sissetulek värskendatud kogusele 1 hinnaga 14,00 USD tükk.
-   4b. Lao finantsiline sissetulek värskendatud koguse 1 eest hinnaga 16,00 USD-d tk.
-   5. Teostatakse lao sulgemine.
-   6a. "Kaalutud keskmise lao sulgemise kande" finantsiline väljaminek luuakse kõigi lao finantsiliste sissetulekute tasakaalustuste summeerimiseks.
-   6b. "Kaalutud keskmise lao sulgemise kande" finantsiline sissetulek luuakse 5a tasakaalustamiseks.

Järgmine joonis selgitab seda kannete seeriat laomudeli Kaalutud keskmine kasutamise mõjuga ja summeeritud tasakaalustuse põhimõttega valikuta Kaasa füüsiline väärtus. 

![Kaalutud keskmise summeeritud tasakaalustus füüsilist väärtust kaasamata.](./media/weightedaveragesummarizedsettlementwithoutincludephysicalvalue.gif) 

**Diagrammi võti**
- Laokandeid tähistavad vertikaalsed nooled.
- Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
- Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
- Iga vertikaalse noole kohal (või all) on laokande väärtus määratletud vormingus Quantity@Unitprice.
- Sulgudega ümbritsetud laokande väärtus näitab, et laokanne on füüsiliselt laovarudesse sisestatud.
- Ilma sulgudeta laokande väärtus näitab, et laokanne on rahaliselt laovarudesse sisestatud.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste jada ajajoonel.
- Lao sulgemisi tähistab punane vertikaaljoon ja silt Lao sulgemine.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste katkendjoontega, mis suunduvad diagonaalselt sissetulekust väljaminekuni.
- Punased nooled illustreerivad sissetulekukandeid, mis tasakaalustatakse süsteemi loodud väljaminekukannete suhtes.
- Roheline nool tähistab süsteemi loodud sissetulekukande vastaskannet mille suhtes algselt sisestatud väljaminekukanne on tasakaalustatud

## <a name="weighted-average-direct-settlement-with-the-include-physical-value-option"></a>Kaalutud keskmise otsene tasakaalustamine valikuga Kaasa füüsiline väärtus
Parameeter Kaasa füüsiline väärtus töötab parameeter kaalutud keskmise laomudeliga toote eelmistest versioonidest erinevalt. Saate märkida kauba puhul ruudu Kaasa füüsiline väärtus vormil Kauba mudeligrupp. Seejärel kasutab süsteem eeldatava kulu hinna või keskmise arvutamisel füüsiliselt värskendatud sissetulekuid. Väljaminekud sisestatakse perioodi vältel hinnangulise omahinna alusel. Lao sulgemise ajal võetakse kaalutud keskmise arvutamisel arvesse ainult finantsiliselt värskendatud sissetulekud. Kui kasutate kaalutud keskmise lao mudelit, soovitame igakuist lao sulgemist. Selles kaalutud keskmise otsese tasakaalustamise näites on kauba mudeligrupp märgitud füüsilist väärtust kaasama. 

Järgmisi kandeid illustreeritakse alloleval pildil:
-   1a. Lao füüsiline sissetulek värskendatud kogusele 1 hinnaga 11,00 USD tükk.
-   1b. Lao finantsiline sissetulek värskendatud kogusele 1 hinnaga 10,00 USD tükk.
-   2a. Lao füüsiline sissetulek värskendatud kogusele 1 hinnaga 15,00 USD tükk.
-   3a. Lao füüsiline väljaminek värskendatud koguse 1 eest hinnaga 12,50 USD-d tk (jooksev keskmine omahind, kuna füüsilise sissetuleku väärtus on arvestatud).
-   3b. Lao finantsiline väljaminek värskendatud koguse 1 eest hinnaga 12,50 USD-d tk (jooksev keskmine omahind, kuna füüsilise sissetuleku väärtus on arvestatud).
-   4. Teostatakse lao sulgemine. Lao sulgemise jooksul ignoreerib süsteem kõiki laokandeid, mida on ainult füüsiliselt värskendatud. Selle asemel rakendatakse otsese tasakaalustamise põhimõtet, sest olemas on ainult üks finantsiline sissetulek. 2,50 USD suurune korrektuur sisestatakse laokandesse, mis on finantsiliselt välja antud lao sulgemiskuupäevast. Pärast lao sulgemist on vaba kaubavaru koguseks 1 jooksva keskmise hinnaga 15,00 USD-d.

Järgmine joonis selgitab seda kannete seeriat laomudeli Kaalutud keskmine kasutamise mõjuga ja otsese tasakaalustuse põhimõttega valikuga Kaasa füüsiline väärtus. 

![Kaalutud keskmise otsene tasakaalustus füüsilise väärtuse valikut kaasamata.](./media/weightedaveragedirectsettlementwithincludephysicalvalue.gif) 

**Diagrammi võti**
- Laokandeid tähistavad vertikaalsed nooled.
- Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
- Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
- Iga vertikaalse noole kohal (või all) on laokande väärtus määratletud vormingus Quantity@Unitprice.
- Sulgudega ümbritsetud laokande väärtus näitab, et laokanne on füüsiliselt laovarudesse sisestatud.
- Ilma sulgudeta laokande väärtus näitab, et laokanne on rahaliselt laovarudesse sisestatud.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste jada ajajoonel.
- Lao sulgemisi tähistab punane vertikaaljoon ja silt Lao sulgemine.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste katkendjoontega, mis suunduvad diagonaalselt sissetulekust väljaminekuni.

## <a name="weighted-average-summarized-settlement-with-the-include-physical-value-option"></a>Kaalutud keskmise summeeritud tasakaalustamine valikuga Kaasa füüsiline väärtus
Parameeter Kaasa füüsiline väärtus töötab varasemates versioonides kaalutud keskmisega teistmoodi. Saate märkida kauba puhul ruudu Kaasa füüsiline väärtus lehel Kauba mudeligrupp. Seejärel kasutab süsteem eeldatava kulu hinna või keskmise arvutamisel füüsiliselt värskendatud sissetulekuid. Väljaminekud sisestatakse sellel perioodi jooksul eeldataval omahinnal põhinedes. Lao sulgemise jooksul arvestatakse kaalutud keskmise arvutamisel ainult finantsiliselt värskendatud sissetulekuid. Kui kasutate kaalutud keskmise lao mudelit, soovitame igakuist lao sulgemist. Selles kaalutud keskmise summeeritud tasakaalustamise näites on laomudel märgitud füüsilist väärtust kaasama. 

Järgmisi kandeid illustreeritakse alloleval pildil:
-   1a. Lao füüsiline sissetulek värskendatud kogusele 2 hinnaga 11,00 USD tükk.
-   1b. Lao finantsiline sissetulek värskendatud kogusele 2 hinnaga 14,00 USD tükk.
-   2. Lao füüsiline sissetulek värskendatud kogusele 1 hinnaga 10,00 USD tükk.
-   3a. Lao füüsiline sissetulek värskendatud kogusele 1 hinnaga 12,00 USD tükk.
-   3b. Lao finantsiline sissetulek värskendatud koguse 1 eest hinnaga 16,00 USD-d tk.
-   4a. Lao füüsiline väljaminek värskendatud koguse 1 eest hinnaga 13,50 USD-d tk (jooksev keskmine omahind, kuna füüsilise sissetuleku väärtus on arvestatud).
-   4b. Lao finantsiline väljaminek värskendatud koguse 1 eest hinnaga 13,50 USD-d tk (jooksev keskmine omahind, kuna füüsilise sissetuleku väärtus on arvestatud).
-   5a. Lao füüsiline sissetulek värskendatud kogusele 1 hinnaga 14,00 USD tükk.
-   5b. Lao finantsiline sissetulek värskendatud koguse 1 eest hinnaga 16,00 USD-d tk.
-   6. Teostatakse lao sulgemine. Lao sulgemise jooksul ignoreerib süsteem kõiki laokandeid, mis on ainult füüsiliselt värskendatud. Rakendatakse summeeritud tasakaalustamise põhimõtet, sest olemas on ainult üks finantsiline sissetulek. 1,50 USD suurune korrektuur sisestatakse laokandesse, mis on finantsiliselt välja antud lao sulgemiskuupäevast. Pärast lao sulgemist on vaba kaubavaru koguseks 3 jooksva keskmise hinnaga 15,00 USD-d.
-   7a. "Kaalutud keskmise lao sulgemise kande" finantsiline väljaminek luuakse kõigi lao finantsiliste sissetulekute tasakaalustuste summeerimiseks.
-   7b. "Kaalutud keskmise lao sulgemise kande" finantsiline sissetulek luuakse 5a tasakaalustamiseks.

Järgmine joonis selgitab seda kannete seeriat laomudeli Kaalutud keskmine kasutamise mõjuga ja summeeritud tasakaalustuse põhimõttega valikuta Kaasa füüsiline väärtus. 

![Kaalutud keskmise summeeritud tasakaalustus füüsilise väärtuse kaasamise valikuga.](./media/weightedaveragesummarizedsettlementwithincludephysicalvalue.gif) 

**Diagrammi võti**
- Laokandeid tähistavad vertikaalsed nooled.
- Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
- Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
- Iga vertikaalse noole kohal (või all) on laokande väärtus määratletud vormingus Quantity@Unitprice.
- Sulgudega ümbritsetud laokande väärtus näitab, et laokanne on füüsiliselt laovarudesse sisestatud.
- Ilma sulgudeta laokande väärtus näitab, et laokanne on rahaliselt laovarudesse sisestatud.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt 1a. Identifikaatorid näitavad laokannete sisestuste jada ajajoonel.
- Lao sulgemisi tähistab punane vertikaaljoon ja silt Lao sulgemine.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste katkendjoontega, mis suunduvad diagonaalselt sissetulekust väljaminekuni.
- Punased nooled illustreerivad sissetulekukandeid, mis tasakaalustatakse süsteemi loodud väljaminekukannete suhtes.
- Roheline nool tähistab süsteemi loodud sissetulekukande vastaskannet mille suhtes algselt sisestatud väljaminekukanne on tasakaalustatud

## <a name="weighted-average-with-marking"></a>Kaalutud keskmine märkega
Märkimine on protsess, mis võimaldab teil väljaminekukande siduda või märkida sissetulekukandega. Märkimine võib toimuda nii enne kui pärast kande sisestamist. Saate kasutada märkimist, kui soovite teada laoseisu täpset hinda kande sisestamise või lao sulgemise ajal. 

Näiteks võttis teie klienditeenindus oluliselt kliendilt vastu kiirtellimuse. Kuna tegemist on kiirtellimusega, peate maksma kauba eest rohkem, et täita kliendi nõuet. Peate olema kindel, et selle müügitellimuse arve puhul kajastuks selle laokauba maksumus varus või tuletusreeglis (COGS). 

Ostutellimuse sisestamisel saadakse laoseis maksumusega 120,00 USD. Näiteks märgitakse müügitellimuse dokument ostutellimusele enne saatelehe või arve sisestamist. Sel juhul on COGS kauba praeguse jooksva keskmise asemel 120,00 USA dollarit. Kui müügitellimuse saateleht või arve sisestatakse enne märkimist, sisestatakse COGS jooksva keskmise omahinna juurde. 

Enne lao sulgemist saab neid kahte kannet veel üksteisele märkida. 

Sissetulekukanne märgitakse väljastuskandele. Seejärel eiratakse kauba mudeligrupile valitud hindamismeetodit ja süsteem tasakaalustab nende kanded üksteisega. 

Väljaminekukande saate sissetulekule märkida enne kande sisestamist. Saate seda teha müügitellimuse realt lehel Müügitellimuse üksikasjad. Avatud sissetulekukandeid saab vaadata lehel Märkimine. 

Saate pärast kande sisestamist märkida väljaminekukande sissetulekule. Väljaminekukande saate märkida või vastendada varude korrigeerimistöölehel sisestatud laokauba avatud sissetulekukandega. 

Järgmisi kandeid illustreeritakse alloleval pildil:
-   1a. Lao füüsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
-   1b. Lao finantsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
-   2a. Lao füüsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
-   2b. Lao finantsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
-   3a. Lao füüsiline sissetulek kogusele 1 hinnaga 25,00 USD tükk.
-   4a. Lao füüsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
-   4b. Lao finantsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
-   5a. Lao füüsiline väljaanne koguse 1 eest hinnaga 21,25 USD-d (käitades finantsiliselt ja füüsiliselt uuendatud kannete keskmist).
-   5b. Lao finantsiline väljaanne koguse 1 eest on märgitud lao sissetulekule 2b enne kande sisestamist. Kanne on sisestatud omahinnaga 20,00 USD-d.
-   6a. Lao füüsiline sissetulek kogusele 1 omahinnaga 21,25 USD tükk.
-   7. Ladu sulgetakse. Kuna finantsiliselt värskendatud kanne on märgitud olemasolevale sissetulekule, on need kanded üksteise suhtes tasakaalustatud ja korrektuure ei tehta.

Uus jooksev keskmine omahind kajastab finantsiliselt ja füüsiliselt värskendatud kannete keskmist: 27,50 USD. 

Järgnev diagramm illustreerib seda kannete seeriat Kaalutud keskmise laomudeli valiku mõjudega märkega. 

![Kaalutud keskmine märkusega.](./media/weightedaveragewithmarking.gif) 

**Diagrammi võti**
- Laokandeid tähistavad vertikaalsed nooled.
- Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
- Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
- Iga vertikaalse noole kohal (või all) on laokande väärtus määratletud vormingus Quantity@"Unitprice".
- Sulgudega ümbritsetud laokande väärtus näitab, et laokanne on füüsiliselt laovarudesse sisestatud.
- Ilma sulgudeta laokande väärtus näitab, et laokanne on rahaliselt laovarudesse sisestatud.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste jada ajajoonel.
- Lao sulgemisi tähistab punane vertikaaljoon ja silt Lao sulgemine.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste katkendjoontega, mis suunduvad diagonaalselt sissetulekust väljaminekuni.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]