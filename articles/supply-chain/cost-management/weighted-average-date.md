---
title: Kaalutud keskmine kuupäev
description: Kaalutud keskmine kuupäev on kaalutud keskmise põhimõttel põhinev laomudel, milles laos olevaid kaupu hinnatakse lattu sissetulevate kaupade keskmise väärtuse järgi iga lao sulgemisperioodi päeva lõikes.
author: AndersGirke
manager: tfehr
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Retail
ms.custom: 28991
ms.assetid: 945d5088-a99d-4e54-bc42-d2bd61c61e22
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d36f60a13fbee91100e406150e7f5ca890320436
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982253"
---
# <a name="weighted-average-date"></a>Kaalutud keskmine kuupäev

[!include [banner](../includes/banner.md)]

Kaalutud keskmine kuupäev on kaalutud keskmise põhimõttel põhinev laomudel. Kaalutud keskmise põhimõtte järgi hinnatakse varude väljaminekuid lattu sissetulevate kaupade keskmise väärtuse järgi iga lao sulgemisperioodi päeva lõikes. 

Kui käitate lao sulgemist kaalutud keskmist kuupäeva kasutades, tasakaalustatakse kõik igapäevased sissetulekud virtuaalse väljaminekuga. See virtuaalne väljamineku hoiab kogu vastuvõetud kogust ja väärtust. Sel virtuaalsel väljaminekul on vastav virtuaalne sissetulek, millega väljaminekud tasakaalustatakse. Seega on kõigil väljaminekutel sama keskmine kulu. Virtuaalset väljaminekut ja sissetulekut saab vaadelda kui virtuaalset ülekannet nimega *kaalutud keskmise lao sulgemise ülekanne*. 

Kui sellel kuupäeval või enne seda on toimunud ainult üks sissetulek, ei ole keskmist tarvis hinnata. kõik kaubad on sealt tasakaalustatud ja virtuaalset ülekannet ei looda. Juhul kui antud kuupäeval toimuvad ainult väljaminekud, ei ole ühtegi sissetulekut, mille alusel keskmist hinnata ja virtuaalset ülekannet ei looda. Kaalutud keskmist kuupäeva kasutades saate märkida laokanded nii, et konkreetse kauba sissetulek tasakaalustatakse konkreetse väljamineku suhtes. Sel juhul ei kasutata kaalutud keskmise kuupäeva reeglit. Kui kasutate kaalutud keskmise kuupäeva laomudelit, soovitame igakuist lao sulgemist. 

Kaalutud keskmise kuupäeva kuluarvutusmeetodi arvutamiseks kasutatakse järgmist valemit. 

Kaalutud keskmine = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q*n* × P*n*\]) ÷ (Q1 + Q2 + Q*n*) 

Varude sulgemise ajal tehakse arvutus iga päev sulgemisperioodi kaudu, nagu on näidatud järgmisel joonisel. 

![Kaalutud keskmise kuupäeva igapäevane arvutusmudel](./media/weightedaveragedatedailycalculationmodel.gif) 

Laokanded, millest jäävad varud, nagu müügitellimused, varude töölehed ja tootmistellimused, toimuvad sisestamise päeval eeldatava omahinnaga. Seda eeldatavat omahinda nimetatakse ka keskmiseks jooksevomahinnaks. Varude sulgemise kuupäeval analüüsib süsteem eelmiste perioodide, eelmiste päevade ja jooksva päeva laokandeid. Seda analüüsi kasutatakse, et määrata, millist järgmistest sulgemispõhimõtetest tuleks kasutada.

-   Otsene tasakaalustus
-   Summeeritud tasakaalustus

Tasakaalustused on lao sulgemissisestused, mis korrigeerivad väljaminekud sulgemiskuupäeva seisuga õigele kaalutud keskmisele. 

**Märkus.** Tasakaalustuste kohta lisateabe saamiseks vaadake artiklit varude sulgemise kohta. Järgmised näited illustreerivad kaalutud keskmise kasutamise mõju viie konfiguratsiooniga:

-   kaalutud keskmise kuupäeva otsene tasakaalustus valikut **Kaasa füüsiline väärtus** kasutamata;
-   kaalutud keskmise kuupäeva summeeritud tasakaalustus valikut **Kaasa füüsiline väärtus** kasutamata;
-   kaalutud keskmise kuupäeva otsene tasakaalustus valikut **Kaasa füüsiline väärtus** kasutades;
-   kaalutud keskmise kuupäeva summeeritud tasakaalustus valikut **Kaasa füüsiline väärtus** kasutades;
-   kaalutud keskmine kuupäev märkimist kasutades.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Kaalutud keskmise kuupäeva otsene tasakaalustus valikut Kaasa füüsiline väärtus kasutamata
Praegune versioon kasutab sama otsest tasakaalustuspõhimõtet, mida kasutati varasemate versioonide kaalutud keskmise arvutamiseks. Süsteem tasakaalustab sissetulekud väljaminekutega otseselt. Süsteem kasutab seda otsest tasakaalustamise põhimõtet konkreetsetes olukordades.

-   Perioodi on sisestatud üks sissetulek ja üks või mitu väljaminekut.
-   Perioodi on sisestatud ainult väljaminekud ja varud sisaldavad vabu kaupu eelmisest sulgemisest.

Järgnevas stsenaariumis on sisestatud finantsiliselt värskendatud sissetulek ja väljaminek. Lao sulgemise ajal tasakaalustab süsteem sissetuleku otse väljaminekutega ja mis tahes omahinna korrigeerimist pole väljaminekul vaja. 

Järgmine illustratsioon näitab järgmisi kandeid.

-   1a. Varude füüsilise sissetuleku kogust värskendatakse viie võrra tüki hinnaga 10,00 USA dollarit.
-   1b. Varude finantsilise sissetuleku kogust värskendatakse viie võrra tüki hinnaga 10,00 USA dollarit.
-   2a. Varude füüsilise väljamineku kogust värskendatakse kahe võrra tüki hinnaga 10,00 USA dollarit.
-   2b. Varude finantsilise väljamineku kogust värskendatakse kahe võrra tüki hinnaga 10,00 USA dollarit.
-   3. Lao sulgemine tehakse otsese tasakaalustuse meetodi abil finantsilise sissetuleku tasakaalustamiseks lao finantsilise väljastusega.

![Kaalutud keskmise kuupäeva otsene tasakaalustus ilma valikuta Kaasa füüsiline väärtus](./media/weightedaveragedatedirectsettlementwithoutincludephysicalvalue.gif) 

**Joonise võti**

-   Laokandeid tähistavad vertikaalsed nooled.
-   Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
-   Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
-   Iga vertikaalse noole kohal või all määratletatakse laokande väärtust vormis *Kogus*@*Ühiku hind*.
-   Sulgudes oleva laokande väärtus on füüsiliselt varudesse sisestatud.
-   Kui laokanne ei ole sulgudes, on laokanne varudesse finantsiliselt sisestatud.
-   Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
-   Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste jada ajajoonel.
-   Lao sulgemisi tähistab punane vertikaalne kriipsjoon ja silt *Lao sulgemine*.
-   Lao sulgemisel tehtud tasakaalustused tähistatakse punaste katkendlike nooltega, mis suunduvad diagonaalselt sissetulekust väljaminekuni.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Kaalutud keskmise kuupäeva summeeritud tasakaalustus valikut Kaasa füüsiline väärtus kasutamata
Kaalutud keskmine põhineb põhimõttel, et kõik sulgemisperioodis olevad sissetulekud koondatakse uude laoülekande kandesse. Seda kannet nimetatakse *kaalutud keskmise lao sulgemine*. Kõik päeva sissetulekud tasakaalustatakse äsja loodud laoülekande kande väljaminekuga. Kõik päeva väljaminekud tasakaalustatakse uue laoülekande sissetulekukandega. Kui vaba kaubavaru on pärast lao sulgemist plussis, summeeritakse vaba kaubavaru ja laoväärtus uuel laoülekande kandel (sissetulek). Kui vaba kaubavaru on pärast lao sulgemist miinuses, siis on vaba kaubavaru ja laoväärtus üksikute, veel lõplikult tasakaalustamata väljaminekute summa. 

Järgnevas stsenaariumis on perioodi jooksul sisestatud mitu finantsiliselt uuendatud sissetulekult ja väljaminekut. Lao sulgemise ajal hindab süsteem iga päev seda, kuidas iga päeva tuleks sulgemisel käsitleda. 

Järgmine illustratsioon näitab järgmisi kandeid. 

**1. päev.**

-   1a. Varude füüsilise sissetuleku kogust värskendatakse kolme võrra tüki hinnaga 15,00 USA dollarit.
-   1b. Varude finantsilise sissetuleku kogust värskendatakse kolme võrra tüki hinnaga 15,00 USA dollarit.
-   2a. Varude füüsiline väljastus, kogus 1, jooksev keskmine hind 15,00 USA dollarit.
-   2b. Varude finantsiline väljastus, kogus 1, jooksev keskmine hind 15,00 USA dollarit.

Süsteem kasutab otsese tasakaalustuse 1. päeva jaoks lähenemist. 

**2. päev.**

-   3a. Varude füüsiline väljaminek koguses 1 jooksva keskmise hinnaga 15,00 USA dollarit.
-   3b. Varude finantsiline väljaminek koguses 1 jooksva keskmise hinnaga 15,00 USA dollarit.

Süsteem kasutab otsese tasakaalustuse lähenemist 2. päeva jaoks. 

**3. päev**

-   4a. Varude füüsiline väljaminek koguses 1 jooksva keskmise hinnaga 15,00 USA dollarit.
-   4b. Varude finantsiline väljaminek koguses 1 jooksva keskmise hinnaga 15,00 USA dollarit.
-   5a. Varude füüsiline sissetulek koguses 1 tüki hinnaga 17,00 USA dollarit.
-   5b. Varude finantsiline sissetulek koguses 1 tüki hinnaga 17,00 USA dollarit.

Teostatakse lao sulgemine. Kasutada tuleb otsest tasakaalustust, sest mitu sissetulekut ristub mitme päevaga.

-   7a. Kaalutud keskmise lao sulgemise kande finantsiline väljastus luuakse kogusele 2 hinnaga 32,00 USA dollarit, et summeerida kõikide laofinantsiliste sissetulekute tasakaalustused veel sulgemata päevale.
-   7b. Kaalutud keskmise lao sulgemise kande finantsiline sissetulek luuakse 7a tasakaalustamiseks.

Süsteem loob ja sisestab summeeritud laoülekande kande. Peale selle tasakaalustab süsteem kõik päeva sissetulekud ja eelmiste päevade vaba kaubavaru summeeritud laoülekande väljaminekukandega. Kõik päeva väljaminekud tasakaalustatakse summeeritud laoülekande sissetulekukandega. Kaalutud keskmiseks omahinnaks arvutatakse 16,00 USA dollarit. Väljaminekul on kaalutud keskmise hinna korrigeerimiseks korrigeering 1,00 USA dollarit. Uus keskmine jooksevomahind on 16,00 USA dollarit. 

Järgmine illustratsioon näitab seda kannete seeriat koos kaalutud keskmise laomudeli valimise mõjudega ja summeeritud põhimõtet ilma valikuta **Kaasa füüsiline väärtus**. 

![Kaalutud keskmise kuupäeva summeeritud tasakaalustus ilma valikuta Kaasa füüsiline väärtus](./media/weightedaveragedatesummarizedsettlementwithoutincludephysicalvalue.gif) 

**Joonise võti**

-   Laokandeid tähistavad vertikaalsed nooled.
-   Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
-   Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
-   Iga vertikaalse noole kohal või all määratletatakse laokande väärtust vormis *Kogus*@*Ühiku hind*.
-   Sulgudes oleva laokande väärtus on füüsiliselt varudesse sisestatud.
-   Kui laokanne ei ole sulgudes, on laokanne varudesse finantsiliselt sisestatud.
-   Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
-   Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste jada ajajoonel.
-   Lao sulgemisi tähistab punane vertikaalne kriipsjoon ja silt *Lao sulgemine*.
-   Lao sulgemisel tehtud tasakaalustused tähistatakse punaste katkendlike nooltega, mis suunduvad diagonaalselt sissetulekust väljaminekuni.
-   Punased diagonaalnooled näitavad süsteemi loodud väljaminekukandega tasakaalustatavaid sissetulekukandeid.
-   Roheline nool tähistab süsteemi loodud sissetulekukande vastaskannet, mille suhtes algselt sisestatud väljaminekukanne on tasakaalustatud.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Kaalutud keskmise kuupäeva otsene tasakaalustus valikut Kaasa füüsiline väärtus kasutades
Praegune versioon kasutab kaalutud keskmise jaoks sama otsest tasakaalustuspõhimõtet, mida kasutati varasemates versioonides. Süsteem tasakaalustab sissetulekud väljaminekutega otseselt. Süsteem kasutab seda otsest tasakaalustamise põhimõtet konkreetsetes olukordades.

-   Perioodi on sisestatud üks sissetulek ja üks või mitu väljaminekut.
-   Perioodil sisestati ainult väljaminekud ja ladu hõlmab vaba kaubavaru eelmisest sulgemisest.

Kui märkeruut **Kaasa füüsiline väärtus** on kauba puhul lehel **Kauba mudeligrupp** valitud, kasutab süsteem jooksva keskmise omahinna arvutamiseks nii füüsilisi kui ka finantsilisi sissetulekukandeid. Väljaminekud sisestatakse sellel perioodi jooksul eeldataval omahinnal põhinedes. Lao sulgemise jooksul arvestatakse kaalutud keskmise arvutamisel ainult finantsiliselt värskendatud sissetulekuid.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Kaalutud keskmise kuupäeva summeeritud tasakaalustus valikut Kaasa füüsiline väärtus kasutades
Kui märkeruut **Kaasa füüsiline väärtus** on kauba puhul lehel **Kauba mudeligrupp** valitud, kasutab süsteem jooksva keskmise omahinna arvutamiseks nii füüsilisi kui ka finantsilisi sissetulekukandeid. Väljaminekud sisestatakse sellel perioodi jooksul eeldataval omahinnal põhinedes. Lao sulgemise jooksul arvestatakse kaalutud keskmise arvutamisel ainult finantsiliselt värskendatud sissetulekuid. Kaalutud keskmise tasakaalustamise aluseks on põhimõte, et kõik sulgemisperioodi jäävad sissetulekud liidetakse uude laoülekande kandesse nimega *kaalutud keskmise lao sulgemine*. Kõik päeva sissetulekud tasakaalustatakse äsja loodud laoülekande kande väljaminekuga. Kõik päeva väljaminekud tasakaalustatakse uue laoülekande sissetulekukandega. Kui vaba kaubavaru on pärast lao sulgemist plussis, summeeritakse vaba kaubavaru ja laoväärtus uuel laoülekande kandel (sissetulek). Kui vaba kaubavaru on pärast lao sulgemist miinuses, siis on vaba kaubavaru ja laoväärtus üksikute, veel lõplikult tasakaalustamata väljaminekute summa.

## <a name="weighted-average-date-when-marking-is-used"></a>kaalutud keskmine kuupäev märkimist kasutades.
Märgistamine on protsess, mis võimaldab linkida väljaminekukande sissetulekukandega. Märkimine võib toimuda nii enne kui pärast kande sisestamist. Märkimist saate kasutada, kui tahate olla kindel varude täpses maksumuses, seda kande sisestamisel või lao sulgemisel. 

Näiteks võttis teie klienditeenindus oluliselt kliendilt vastu kiirtellimuse. Kuna tegemist on kiirtellimusega, peate kauba eest kliendi nõude rahuldamiseks rohkem maksma. Peate olema kindel, et selle müügitellimuse arve puhul kajastuks selle laokauba maksumus varus või tuletusreeglis (COGS). Ostutellimuse sisestamisel saadakse laoseis maksumusega 120,00 USD. Müügitellimuse dokument märgitakse ostutellimusele enne, kui saateleht või arve sisestatakse. Sel juhul on COGS kauba praeguse jooksva keskmise asemel 120,00 USA dollarit. Kui müügitellimuse saateleht või arve sisestatakse enne märkimist, sisestatakse COGS jooksva keskmise omahinna juurde. Enne lao sulgemist saab neid kahte kannet veel üksteisele märkida. Kui sissetulekukanne märgitakse väljaminekukandega, eiratakse kauba laomudeli grupis määratletud hinna määramise meetodit. Selle asemel tasakaalustab süsteem nende kanded üksteisega. 

Väljaminekukande saate sissetulekule märkida enne kande sisestamist. Seda saate teha müügitellimuse realt lehel **Müügitellimuse üksikasjad**. Avatud sissetulekukandeid saate vaadata lehel **Märkimine**. Väljaminekukande saate sissetulekule märkida pärast kande sisestamist. Väljaminekukande saate märkida või vastendada varude korrigeerimistöölehel sisestatud laokauba avatud sissetulekukandega. Järgmine illustratsioon näitab järgmisi kandeid.

-   1a. Varude füüsiline sissetulek, kogus 1, tüki omahind 10,00 USA dollarit.
-   1b. Varude finantsiline sissetulek, kogus 1, tüki omahind 10,00 USA dollarit.
-   2a. Varude füüsiline sissetulek, kogus 1, tüki omahind 20,00 USA dollarit.
-   2b. Varude finantsiline sissetulek, kogus 1, tüki omahind 20,00 USA dollarit.
-   3a. Varude füüsiline sissetulek, kogus 1, tüki omahind 25,00 USA dollarit.
-   4a. Varude füüsiline sissetulek, kogus 1, tüki omahind 30,00 USA dollarit.
-   4b. Varude finantsiline sissetulek, kogus 1, tüki omahind 30,00 USA dollarit.
-   5a. Varude füüsiline väljaminek koguses 1 omahinnaga 21,25 USA dollarit (finantsiliselt ja füüsiliselt uuendatud kannete jooksev keskmine).
-   5b. Varude füüsiline väljastus, kogus 1, märgitakse varude sissetulekusse 2b enne kande sisestamist. See kanne sisestatakse omahinnaga 20,00 USA dollarit.
-   6a. Varude füüsiline väljastus, kogus 1, omahind 21,25 USA dollarit.
-   7. Teostatakse lao sulgemine. Kuna finantsiliselt värskendatud kanne märgiti olemasolevale sissetulekule, tasakaalustatakse need kanded üksteisega ja korrigeerimisi ei tehta.

Uus jooksev keskmine omahind kajastab finantsiliselt ja füüsiliselt värskendatud kannete keskmist: 27,50 USD. Järgnev illustratsioon näitab seda kannete seeriat, kaalutud keskmise kuupäeva laomudeli valiku mõju ja märkimist.

![Kaalutud keskmise kuupäev koos märkimisega](./media/weightedaveragedatewithmarking.gif) 

**Joonise võti**

-   Laokandeid tähistavad vertikaalsed nooled.
-   Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
-   Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
-   Iga vertikaalse noole kohal või all määratletatakse laokande väärtust vormis *Kogus*@*Ühiku hind*.
-   Sulgudes oleva laokande väärtus on füüsiliselt varudesse sisestatud.
-   Kui laokanne ei ole sulgudes, on laokanne varudesse finantsiliselt sisestatud.
-   Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
-   Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste jada ajajoonel.
-   Lao sulgemisi tähistab punane vertikaalne kriipsjoon ja silt *Lao sulgemine*.
-   Lao sulgemisel tehtud tasakaalustused tähistatakse punaste katkendlike nooltega, mis suunduvad diagonaalselt sissetulekust väljaminekuni.




