---
title: FIFO füüsilise väärtuse ja märkimisega
description: FIFO on laomudel, milles esimesena hangitud sissetulekud väljastatakse esimesena. Finantsiliselt värskendatud väljaminekud laost tasakaalustatakse esimeste finantsiliselt värskendatud lattu minevate sissetulekutega, põhinedes laokannete finantsilisel kuupäeval.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54682
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 663dce9f871e96fec7017616732428c49b1224a0
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676239"
---
# <a name="fifo-with-physical-value-and-marking"></a>FIFO füüsilise väärtuse ja märkimisega

[!include [banner](../includes/banner.md)]


FIFO on varude haldus ja hinna määramise meetod, mille puhul esimesena toodetud või soetatud varusid müüakse, kasutatakse või likvideeritakse esimesena. Microsoft lao sulgemise protsessi ajal Dynamics 365 Supply Chain Management loob süsteem tasakaalustused, kus esimene sissetulek on vastendatud esimese väljaminek jne.

Tasakaalustuste ja sobitamise põhimõte põhinevad laokannete finantskuupäeval. Tasakaalustuste ja korrigeerimiste eelhindamist saab läbi viia lao ümberarvutamise protsessi käivitades.

SAATE FIFO põhimõtte alistada, märkides laokanded nii, et konkreetse kauba sissetulek tasakaalustatakse konkreetse väljaminek. Perioodiline lao sulgemine on vajalik siis, kui kasutate FIFO laomudelit tasakaalustuste loomiseks ja korrigeerite väljaminevate kaupade väärtust FIFO-printsiip põhjal. Lao sulgemise protsessi käivitamiseni väärtussaatakse väljaminek jooksva keskmiseni, kui toimusid füüsilised ja finantsilist uuendused. Kui te ei kasuta märkimist, arvutatakse füüsilise või finantsilise uuendamise ajal jooksev keskmine. Järgmised näited näitavad FIFO kasutamise mõju kolmes eri konfiguratsioonis.

- FIFO valikuta **Füüsilise väärtuse kaasamine**
- FIFO valikuga **Füüsilise väärtuse kaasamine**
- FIFO märkimisega

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO valikuta Füüsilise väärtuse kaasamine

Selles näites tühjendatakse **väljastatud** toote kauba mudeligrupi märkeruut Kaasa füüsiline väärtus. Alloleval joonisel on kuvatud järgmised kanded.

- 1a. Lao füüsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
- 1b. Lao finantsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
- 2a. Lao füüsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
- 2b. Lao finantsiline sissetulek kogusele 1 hinnaga 22,00 USD tükk.
- 3a. Lao füüsiline väljastus, kogus 1, omahind USD 16.00 (finantsiliselt sisestatud kannete jooksev keskmine).
- 3b. Lao finantsiliselt väljaminev kogus 1 omahinnaga USD 16.00 (finantsiliselt sisestatud kannete jooksev keskmine).
- 4a. Lao füüsiline sissetulek kogusele 1 hinnaga 25,00 USD tükk.
- 5a. Lao füüsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 5b. Lao finantsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 6a. Lao füüsiline väljastus, kogus 1, omahind USD 23.00 (finantsiliselt sisestatud kannete jooksev keskmine)
- 7\. Teostatakse lao sulgemine. FIFO meetodil põhinedes tasakaalustatakse esimene finantsiliselt värskendatud väljaminek esimese finantsiliselt värskendatud sissetulekuga jne. Selles näites luuakse üks tasakaalustus vahemikus 1b kuni 3b. Korrigeerimine – 6,00 USD-d tehakse 3b-ks ja tulemuseks saadav lõplik kulu USD 10.00.

Uus keskmise hinna käitamine kajastab finantsiliselt värskendatud kannete keskmist. Järgmised illustratsioonid näitavad FIFO laomudeli mõju sellele kannete seeriale, kui valikut **Füüsilise väärtuse kaasamine** ei kasutata.

![FIFO valikuta Füüsilise väärtuse kaasamine](./media/fifo-without-include-physical-value.png)

**Diagrammi võti**

- Laokandeid tähistavad vertikaalsed nooled.
- Füüsilisi kandeid esindavad lühemad helehallid nooled.
- Finantskandeid esindavad pikemad mustad nooled.
- Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
- Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Iga diagrammi kuupäev on eraldatud mustade vertikaalsete joontega. Kuupäev on märgitud diagrammi allservas.
- Lao sulgemisi tähistab punane vertikaaljoon.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO valikuga Füüsilise väärtuse kaasamine

Kui kauba **puhul on** **kauba** mudeligrupi lehel märgitud ruut Kaasa füüsiline väärtus, kasutab süsteem nii füüsilisi kui finantsilisi sissetulekukandeid jooksva keskmise omahinna arvutamiseks. Vajadusel korrigeerib süsteem ka füüsiliselt värskendatud väljaminekkannet. Lao sulgemine, mis kasutab FIFO laomudelit, teeb tasakaalustusi ainult finantsiliselt uuendatud kannetele. Alloleval joonisel on kuvatud järgmised kanded.

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
- 7\. Teostatakse lao sulgemine. FIFO meetodil põhinedes tasakaalustatakse esimene finantsiliselt värskendatud väljaminek esimese finantsiliselt värskendatud sissetulekuga jne. Selles näites luuakse üks tasakaalustus vahemikus 1b kuni 3b. Korrigeerimine – 6,00 USD-d tehakse 3b-ks ja tulemuseks saadav lõplik kulu USD 10.00. Lisaks korrigeeritakse kanne 6a sissetulekukande kuluks 2b. Süsteem ei tasakaalusta neid kandeid, kuna sissetulek on värskendatud ainult füüsiliselt ja mitte rahaliselt. Selle asemel sisestatakse ainult -1,67 USA dollarit korrigeerimine füüsilise väljamineu kandele ja tulemuseks saadav korrigeeritud kulu USD 22.00.

![FIFO valikuga Füüsilise väärtuse kaasamine](./media/fifo-with-include-physical-value.png)

Pange tähele, et lao sulgemise protsessi käitamine on **sama, sõltumata sellest,** **kas valisite kauba mudeligrupi lehel suvandi Kaasa füüsiline** väärtus. Suvand **Kaasa füüsiline väärtus** mõjutab ainult jooksvat keskmist.

**Diagrammi võti**

- Laokandeid tähistavad vertikaalsed nooled.
- Füüsilisi kandeid esindavad lühemad helehallid nooled.
- Finantskandeid esindavad pikemad mustad nooled.
- Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
- Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Iga diagrammi kuupäev on eraldatud mustade vertikaalsete joontega. Kuupäev on märgitud diagrammi allservas.
- Lao sulgemisi tähistab punane vertikaaljoon.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

## <a name="fifo-with-marking"></a>FIFO märkimisega

Märkimine on protsess, mis võimaldab teil väljaminekukande siduda või märkida sissetulekukandega. Märkimine võib toimuda nii enne kui pärast kande sisestamist. Saate kasutada märkimist, kui soovite teada laoseisu täpset hinda kande sisestamise või lao sulgemise ajal.

Näiteks võttis teie klienditeenindusosakond oluliselt kliendilt vastu kiirtellimuse. Kuna see tellimus on kiirtellimus, peate maksma kauba eest rohkem, et täita oma kliendi nõue. Müügitellimuse arve puhul peate veenduma, et laokauba kulu kajastub marginaalis või müüdud kaupade maksumuses (COGS). Ostutellimuse sisestamisel saadakse laoseis maksumusega 120,00 USD. Kui müügitellimuse dokument märgitakse ostutellimusele enne saatelehe või arve sisestamist, sisestatakse omahind USD 120.00, mitte kauba praegune jooksev keskmine kulu. Kui müügitellimuse saateleht või arve sisestatakse enne märkimist, sisestatakse COGS jooksva keskmise omahinna juurde. Enne lao sulgemist saab neid kahte kannet veel üksteisele märkida.

Kui sissetulekukanne on märgitud väljaminekkandeks, ignoreeritakse kauba mudeligrupis määratletud hinna määramise meetodit ja süsteem tasakaalustab need kanded üksteisega. Kande saate müügitellimuse rea suhtes käsitsi märkida müügitellimuse **üksikasjade** **\>** **lehel, valides müügitellimuse ridade kiirkaardil suvandi Varude** märkimine. Avatud sissetulekukandeid saate vaadata lehel **Märkimine**. Saate vastendada või märkida väljaminek kande avatud sissetuleku kandele laovarude korrigeerimise töölehelt laovarude korrigeerimise töölehel laovarude jaoks. Alloleval joonisel on kuvatud järgmised kanded.

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
- 6a. Lao füüsiline väljastus, kogus 1, omahind USD 23.00 (finantsiliselt sisestatud kannete jooksev keskmine)
- 7\. Teostatakse lao sulgemine. FiFO-meetodit kasutav märgistuspõhimõte põhinedes tasakaalustatakse märgitud kanded üksteise suhtes. Selles näites tasakaalustatakse 3b 2b-ga ja korrigeerimine USD 6.00 sisestatakse 3b-sse, et väärtus USD 22.00. Selles näites pole rohkem tasakaalustusi tehtud, sest sulgemine loob tasakaalustusi ainult finantsiliselt uuendatud kannete puhul.

Järgmine illustratsioon näitab FIFO laomudeli mõju sellele kannete seeriale väljaminekute ja sissetulekute vahelise märkimise kasutamisel.

![FIFO märkimisega.](./media/fifo-with-marking.png)

**Diagrammi võti**

- Laokandeid tähistavad vertikaalsed nooled.
- Füüsilisi kandeid esindavad lühemad helehallid nooled.
- Finantskandeid esindavad pikemad mustad nooled.
- Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
- Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Iga diagrammi kuupäev on eraldatud mustade vertikaalsete joontega. Kuupäev on märgitud diagrammi allservas.
- Lao sulgemisi tähistab punane vertikaaljoon.
- Tasakaalustusi ja märgistusi, mida täidetakse lao sulgemisel, tähistavad punased diagonaalkriipsuga nooled, mis lähevad sissetulekust väljamineki.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
