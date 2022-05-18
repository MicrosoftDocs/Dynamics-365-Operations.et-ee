---
title: LIFO füüsilise väärtuse ja märkimisega
description: Viimasena sisse, esimesena välja (LIFO) on kaubavarude meetod, milles viimased (uusimad) sissetulekud väljastatakse esimesena. Laost väljastamine tasakaalustatakse viimaste sissetulekutega lattu, laokande kuupäeva alusel.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55021
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 45316c40cce988c0758e70af627b0123ec1f7873
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670436"
---
# <a name="lifo-with-physical-value-and-marking"></a>LIFO füüsilise väärtuse ja märkimisega

[!include [banner](../includes/banner.md)]

Viimasena sisse, esimesena välja (LIFO) on varude haldus ja hinna määramise meetod, kus viimati toodetud või hangitud varusid müüakse, kasutatakse või likvideeritakse esimesena. Microsoft lao sulgemise protsessi ajal Dynamics 365 Supply Chain Management loob süsteem tasakaalustusi, kus viimane sissetulek on vastendatud esimese väljaminek jne. Tasakaalustuste ja sobitamise põhimõte põhinevad laokannete finantskuupäeval. Tasakaalustuste ja korrigeerimiste eelhindamist saab läbi viia lao ümberarvutamise protsessi käivitades.

Saate LIFO põhimõtte alistada laokannete märkimisega nii, et konkreetse kauba sissetulek tasakaalustatakse konkreetse väljaminek. Perioodiline lao sulgemine on vajalik siis, kui kasutate LIFO laomudelit tasakaalustuste loomiseks ja väljaminevate kaupade väärtuse korrigeerimiseks vastavalt LIFO põhimõttele. Lao sulgemise protsessi käivitamiseni väärtussaatakse väljaminek jooksva keskmiseni, kui toimusid füüsilised ja finantsilist uuendused. Kui te ei kasuta märkimist, arvutatakse füüsilise või finantsilise uuendamise ajal jooksev keskmine.

Järgmised näited näitavad LIFO kasutamise mõju kolmes eri konfiguratsioonis.

- LIFO valikuta **Füüsilise väärtuse kaasamine**
- LIFO valikuga **Füüsilise väärtuse kaasamine**
- LIFO märkimisega

## <a name="lifo-without-the-include-physical-value-option"></a>LIFO ilma valikuta Füüsilise väärtuse kaasamine

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
- 7\. Teostatakse lao sulgemine. LIFO-meetodil põhinedes tasakaalustatakse esimene finantsiliselt värskendatud väljaminek viimase finantsiliselt värskendatud sissetulekuga jne. Selles näites luuakse üks tasakaalustus vahemikus 5b kuni 3b. Korrigeeritakse USD 14.00 3b-ks ja tulemuseks saadav lõplik kulu USD 30.00.

Järgmine illustratsioon näitab FIFO laomudeli mõju sellele kannete seeriale, kui valikut **Füüsilise väärtuse kaasamine** ei kasutata.

![LIFO valikuta Füüsilise väärtuse kaasamine](./media/lifo-without-including-physical-value.png)

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

## <a name="lifo-with-the-include-physical-value-option"></a>LIFO koos valikuga Füüsilise väärtuse kaasamine

Kui kauba **puhul on** **lehel** Kauba mudeligrupid märgitud ruut Kaasa füüsiline väärtus, kasutab süsteem nii füüsilisi kui finantsilisi sissetulekukandeid jooksva keskmise omahinna arvutamiseks. Vajadusel korrigeerib süsteem ka füüsiliselt värskendatud väljaminekkannet. Kui märkeruut **Kaasa füüsiline väärtus on** tühjendatud, teeb LIFO laomudelit kasutav lao sulgemine tasakaalustusi ainult kannetele, mis on finantsiliselt uuendatud.

Alloleval joonisel on kuvatud järgmised kanded.

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
- 7\. Teostatakse lao sulgemine. LIFO-meetodil põhinedes tasakaalustatakse esimene finantsiliselt värskendatud väljaminek viimase finantsiliselt värskendatud sissetulekuga jne. Selles näites luuakse üks tasakaalustus vahemikus 3b kuni 5b. Korrigeeritakse USD 14.00 3b-ks ja tulemuseks saadav lõplik kulu USD 30.00. Lisaks korrigeeritakse kanne 6a sissetulekukande kuluks 4a. Süsteem ei tasakaalusta neid kandeid, kuna sissetulek on värskendatud ainult füüsiliselt ja mitte rahaliselt. Selle asemel sisestatakse ainult USD 1.33 korrigeerimine füüsilise väljamineu kandesse ja tulemuseks saadav korrigeeritud kulu USD 25.00.

Järgmine illustratsioon näitab LIFO laomudeli mõju sellele kannete seeriale, kui valikut **Füüsilise väärtuse kaasamine** kasutatakse.

![LIFO valikuga Füüsilise väärtuse kaasamine.](./media/lifo-with-included-physical-value.png)

**Diagrammi võti**

- Laokandeid tähistavad vertikaalsed nooled.
- Füüsilisi kandeid esindavad lühemad helehallid nooled.
- Finantskandeid esindavad pikemad mustad nooled.
- Sissetulekuid laovarudesse esindavad vertikaalsed nooled telje kohal.
- Väljaminek laovarudest on esindatud vertikaalnooltega telje all.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Iga diagrammi kuupäev on eraldatud mustade vertikaalsete joontega. Kuupäev on märgitud diagrammi allosas.
- Lao sulgemisi tähistab punane vertikaaljoon.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

## <a name="lifo-with-marking"></a>LIFO märkimisega

Märkimine on protsess, mis võimaldab teil väljaminekukande siduda või märkida sissetulekukandega. Märkimine võib toimuda nii enne kui pärast kande sisestamist. Saate kasutada märkimist, kui soovite teada laoseisu täpset hinda kande sisestamise või lao sulgemise ajal. Näiteks võttis teie klienditeenindusosakond oluliselt kliendilt vastu kiirtellimuse. Kuna see tellimus on kiirtellimus, peate maksma kaubale rohkem, et kliendi taotlust täita.

Müügitellimuse arve puhul peate veenduma, et laokauba kulu kajastub marginaalis või müüdud kaupade maksumuses (COGS). Ostutellimuse sisestamisel saadakse laoseis maksumusega 120,00 USD. Kui see müügitellimuse dokument märgitakse ostutellimusele enne saatelehe või arve sisestamist, kasutatakse laokauba kulu (COGS) 120,00 USA dollarit, mitte kauba praegust jooksvat keskmist kulu. Kui müügitellimuse saateleht või arve sisestatakse enne märkimist, sisestatakse COGS jooksva keskmise omahinna juurde.

Enne lao sulgemist saab neid kahte kannet veel üksteisele märkida.

Väljaminekukande saate sissetulekule märkida enne kande sisestamist. Seda märgistust saate teha müügitellimuse realt **müügitellimuse** **\>** **üksikasjade lehel, valides lao märkimise müügitellimuse ridade kiirkaardil.** Avatud sissetulekukandeid saate vaadata lehel **Märkimine**.

Samuti saate pärast kande sisestamist märkida väljastuskande sissetulekule. Väljaminekukande saate märkida või vastendada varude korrigeerimistöölehel sisestatud laokauba avatud sissetulekukandega.

Alloleval joonisel on kuvatud järgmised kanded.

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
- 7\. Teostatakse lao sulgemine. LIFO-meetodit kasutav märgistuspõhimõte põhinedes tasakaalustatakse märgitud kanded üksteise suhtes. Selles näites tasakaalustatakse 3b 2b-ga ja korrigeerimine USD 6.00 sisestatakse 3b-sse, et väärtus USD 22.00. Selles näites pole rohkem tasakaalustusi tehtud, sest sulgemine loob tasakaalustusi ainult finantsiliselt uuendatud kannete puhul.

Uus jooksev keskmine omahind kajastab finantsiliselt ja füüsiliselt värskendatud kannete keskmist: 27,50 USA dollarit.

Järgmine illustratsioon näitab LIFO laomudeli mõju sellele kannete seeriale väljaminekute ja sissetulekute vahelise märkimise kasutamisel.

![LIFO märkimisega.](./media/lifo-with-marking.png)

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
- Tasakaalustusi ja märgistusi, mida täidetakse lao sulgemisel, tähistavad punased diagonaalkriipsuga nooled, mis lähevad sissetulekust väljamineki.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
