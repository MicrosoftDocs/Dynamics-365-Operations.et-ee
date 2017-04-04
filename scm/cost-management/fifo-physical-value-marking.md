---
title: "FIFO füüsilise väärtuse ja märkimisega"
description: "FIFO on laomudel, milles esimesena hangitud sissetulekud väljastatakse esimesena. Finantsiliselt värskendatud väljaminekud laost tasakaalustatakse esimeste finantsiliselt värskendatud lattu minevate sissetulekutega, põhinedes laokannete finantsilisel kuupäeval."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-24 18 - 57 - 00
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 54682
ms.assetid: dc0e2855-83a0-41a7-a398-3c7852597d1a
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8e3d189fc4dbc5c747a3473d3a221c739c323050
ms.lasthandoff: 03/29/2017


---

# <a name="fifo-with-physical-value-and-marking"></a>FIFO füüsilise väärtuse ja märkimisega

FIFO on laomudel, milles esimesena hangitud sissetulekud väljastatakse esimesena. Finantsiliselt värskendatud väljaminekud laost tasakaalustatakse esimeste finantsiliselt värskendatud lattu minevate sissetulekutega, põhinedes laokannete finantsilisel kuupäeval. 

FIFO kasutamisel ei pea te kasutama FIFO-reeglit. Selle asemel saate märkida laokanded nii, et konkreetse kauba sissetulek tasakaalustatakse konkreetse kauba suhtes. FIFO laomudeli kasutamisel soovitame perioodilist lao sulgemist. Järgmised näited näitavad FIFO kasutamise mõju kolmes eri konfiguratsioonis.

-   FIFO valikuta **Füüsilise väärtuse kaasamine**
-   FIFO valikuga **Füüsilise väärtuse kaasamine**
-   FIFO märkimisega

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO valikuta Füüsilise väärtuse kaasamine
Selles näites pole kauba mudeligrupil füüsilise väärtuse kaasamine märgitud. Alloleval joonisel on kuvatud järgmised kanded.

-   1a. Lao füüsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
-   1b. Lao finantsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
-   2a. Lao füüsiline sissetulek kogusele 2 hinnaga 10,00 USD tükk.
-   2b. Lao finantsiline sissetulek kogusele 2 hinnaga 10,00 USD tükk.
-   3a. Lao füüsiline sissetulek kogusele 1 hinnaga 25,00 USD tükk.
-   4a. Lao füüsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
-   4b. Lao finantsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
-   5a. Lao füüsiline väljaminek kogusele 1 omahinnaga 20,00 USA dollarit tükk (finantsiliselt värskendatud kannete jooksev keskmine).
-   5b. Lao finantsiline väljaminek kogusele 1 omahinnaga 20,00 USA dollarit tükk (finantsiliselt värskendatud kannete jooksev keskmine).
-   6. Teostatakse lao sulgemine. FIFO-meetodi põhjal tasakaalustatakse esimene finantsiliselt värskendatud väljaminek esimese finantsiliselt värskendatud sissetulekuga. Väljaminekukandele tehakse 10,00 USA dollari ulatuses korrigeerimine.

Uus keskmise hinna käitamine kajastab finantsiliselt värskendatud kannete keskmist. Järgmised illustratsioonid näitavad FIFO laomudeli mõju sellele kannete seeriale, kui valikut **Füüsilise väärtuse kaasamine** ei kasutata. ![FIFO without Include Physical Value](./media/fifowithoutincludephysicalvalue.gif) **Diagrammi võti**

-   Laokandeid tähistavad vertikaalsed nooled.
-   Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
-   Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
-   Üle (või alla) iga vertikaalse noole laokande väärtus on määratud vormingusQuantity@Unitprice.
-   Sulgudes laokande väärtus näitab, et laokanne on füüsiliselt varudesse sisestatud.
-   Sulgudes mitteolev laokande väärtus näitab, et laokanne on finantsiliselt varudesse sisestatud.
-   Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
-   Each vertical arrow is labeled with a sequential identifier, such as *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
-   Lao sulgemisi tähistab punane vertikaalne kriipsjoon ja silt *Lao sulgemine*.
-   Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO valikuga Füüsilise väärtuse kaasamine
Kui on **kaasa füüsiline väärtus** märkige ruut kauba kohta on **kauba tootemudeli grupi** lehekülg, süsteem kasutab nii füüsiliste ja sissetulekukanded töötab keskmise omahinna arvutamiseks. Kohaldatavusel korrigeerib süsteem ka füüsiliselt värskendatud väljastuskandeid. Märkeruudu **Kaasa füüsiline väärtus** tühjendamisel teeb lao sulgemine koos FIFO laomudeliga tasakaalustusi ainult finantsiliselt värskendatud kannetega. Alloleval joonisel on kuvatud järgmised kanded.

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
-   7. Teostatakse lao sulgemine. FIFO meetodi põhjal kohandatakse või tasakaalustatakse esimest finantsilist väljamineku kannet esimese finantsilise või füüsilise värskendatud sissetulekuga.

Kanne 5b tasakaalustatakse sissetulekukandele 1b. Seda väljamineku kannet korrigeeritakse 11,25 USA dollariga. Uus jooksev keskmine omahind kajastab finantsiliselt ja füüsiliselt värskendatud kannete keskmist: 27,50 USA dollarit. Järgmine illustratsioon näitab FIFO laomudeli mõju sellele kannete seeriale, kui valikut **Füüsilise väärtuse kaasamine** kasutatakse. ![FIFO with Include Physical Value](./media/fifowithincludephysicalvalue.gif) **Diagrammi võti**

-   Laokandeid tähistavad vertikaalsed nooled.
-   Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
-   Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
-   Üle (või alla) iga vertikaalse noole laokande väärtus on määratud vormingusQuantity@Unitprice.
-   Sulgudes laokande väärtus näitab, et laokanne on füüsiliselt varudesse sisestatud.
-   Sulgudes mitteolev laokande väärtus näitab, et laokanne on finantsiliselt varudesse sisestatud.
-   Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
-   Each vertical arrow is labeled with a sequential identifier, such as *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
-   Lao sulgemisi tähistab punane vertikaalne kriipsjoon ja silt *Lao sulgemine*.
-   Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

## <a name="fifo-with-marking"></a>FIFO märkimisega
Märgistus on protsess, mille abil saab linkida või märkida, et sissetulekukande kande. Märkimine võib toimuda nii enne kui pärast kande sisestamist. Saate kasutada märkimist, kui soovite teada laoseisu täpset hinda kande sisestamise või lao sulgemise ajal. Näiteks võttis teie klienditeenindusosakond oluliselt kliendilt vastu kiirtellimuse. Kuna tegemist on kiirtellimusega, peate kliendi nõude täitmiseks maksma kauba eest rohkem. Peate veenduma, et selle müügitellimuse arve puhul kajastuks selle laokauba maksumus varus või tuletusreeglis (COGS). Ostutellimuse sisestamisel saadakse laoseis maksumusega 120,00 USD. Kui see müügitellimuse dokument märgitakse ostutellimusele enne saatelehe või arve sisestamist, kasutatakse laokauba kulu (COGS) 120,00 USA dollarit, mitte kauba praegust jooksvat keskmist kulu. Kui müügitellimuse saateleht või arve sisestatakse enne märkimist, sisestatakse COGS jooksva keskmise omahinna juurde. Enne lao sulgemist saab neid kahte kannet veel üksteisele märkida. Kui sissetulekukande vastab kande, hindamismeetodit, mis on määratletud kauba tootemudeli grupi vastavat ning süsteem lahendab need tehingud omavahel. Väljaminekukande saate sissetulekule märkida enne kande sisestamist. Seda saate teha müügitellimuse realt lehel **Müügitellimuse üksikasjad**. Avatud sissetulekukandeid saate vaadata lehel **Märkimine**. Samuti saate pärast kande sisestamist märkida väljastuskande sissetulekule. Väljaminekukande saate märkida või vastendada varude korrigeerimistöölehel sisestatud laokauba avatud sissetulekukandega. Alloleval joonisel on kuvatud järgmised kanded.

-   1a. Lao füüsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
-   1b. Lao finantsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
-   2a. Lao füüsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
-   2b. Lao finantsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
-   3a. Lao füüsiline sissetulek kogusele 1 hinnaga 25,00 USD tükk.
-   4a. Lao füüsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
-   4b. Lao finantsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
-   5a. Lao füüsiline väljaminek kogusele 1 omahinnaga 21,25 USD tükk (finantsiliste ja füüsiliste värskendatud kannete jooksev keskmine).
-   5b. Varude finantsiline väljastus kogusega 1 märgitakse varude sissetulekusse 2b enne kande sisestamist. Kanne on sisestatud omahinnaga 20,00 USD-d tk.
-   6a. Lao füüsiline sissetulek kogusele 1 omahinnaga 21,25 USD tükk.
-   7. Teostatakse lao sulgemine. Kuna finantsiliselt värskendatud FIFO-kanne märgitakse olemasolevale sissetulekule, tasakaalustatakse need kanded üksteisega ja korrigeerimisi ei tehta.

Uus jooksev keskmine omahind kajastab finantsiliselt ja füüsiliselt värskendatud kannete keskmist: 27,50 USA dollarit. Järgmine illustratsioon näitab FIFO laomudeli mõju sellele kannete seeriale väljaminekute ja sissetulekute vahelise märkimise kasutamisel. ![FIFO with Marking](./media/fifowithmarking.gif) **Diagrammi võti**

-   Laokandeid tähistavad vertikaalsed nooled.
-   Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
-   Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
-   Üle (või alla) iga vertikaalse noole laokande väärtus on määratud vormingusQuantity@Unitprice.
-   Sulgudes laokande väärtus näitab, et laokanne on füüsiliselt varudesse sisestatud.
-   Sulgudes mitteolev laokande väärtus näitab, et laokanne on finantsiliselt varudesse sisestatud.
-   Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
-   Each vertical arrow is labeled with a sequential identifier, such as *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
-   Lao sulgemisi tähistab punane vertikaalne kriipsjoon ja silt *Lao sulgemine*.
-   Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.



