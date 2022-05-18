---
title: LIFO kuupäev füüsilise väärtuse ja märkimisega
description: Viimasena sisse, esimesena välja (LIFO) on LIFO-põhimõttel põhinev laomudel. Laost väljastamine tasakaalustatakse viimaste sissetulekutega lattu, laokande kuupäeva alusel. Kui enne väljaminek ei ole sissetulekut, siis LIFO kuupäeva kasutades tasakaalustatakse väljaminek mis tahes sissetulekutega, mis toimuvad pärast väljaminek kuupäeva. Mitmed väljaminekud samal päeval tasakaalustatakse viimase väljamineku, viimase sissetuleku järjekorras.
author: JennySong-SH
ms.date: 02/21/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 51592
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ca344e6ca81814e787046f6ece97625d035346d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671446"
---
# <a name="lifo-date-with-physical-value-and-marking"></a>LIFO kuupäev füüsilise väärtuse ja märkimisega

[!include [banner](../includes/banner.md)]

Viimasena sisse, esimesena välja (LIFO) on varude haldus ja hinna määramise meetod, kus viimati toodetud või hangitud varusid müüakse, kasutatakse või likvideeritakse esimesena. Microsoft lao sulgemise protsessi Dynamics 365 Supply Chain Management ajal loob süsteem tasakaalustused, kus viimane sissetulek on vastendatud iga antud kuupäeva esimese väljaminek, alustades vanimast kuupäevast, jne. Kui kasutate laomudelit Viimasena sisse, esimesena välja (LIFO kuupäev) ja kui väljaminek puudub, tasakaalustatakse väljaminek mis tahes sissetulekutega, mis toimuvad pärast väljaminek kuupäeva. Tasakaalustuste ja sobitamise põhimõte põhinevad laokannete finantskuupäeval. Kui samal kuupäeval on mitu väljaminek, tasakaalustatakse need viimase väljamineu, viimase sissetuleku järjekorras. Tasakaalustuste ja korrigeerimiste eelhindamist saab läbi viia lao ümberarvutamise protsessi käivitades.

Saate LIFO kuupäevapõhimõtte alistada, märgistades laokanded nii, et konkreetse kauba sissetulek tasakaalustatakse konkreetse väljaminek. Perioodiline lao sulgemine on vajalik siis, kui kasutate LIFO kuupäeva laomudelit tasakaalustuste loomiseks ja väljaminevate kaupade väärtuse korrigeerimiseks vastavalt LIFO põhimõttele. Lao sulgemise protsessi käivitamiseni väärtussaatakse väljaminek jooksva keskmiseni, kui toimusid füüsilised ja finantsilist uuendused. Kui te ei kasuta märkimist, arvutatakse füüsilise või finantsilise uuendamise ajal jooksev keskmine.

Kui kasutate LIFO kuupäeva laomudelit, soovitame perioodilist lao sulgemist.

Järgmised näited näitavad LIFO kuupäeva kasutamise mõju kolmes konfiguratsioonis:

- LIFO kuupäev füüsilise väärtuse **valiku kaasamata**
- LIFO kuupäev füüsilise väärtuse **valiku kaasamine**
- LIFO kuupäev märkimisega

## <a name="lifo-date-without-the-include-physical-value-option"></a>LIFO kuupäev füüsilise väärtuse valiku kaasamata

Selles näites pole kauba mudeligrupil füüsilise väärtuse kaasamine märgitud. Alloleval joonisel on kuvatud järgmised kanded.

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
- 7\. Teostatakse lao sulgemine. LIFO kuupäeva meetodil põhinedes tasakaalustatakse esimene finantsiliselt värskendatud väljaminek viimase finantsiliselt värskendatud sissetulekuga alates esimesest kuupäevast jne. Selles näites luuakse üks tasakaalustus vahemikus 3b kuni 2b. Korrigeeritakse USD 6.00 3b-ks ja tulemuseks saadav lõplik kulu USD 22.00.

Järgmine näide näitab LIFO kuupäeva laomudeli efekti, kui **valikut** Füüsilise väärtuse hulka ei kasutata.

![LIFO kuupäev füüsilise väärtuse valiku kaasamata.](media/lifo-date-without-include-physical-value.png)

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

## <a name="lifo-date-with-the-include-physical-value-option"></a>LIFO kuupäev füüsilise väärtuse valiku kaasamine

Kui kauba **puhul on** **lehel** Kauba mudeligrupid märgitud ruut Kaasa füüsiline väärtus, kasutab süsteem nii füüsilisi kui finantsilisi sissetulekukandeid jooksva keskmise omahinna arvutamiseks. Vajadusel korrigeerib süsteem ka füüsiliselt värskendatud väljaminekkannet. Kui märkeruut **Kaasa füüsiline väärtus on** tühjendatud, teeb LIFO kuupäeva laomudelit kasutav lao sulgemine tasakaalustusi ainult kannetele, mis on finantsiliselt uuendatud.

Selles näites on kauba mudeligrupil füüsilise väärtuse kaasamine märgitud. 

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
- 7\. Teostatakse lao sulgemine. LIFO kuupäeva meetodi põhjal tasakaalustatakse esimene finantsiliselt värskendatud väljaminek viimase finantsiliselt värskendatud sissetulekuga igal alguskuupäeval, jne. Selles näites luuakse üks tasakaalustus vahemikus 2b kuni 3b. Korrigeeritakse USD 6.00 3b-ks ja tulemuseks saadav lõplik kulu USD 22.00. Lisaks korrigeeritakse kanne 6a sissetulekukande kuluks 5b. Süsteem ei tasakaalusta neid kandeid, kuna sissetulek on füüsiliselt, kuid mitte finantsiliselt uuendatud. Selle asemel sisestatakse ainult USD 6.33 korrigeerimine füüsilise väljamineu kandesse ja tulemuseks saadav korrigeeritud kulu USD 30.00.

Järgmisel joonisel on kujutatud laomudeli LIFO mõju, kui kasutatakse valikut **Kaasa füüsiline väärtus**.

![LIFO kuupäev valikuga Füüsilise väärtuse kaasamine.](media/lifo-date-with-include-physical-value.png)

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

## <a name="lifo-date-with-marking"></a>LIFO kuupäev märkimisega

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
- 3c. <a1/&. 3b varude finants väljastamis on märgitud 1b varude finantsi aastaseks väljaminekuks.
- 4a. Lao füüsiline sissetulek kogusele 1 hinnaga 25,00 USD tükk.
- 5a. Lao füüsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 5b. Lao finantsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 6a. Lao füüsiline väljastus, kogus 1, omahind USD 23.00 (finantsiliselt sisestatud kannete jooksev keskmine)
- 7\. Teostatakse lao sulgemine. Märgitud kanded tasakaalustatakse üksteise suhtes märkimispõhimõtte järgi, mis kasutab LIFO kuupäeva meetodit. Selles näites tasakaalustatakse 3b 1b-ga ja korrektsioon -6,00 USD-le sisestatakse 3b-sse, et väärtus USD 10.00. Selles näites pole rohkem tasakaalustusi tehtud, sest sulgemine loob tasakaalustusi ainult finantsiliselt uuendatud kannete puhul.

Järgmine näide näitab LIFO kuupäeva laomudeli efektide kohta, kui kasutatakse kaupade ja sissetulekute omavahelist märkimist. 

![LIFO kuupäev koos märkimisega.](media/lifo-date-with-marking.png)

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
