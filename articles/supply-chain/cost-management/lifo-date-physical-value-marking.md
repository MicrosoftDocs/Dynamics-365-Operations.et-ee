---
title: LIFO kuupäev füüsilise väärtuse ja märgistusega
description: Laomudel Viimasena sisse, esimesena välja (LIFO) põhineb LIFO põhimõttel. Laost väljastamine tasakaalustatakse viimaste sissetulekutega lattu, laokande kuupäeva alusel. Kui LIFO-kuupäeva kasutamisel enne väljaminekut sissetulekut pole, tasakaalustatakse väljaminek mis tahes sissetulekuga, mis toimub pärast väljamineku kuupäeva. Mitmed väljaminekud samal päeval tasakaalustatakse viimase väljamineku, viimase sissetuleku järjekorras.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 51592
ms.assetid: d9f13274-3268-444f-85c8-b686fd39286d
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2c06443532519ad5d6c36a6f4ed1f1c4d136664
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967629"
---
# <a name="lifo-date-with-physical-value-and-marking"></a>LIFO kuupäev füüsilise väärtuse ja märgistusega

[!include [banner](../includes/banner.md)]

Laomudel Viimasena sisse, esimesena välja (LIFO) põhineb LIFO põhimõttel. Laost väljastamine tasakaalustatakse viimaste sissetulekutega lattu, laokande kuupäeva alusel. Kui LIFO-kuupäeva kasutamisel enne väljaminekut sissetulekut pole, tasakaalustatakse väljaminek mis tahes sissetulekuga, mis toimub pärast väljamineku kuupäeva. Mitmed väljaminekud samal päeval tasakaalustatakse viimase väljamineku, viimase sissetuleku järjekorras. 

Kui kasutate laomudelit Viimasena sisse, esimesena välja (LIFO kuupäev) ja enne väljastamist sissetulekut pole, tasakaalustatakse väljastus mis tahes sissetulekuga, mis toimub pärast väljastamise kuupäeva. Mitu sama päeva väljastust saab tasakaalustada viimase väljastuse, viimase sisseetuleku järjestuses. LIFO kuupäeva kasutamisel ei pea te kasutama LIFO kuupäeva reeglit. Selle asemel saate märkida laokanded nii, et konkreetse kauba sissetulek tasakaalustatakse konkreetse kauba suhtes. 

Kui kasutate LIFO kuupäeva laomudelit, soovitame perioodilist lao sulgemist. 

Järgmised näited selgitavad LIFO kuupäeva kasutamise mõju kolmes konfiguratsioonis.

-   LIFO kuupäev valikuta **Kaasa füüsiline väärtus**
-   LIFO kuupäev valikuga **Kaasa füüsiline väärtus**
-   LIFO kuupäev märkimisega

## <a name="lifo-date-without-the-include-physical-value-option"></a>LIFO kuupäev füüsilise väärtuse valiku kaasamiseta
Selles näites pole kauba mudeligrupil füüsilise väärtuse kaasamine märgitud. Alloleval joonisel on kuvatud järgmised kanded.

-   1a. Lao füüsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
-   1b. Lao finantsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
-   2a. Lao füüsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
-   2b. Lao finantsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
-   3a. Lao füüsiline sissetulek kogusele 1 hinnaga 25,00 USD tükk.
-   4a. Varude füüsiline väljastus koguse 1 puhul omahinnaga 15,00 USA dollarit (finantsiliselt värskendatud kannete jooksev keskmine).
-   4b. Varude finantsiline väljastus koguse 1 puhul omahinnaga 15,00 USA dollarit (finantsiliselt värskendatud kannete jooksev keskmine).
-   5a. Lao füüsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
-   5b. Lao finantsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
-   6. Teostatakse lao sulgemine. LIFO kuupäeva meetodi põhjal tasakaalustatakse viimane finantsiliselt värskendatud väljastus viimase finantsiliselt värskendatud sissetulekuga kuupäeva kaupa. Korrigeerimine 5,00 USA dollarit tehakse väljastamise kandel. Need kanded tasakaalustatakse üksteisega.

Uus jooksev keskmine omahind kajastab finantsiliselt värskendatud kannete keskmist 15,00 USD juures 

Järgmisel joonisel on kujutatud laomudeli LIFO kuupäev mõju, kui valikut **Kaasa füüsiline väärtus** ei kasutata. ![LIFO kuupäev valikuga Kaasa füüsiline väärtus](./media/lifodatewithoutincludephysicalvalue.gif) 

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

## <a name="lifo-date-with-the-include-physical-value-option"></a>LIFO kuupäev füüsilise väärtuse valiku kaasamisega
Saate märkida kauba puhul ruudu **Kaasa füüsiline väärtus** lehel **Kauba mudeligrupid**. Sellisel juhul kasutab süsteem jooksva keskmise omahinna arvutamiseks nii füüsilisi kui ka finantsilisi sissetulekukandeid. Kohaldatavusel korrigeerib süsteem ka füüsiliselt värskendatud väljastuskandeid. Ruudu **Kaasa füüsiline väärtus** tühjendamisel teeb lao sulgemine, mis kasutab laomudelit LIFO kuupäev, tasakaalustusi ainult finantsiliselt värskendatud kannetele. 

Selles näites on kauba mudeligrupil füüsilise väärtuse kaasamine märgitud. 

Alloleval joonisel on kuvatud järgmised kanded.

-   1a. Lao füüsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
-   1b. Lao finantsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
-   2a. Lao füüsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
-   2b. Lao finantsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
-   3a. Lao füüsiline sissetulek kogusele 1 hinnaga 25,00 USD tükk.
-   4a. Lao füüsiline väljaminek kogusele 1 omahinnaga 18,33 USA dollarit tükk (finantsiliselt värskendatud kannete jooksev keskmine).
-   4b. Varude finantsiline väljastus koguse 1 puhul omahinnaga 18,33 USA dollarit tk (finantsiliselt värskendatud kannete jooksev keskmine).
-   5a. Lao füüsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
-   5b. Lao finantsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
-   6. Teostatakse lao sulgemine. LIFO kuupäeva meetodi põhjal tasakaalustatakse viimasena värskendatud väljastus viimasena värskendatud sissetulekuga kuupäeva kaupa. Neid kandeid ei tasakaalustata üksteisega, sest finantsiline sissetulekukanne korrigeeritakse füüsilise värskendamise kandele. Selle asemel tehakse korrigeerimine 6,67 USA dollarit väljastuskandel.

Uus jooksev keskmine omahind kajastab finantsiliselt värskendatud kannete keskmist 20,00 USD juures 

Järgmisel joonisel on kujutatud laomudeli LIFO mõju, kui kasutatakse valikut **Kaasa füüsiline väärtus**. ![LIFO kuupäev valikuga Kaasa füüsiline väärtus](./media/lifodatewithincludephysicalvalue.gif) 

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

## <a name="lifo-date-with-marking"></a>LIFO kuupäev märkimisega
Märkimine on protsess, mis võimaldab teil väljaminekukande siduda või märkida sissetulekukandega. Märkimine võib toimuda nii enne kui pärast kande sisestamist. Saate kasutada märkimist, kui soovite teada laoseisu täpset hinda kande sisestamise või lao sulgemise ajal. 

Näiteks võttis teie klienditeenindusosakond oluliselt kliendilt vastu kiirtellimuse. Kuna tegemist on kiirtellimusega, peate maksma kauba eest rohkem, et täita kliendi nõudmine. Peate veenduma, et selle müügitellimuse arve puhul kajastuks selle laokauba maksumus varus või tuletusreeglis (COGS). 

Ostutellimuse sisestamisel saadakse laoseis maksumusega 120,00 USD. Kui see müügitellimuse dokument märgitakse ostutellimusele enne saatelehe või arve sisestamist, kasutatakse laokauba kulu (COGS) 120,00 USA dollarit, mitte kauba praegust jooksvat keskmist kulu. Kui müügitellimuse saateleht või arve sisestatakse enne märkimist, sisestatakse COGS jooksva keskmise omahinna juurde. 

Enne lao sulgemist saab neid kahte kannet veel üksteisele märkida. 

Näiteks märgitakse sissetulekukanne väljastuskande jaoks. Sellisel juhul eiratakse kaubamudeli grupis määratletud hinna määramise meetodit ja süsteem tasakaalustab need kanded üksteisega. 

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
-   7. Teostatakse lao sulgemine. Kuna olemasolevale sissetulekule on märgitud finantsiliselt värskendatud kaubavarude hinna määramise elavjärjekorra (FIFO) kanne, tasakaalustatakse need kanded omavahel ja korrektsioone ei tehta.

Uus jooksev keskmine omahind kajastab finantsiliselt ja füüsiliselt värskendatud kannete keskmist: 27,50 USD. 

Järgmisel joonisel on kujutatud laomudeli LIFO mõju, kui kasutatakse väljastuste ja sissetulekute omavahelist märkimist. ![LIFO kuupäev valikuga Märkus](./media/lifodatewithmarking.gif) 

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