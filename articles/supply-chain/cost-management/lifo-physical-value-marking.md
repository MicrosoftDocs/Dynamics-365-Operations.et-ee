---
title: LIFO füüsilise väärtuse ja märkimisega
description: Viimasena sisse, esimesena välja (LIFO) on kaubavarude meetod, milles viimased (uusimad) sissetulekud väljastatakse esimesena. Laost väljastamine tasakaalustatakse viimaste sissetulekutega lattu, laokande kuupäeva alusel.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 55021
ms.assetid: 49c492b0-b018-44e0-928f-9671e54eee20
ms.search.region: Global
ms.search.industry: Retail
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 792ff4d7b72ce092fe1ad92e53172cf40f0ecf26
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569267"
---
# <a name="lifo-with-physical-value-and-marking"></a>LIFO füüsilise väärtuse ja märkimisega

[!include [banner](../includes/banner.md)]

Viimasena sisse, esimesena välja (LIFO) on kaubavarude meetod, milles viimased (uusimad) sissetulekud väljastatakse esimesena. Laost väljastamine tasakaalustatakse viimaste sissetulekutega lattu, laokande kuupäeva alusel. 

LIFO (viimasena sisse, esimesena välja) on laomudel, mille puhul viimased (uusimad) sissetulekud väljastatakse esimesena. Laost väljastamine tasakaalustatakse viimaste sissetulekutega lattu, laokande kuupäeva alusel. LIFO kasutamisel ei pea te kasutama LIFO-reeglit. Selle asemel saate märkida laokanded nii, et konkreetse kauba väljaminek tasakaalustatakse konkreetse sissetuleku suhtes. Kui kasutate LIFO laomudelit, soovitame perioodilist lao sulgemist. 

Järgmised näited näitavad LIFO kasutamise mõju kolmes eri konfiguratsioonis.

-   LIFO valikuta **Füüsilise väärtuse kaasamine**
-   LIFO valikuga **Füüsilise väärtuse kaasamine**
-   LIFO märkimisega

## <a name="lifo-without-the-include-physical-value-option"></a>LIFO ilma valikuta Füüsilise väärtuse kaasamine
Selles näites pole kauba mudeligrupil füüsilise väärtuse kaasamine märgitud. Alloleval joonisel on kuvatud järgmised kanded.

-   1a. Lao füüsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
-   1b. Lao finantsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
-   2a. Lao füüsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
-   2b. Lao finantsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
-   3a. Lao füüsiline sissetulek kogusele 1 hinnaga 25,00 USD tükk.
-   4a. Lao füüsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
-   4b. Lao finantsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
-   5a. Lao füüsiline väljaminek kogusele 1 omahinnaga 20,00 USA dollarit tükk (finantsiliselt värskendatud kannete jooksev keskmine).
-   5b. Lao finantsiline väljaminek kogusele 1 omahinnaga 20,00 USA dollarit tükk (finantsiliselt värskendatud kannete jooksev keskmine).
-   6. Teostatakse lao sulgemine. LIFO-meetodi alusel tasakaalustatakse viimane rahaliselt värskendatud väljaminek viimase rahaliselt värskendatud sissetuleku suhtes. Väljaminekukandele tehakse 10,00 USA dollarit ulatuses korrigeerimine.

Uus jooksev keskmine omahind kajastab finantsiliselt värskendatud kannete keskmist 15.00 USD juures Järgmine illustratsioon näitab LIFO laomudeli mõju sellele kannete seeriale, kui valikut **Füüsilise väärtuse kaasamine** ei kasutata. 

![LIFO valikuta Kaasa füüsiline väärtus](./media/lifowithoutincludephysicalvalue.gif) 

**Diagrammi võti**

- Laokandeid tähistavad vertikaalsed nooled.
- Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
- Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
- Iga vertikaalse noole kohal (või all) on laokande väärtus määratletud vormingus Quantity@Unit price.
- Sulgudes laokande väärtus näitab, et laokanne on füüsiliselt varudesse sisestatud.
- Sulgudes mitteolev laokande väärtus näitab, et laokanne on finantsiliselt varudesse sisestatud.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Lao sulgemisi tähistab punane vertikaalne kriipsjoon ja silt *Lao sulgemine*.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

## <a name="lifo-with-the-include-physical-value-option"></a>LIFO koos valikuga Füüsilise väärtuse kaasamine
Kui märkeruut **Kaasa füüsiline väärtus** on kauba puhul lehel **Kauba mudeligrupid** valitud, kasutab süsteem jooksva keskmise omahinna arvutamiseks nii füüsilisi kui ka finantsilisi sissetuleku kandeid. Kohaldatavusel korrigeerib süsteem ka füüsiliselt värskendatud väljastuskandeid. Märkeruudu **Kaasa füüsiline väärtus** tühjendamisel teeb lao sulgemine koos LIFO laomudeliga tasakaalustusi ainult finantsiliselt värskendatud kannetega. 

Alloleval joonisel on kuvatud järgmised kanded.

-   1a. Lao füüsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
-   1b. Lao finantsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
-   2a. Lao füüsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
-   2b. Lao finantsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
-   3a. Lao füüsiline sissetulek kogusele 1 hinnaga 25,00 USD tükk.
-   4a. Lao füüsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
-   4b. Lao finantsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
-   5a. Lao füüsiline väljaminek kogusele 1 omahinnaga 21,25 USD tükk (finantsiliste ja füüsiliste värskendatud kannete jooksev keskmine).
-   5b. Lao finantsiline väljaminek kogusele 1 omahinnaga 21,25 USD tükk (finantsiliste ja füüsiliste värskendatud kannete jooksev keskmine).
-   6a. Lao füüsiline sissetulek kogusele 1 omahinnaga 21,25 USD tükk.
-   7. Teostatakse lao sulgemine. LIFO-meetodi alusel korrigeeritakse või tasakaalustatakse viimane väljamineku kanne viimase värskendatud sissetuleku suhtes.

Kanne 6a korrigeeritakse sissetulekukandeks 4b. Süsteem ei tasakaalusta neid kandeid, kuna sissetulek on värskendatud ainult füüsiliselt ja mitte rahaliselt. Selle asemel sisestatakse üksnes 8,75 USA dollarit suurune korrigeering füüsilise väljamineku kandele. Kanne 5b korrigeeritakse füüsilise sissetuleku kandeks 3a. Süsteem ei tasakaalusta neid kandeid, kuna need mõlemad pole rahaliselt värskendatud. Selle asemel korrigeeritakse seda väljaminekukannet ainult USD –3.75 ulatuses. Uus jooksev keskmine omahind kajastab finantsiliselt ja füüsiliselt värskendatud kannete keskmist: 20,00 USA dollarit. 

Järgmine illustratsioon näitab LIFO laomudeli mõju sellele kannete seeriale, kui valikut **Füüsilise väärtuse kaasamine** kasutatakse. 

![LIFO valikuga Kaasa füüsiline väärtus](./media/lifowithincludephysicalvalue.gif) 

**Diagrammi võti**

- Laokandeid tähistavad vertikaalsed nooled.
- Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
- Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
- Iga vertikaalse noole kohal (või all) on laokande väärtus määratletud vormingus Quantity@Unit price.
- Sulgudes laokande väärtus näitab, et laokanne on füüsiliselt varudesse sisestatud.
- Sulgudes mitteolev laokande väärtus näitab, et laokanne on finantsiliselt varudesse sisestatud.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Lao sulgemisi tähistab punane vertikaalne kriipsjoon ja silt *Lao sulgemine*.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

## <a name="lifo-with-marking"></a>LIFO märkimisega
Märkimine on protsess, mis võimaldab teil väljaminekukande siduda või märkida sissetulekukandega. Märkimine võib toimuda nii enne kui pärast kande sisestamist. Saate kasutada märkimist, kui soovite teada laoseisu täpset hinda kande sisestamise või lao sulgemise ajal. Näiteks võttis teie klienditeenindusosakond oluliselt kliendilt vastu kiirtellimuse. Kuna tegemist on kiirtellimusega, peate kliendi nõude täitmiseks maksma kauba eest rohkem. 

Peate veenduma, et selle müügitellimuse arve puhul kajastuks selle laokauba maksumus varus või tuletusreeglis (COGS). Ostutellimuse sisestamisel saadakse laoseis maksumusega 120,00 USD. Kui see müügitellimuse dokument märgitakse ostutellimusele enne saatelehe või arve sisestamist, kasutatakse laokauba kulu (COGS) 120,00 USA dollarit, mitte kauba praegust jooksvat keskmist kulu. Kui müügitellimuse saateleht või arve sisestatakse enne märkimist, sisestatakse COGS jooksva keskmise omahinna juurde. 

Enne lao sulgemist saab neid kahte kannet veel üksteisele märkida. 

Väljaminekukande saate sissetulekule märkida enne kande sisestamist. Seda saate teha müügitellimuse realt lehel **Müügitellimuse üksikasjad**. Avatud sissetulekukandeid saate vaadata lehel **Märkimine**. 

Samuti saate pärast kande sisestamist märkida väljastuskande sissetulekule. Väljaminekukande saate märkida või vastendada varude korrigeerimistöölehel sisestatud laokauba avatud sissetulekukandega. 

Alloleval joonisel on kuvatud järgmised kanded.

-   1a. Lao füüsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
-   1b. Lao finantsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
-   2a. Lao füüsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
-   2b. Lao finantsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
-   3a. Lao füüsiline sissetulek kogusele 1 hinnaga 25,00 USD tükk.
-   4a. Lao füüsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
-   4b. Lao finantsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
-   5a. Lao füüsiline väljaminek kogusele 1 omahinnaga 21,25 USD tükk (finantsiliste ja füüsiliste värskendatud kannete jooksev keskmine).
-   5b. Varude finantsiline väljastus kogusega 1 märgitakse varude sissetulekusse 2b enne kande sisestamist. See kanne sisestatakse omahinnaga 20,00 USD tükk.
-   6a. Lao füüsiline sissetulek kogusele 1 omahinnaga 21,25 USD tükk.
-   7. Teostatakse lao sulgemine. Kuna finantsiliselt värskendatud FIFO-kanne märgitakse olemasolevale sissetulekule, tasakaalustatakse need kanded üksteisega ja korrigeerimisi ei tehta.

Uus jooksev keskmine omahind kajastab finantsiliselt ja füüsiliselt värskendatud kannete keskmist: 27,50 USA dollarit. 

Järgmine illustratsioon näitab LIFO laomudeli mõju sellele kannete seeriale väljaminekute ja sissetulekute vahelise märkimise kasutamisel. 

![LIFO valikuga Märkus](./media/lifowithmarking.gif) 

**Diagrammi võti**

- Laokandeid tähistavad vertikaalsed nooled.
- Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
- Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
- Iga vertikaalse noole kohal (või all) on laokande väärtus määratletud vormingus Quantity@Unit price.
- Sulgudes laokande väärtus näitab, et laokanne on füüsiliselt varudesse sisestatud.
- Sulgudes mitteolev laokande väärtus näitab, et laokanne on finantsiliselt varudesse sisestatud.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Lao sulgemisi tähistab punane vertikaalne kriipsjoon ja silt *Lao sulgemine*.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

