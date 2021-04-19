---
title: FIFO füüsilise väärtuse ja märkimisega
description: FIFO on laomudel, milles esimesena hangitud sissetulekud väljastatakse esimesena. Finantsiliselt värskendatud väljaminekud laost tasakaalustatakse esimeste finantsiliselt värskendatud lattu minevate sissetulekutega, põhinedes laokannete finantsilisel kuupäeval.
author: AndersGirke
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54682
ms.assetid: dc0e2855-83a0-41a7-a398-3c7852597d1a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d37efef723a7ca5e5f2333ff41cdf8351156e9bb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821605"
---
# <a name="fifo-with-physical-value-and-marking"></a>FIFO füüsilise väärtuse ja märkimisega

[!include [banner](../includes/banner.md)]

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
-   5b. Lao finantsiline väljaminek kogusele 1 omahinnaga 15,00 USA dollarit tükk (finantsiliselt värskendatud kannete jooksev keskmine).
-   6. Teostatakse lao sulgemine. FIFO-meetodi põhjal tasakaalustatakse esimene finantsiliselt värskendatud väljaminek esimese finantsiliselt värskendatud sissetulekuga. Väljaminekukandele tehakse 5,00 USA dollari ulatuses korrigeerimine.

Uus keskmise hinna käitamine kajastab finantsiliselt värskendatud kannete keskmist. Järgmised illustratsioonid näitavad FIFO laomudeli mõju sellele kannete seeriale, kui valikut **Füüsilise väärtuse kaasamine** ei kasutata. 

![FIFO valikuta Kaasa füüsiline väärtus](./media/fifowithoutincludephysicalvalue.gif) 

**Diagrammi võti**

- Laokandeid tähistavad vertikaalsed nooled.
- Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
- Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
- Iga vertikaalse noole kohal (või all) on laokande väärtus määratletud vormingus Quantity@Unitprice.
- Sulgudes laokande väärtus näitab, et laokanne on füüsiliselt varudesse sisestatud.
- Sulgudes mitteolev laokande väärtus näitab, et laokanne on finantsiliselt varudesse sisestatud.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Lao sulgemisi tähistab punane vertikaalne kriipsjoon ja silt *Lao sulgemine*.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO valikuga Füüsilise väärtuse kaasamine
Kui märkeruut **Kaasa füüsiline väärtus** on kauba puhul lehel **Kauba mudeligrupp** valitud, kasutab süsteem jooksva keskmise omahinna arvutamiseks nii füüsilisi kui ka finantsilisi sissetuleku kandeid. Kohaldatavusel korrigeerib süsteem ka füüsiliselt värskendatud väljastuskandeid. Märkeruudu **Kaasa füüsiline väärtus** tühjendamisel teeb lao sulgemine koos FIFO laomudeliga tasakaalustusi ainult finantsiliselt värskendatud kannetega. Alloleval joonisel on kuvatud järgmised kanded.

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

Kanne 5b tasakaalustatakse sissetulekukandele 1b. Seda väljamineku kannet korrigeeritakse 11,25 USA dollariga. Uus jooksev keskmine omahind kajastab finantsiliselt ja füüsiliselt värskendatud kannete keskmist: 27,50 USA dollarit. Järgmine illustratsioon näitab FIFO laomudeli mõju sellele kannete seeriale, kui valikut **Füüsilise väärtuse kaasamine** kasutatakse. 

![FIFO valikuga Kaasa füüsiline väärtus](./media/fifowithincludephysicalvalue.gif) 

**Diagrammi võti**

- Laokandeid tähistavad vertikaalsed nooled.
- Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
- Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
- Iga vertikaalse noole kohal (või all) on laokande väärtus määratletud vormingus Quantity@Unitprice.
- Sulgudes laokande väärtus näitab, et laokanne on füüsiliselt varudesse sisestatud.
- Sulgudes mitteolev laokande väärtus näitab, et laokanne on finantsiliselt varudesse sisestatud.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Lao sulgemisi tähistab punane vertikaalne kriipsjoon ja silt *Lao sulgemine*.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

## <a name="fifo-with-marking"></a>FIFO märkimisega
Märkimine on protsess, mis võimaldab teil väljaminekukande siduda või märkida sissetulekukandega. Märkimine võib toimuda nii enne kui pärast kande sisestamist. Saate kasutada märkimist, kui soovite teada laoseisu täpset hinda kande sisestamise või lao sulgemise ajal. Näiteks võttis teie klienditeenindusosakond oluliselt kliendilt vastu kiirtellimuse. Kuna tegemist on kiirtellimusega, peate kliendi nõude täitmiseks maksma kauba eest rohkem. Peate veenduma, et selle müügitellimuse arve puhul kajastuks selle laokauba maksumus varus või tuletusreeglis (COGS). Ostutellimuse sisestamisel saadakse laoseis maksumusega 120,00 USD. Kui see müügitellimuse dokument märgitakse ostutellimusele enne saatelehe või arve sisestamist, kasutatakse laokauba kulu (COGS) 120,00 USA dollarit, mitte kauba praegust jooksvat keskmist kulu. Kui müügitellimuse saateleht või arve sisestatakse enne märkimist, sisestatakse COGS jooksva keskmise omahinna juurde. Enne lao sulgemist saab neid kahte kannet veel üksteisele märkida. Kui sissetulekukanne ühtib väljaminekukandega, eiratakse kaubamudeli grupis määratletud hinna määramise meetodit ja süsteem tasakaalustab need kanded üksteisega. Väljaminekukande saate sissetulekule märkida enne kande sisestamist. Seda saate teha müügitellimuse realt lehel **Müügitellimuse üksikasjad**. Avatud sissetulekukandeid saate vaadata lehel **Märkimine**. Samuti saate pärast kande sisestamist märkida väljastuskande sissetulekule. Väljaminekukande saate märkida või vastendada varude korrigeerimistöölehel sisestatud laokauba avatud sissetulekukandega. Alloleval joonisel on kuvatud järgmised kanded.

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

Uus jooksev keskmine omahind kajastab finantsiliselt ja füüsiliselt värskendatud kannete keskmist: 27,50 USA dollarit. Järgmine illustratsioon näitab FIFO laomudeli mõju sellele kannete seeriale väljaminekute ja sissetulekute vahelise märkimise kasutamisel. 

![FIFO valikuga Märkimine](./media/fifowithmarking.gif) 

**Diagrammi võti**

- Laokandeid tähistavad vertikaalsed nooled.
- Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
- Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
- Iga vertikaalse noole kohal (või all) on laokande väärtus määratletud vormingus Quantity@Unitprice.
- Sulgudes laokande väärtus näitab, et laokanne on füüsiliselt varudesse sisestatud.
- Sulgudes mitteolev laokande väärtus näitab, et laokanne on finantsiliselt varudesse sisestatud.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Lao sulgemisi tähistab punane vertikaalne kriipsjoon ja silt *Lao sulgemine*.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]