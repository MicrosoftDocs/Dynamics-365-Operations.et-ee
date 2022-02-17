---
title: LIFO füüsilise väärtuse ja märkimisega
description: Viimasena sisse, esimesena välja (LIFO) on kaubavarude meetod, milles viimased (uusimad) sissetulekud väljastatakse esimesena. Laost väljastamine tasakaalustatakse viimaste sissetulekutega lattu, laokande kuupäeva alusel.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 55021
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd57d58aa91aa87b1c2feff52a568296fc18ed9b
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092160"
---
# <a name="lifo-with-physical-value-and-marking"></a>LIFO füüsilise väärtuse ja märkimisega

[!include [banner](../includes/banner.md)]

Viimane sisse, esimene välja (LIFO) on varude haldamise ja hindamise meetod, kus viimasena toodetud või omandatud varusid müüakse, kasutatakse või kõrvaldatakse esimesena. Microsofti Dynamics 365 Supply Chain Management varude sulgemise protsessi käigus loob süsteem tasakaalustused, kus viimane tarne sobitatakse esimese väljaminekuga jne. Tasakaalustuste ja sobitamise põhimõte põhinevad laokannete finantskuupäevanil. Arvelduste ja kohanduste esialgse hindamise saab teha varude ümberarvutamise protsessi käitamisega.

Lifo põhimõtte alistamiseks märkige laokanded nii, et konkreetne kauba sissetulek tasakaalustatakse konkreetse väljaminekuga. Perioodiline varude sulgemine on vajalik, kui kasutate LIFO laomudelit tasakaalustuste loomiseks ja väljaminekute väärtuse kohandamiseks vastavalt LIFO põhimõttele. Kuni varude sulgemise protsessi käivitamiseni hinnatakse väljaminekkandeid füüsiliste ja finantsvärskenduste ilmnemisel jooksva keskmise juures. Kui te ei kasuta märgistust, arvutatakse jooksev keskmine füüsilise või finantsvärskenduse tegemisel.

Järgmised näited näitavad LIFO kasutamise mõju kolmes eri konfiguratsioonis.

- LIFO valikuta **Füüsilise väärtuse kaasamine**
- LIFO valikuga **Füüsilise väärtuse kaasamine**
- LIFO märkimisega

## <a name="lifo-without-the-include-physical-value-option"></a>LIFO ilma valikuta Füüsilise väärtuse kaasamine

Selles näites **tühjendatakse välja lastud toote kaubamudeligrupis märkeruut Kaasa füüsiline väärtus**. Alloleval joonisel on kuvatud järgmised kanded.

- 1a. Lao füüsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
- 1b. Lao finantsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
- 2a. Lao füüsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
- 2b. Lao finantsiline sissetulek kogusele 1 hinnaga 22,00 USD tükk.
- 3a. Varude füüsiline väljaminek kogusele 1 omahinnaga USD 16.00 (finantsiliselt konteeritud kannete jooksev keskmine).
- 3b. Varude finantsemissioon kogusele 1 omahinnaga USD 16.00 (finantssisestuskannete jooksev keskmine).
- 4a. Lao füüsiline sissetulek kogusele 1 hinnaga 25,00 USD tükk.
- 5a. Lao füüsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 5b. Lao finantsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 6a. Varude füüsiline väljaminek kogusele 1 omahinnaga USD 23.00 (finantsiliselt konteeritud kannete jooksev keskmine)
- 7\. Teostatakse lao sulgemine. LIFO meetodil lahendatakse esimene rahaliselt värskendatud väljaminek viimase rahaliselt värskendatud kviitungi ja nii edasi. Selles näites luuakse üks asula vahemikus 5b kuni 3b. Korrigeeritakse USD 14.00 3b-ni ja sellest tulenev lõplik maksumus USD 30.00.

Järgmine illustratsioon näitab FIFO laomudeli mõju sellele kannete seeriale, kui valikut **Füüsilise väärtuse kaasamine** ei kasutata.

![LIFO ilma valikuta Kaasa füüsiline väärtus.](./media/lifo-without-including-physical-value.png)

**Diagrammi võti**

- Laokandeid tähistavad vertikaalsed nooled.
- Füüsilisi tehinguid esindavad lühemad helehallid nooled.
- Finantstehinguid esindavad pikemad mustad nooled.
- Varudesse laekumisi esindavad telje kohal olevad vertikaalsed nooled.
- Varudest väljas olevaid väljumisi esindavad telje all olevad vertikaalsed nooled.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Iga diagrammi kuupäev on eraldatud õhukese musta vertikaalse joonega. Kuupäev on märgitud diagrammi allosas.
- Varude sulgemist tähistab punane vertikaalne kriipsjoon.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

## <a name="lifo-with-the-include-physical-value-option"></a>LIFO koos valikuga Füüsilise väärtuse kaasamine

**Kui lehel Kauba mudeligrupid** on kauba **jaoks märgitud märkeruut Kaasa füüsiline väärtus**, kasutab süsteem jooksva keskmise omahinna arvutamiseks nii füüsilisi kui ka finantstarnekandeid. Vajaduse korral kohandab süsteem ka füüsiliselt uuendatud väljalasketehingut. **Kui märkeruut Kaasa füüsiline väärtus** on tühjendatud, teeb LIFO laomudelit kasutav varude sulgemine tasakaalustused ainult finantsiliselt värskendatavatele kannetele.

Alloleval joonisel on kuvatud järgmised kanded.

- 1a. Lao füüsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
- 1b. Lao finantsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
- 2a. Lao füüsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
- 2b. Lao finantsiline sissetulek kogusele 1 hinnaga 22,00 USD tükk.
- 3a. Varude füüsiline väljaminek kogusele 1 omahinnaga USD 16.00 (füüsiliselt ja rahaliselt sisestatud kannete jooksev keskmine).
- 3b. Varude finantsemissioon kogusele 1 omahinnaga USD 16.00 (füüsiliselt ja rahaliselt sisestatud kannete jooksev keskmine).
- 4a. Lao füüsiline sissetulek kogusele 1 hinnaga 25,00 USD tükk.
- 5a. Lao füüsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 5b. Lao finantsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 6a. Varude füüsiline väljaminek kogusele 1 omahinnaga USD 23.67 (füüsiliselt ja rahaliselt sisestatud kannete jooksev keskmine).
- 7\. Teostatakse lao sulgemine. LIFO meetodil lahendatakse esimene rahaliselt värskendatud väljaminek viimase rahaliselt värskendatud kviitungi ja nii edasi. Selles näites luuakse üks asula vahemikus 3b kuni 5b. Korrigeeritakse USD 14.00 3b-ni ja sellest tulenev lõplik maksumus USD 30.00. Lisaks korrigeeritakse kannet 6a kviitungi tehingu maksumusega 4a. Süsteem ei tasakaalusta neid kandeid, kuna sissetulek on värskendatud ainult füüsiliselt ja mitte rahaliselt. Selle asemel sisestatakse füüsilisele väljaminekukandele ainult USD 1.33 korrigeerimine ja sellest tulenev korrigeeritud kulu USD 25.00.

Järgmine illustratsioon näitab LIFO laomudeli mõju sellele kannete seeriale, kui valikut **Füüsilise väärtuse kaasamine** kasutatakse.

![LIFO koos valikuga Kaasa füüsiline väärtus.](./media/lifo-with-included-physical-value.png)

**Diagrammi võti**

- Laokandeid tähistavad vertikaalsed nooled.
- Füüsilisi tehinguid esindavad lühemad helehallid nooled.
- Finantstehinguid esindavad pikemad mustad nooled.
- Varudesse laekumisi esindavad telje kohal olevad vertikaalsed nooled.
- Varudest väljas olevaid väljumisi esindavad telje all olevad vertikaalsed nooled.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Iga diagrammi kuupäev on eraldatud õhukese musta vertikaalse joonega. Kuupäev on märgitud diagrammi allosas.
- Varude sulgemist tähistab punane vertikaalne kriipsjoon.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

## <a name="lifo-with-marking"></a>LIFO märkimisega

Märkimine on protsess, mis võimaldab teil väljaminekukande siduda või märkida sissetulekukandega. Märkimine võib toimuda nii enne kui pärast kande sisestamist. Saate kasutada märkimist, kui soovite teada laoseisu täpset hinda kande sisestamise või lao sulgemise ajal. Näiteks võttis teie klienditeenindusosakond oluliselt kliendilt vastu kiirtellimuse. Kuna see tellimus on kiirtellimus, peate kliendi taotluse täitmiseks kauba eest rohkem maksma.

Peate veenduma, et laokauba maksumus kajastub müügitellimuse arve veeruses või müüdud kauba maksumuses (COGS). Ostutellimuse sisestamisel saadakse laoseis maksumusega 120,00 USD. Kui see müügitellimuse dokument märgitakse ostutellimusele enne saatelehe või arve sisestamist, kasutatakse laokauba kulu (COGS) 120,00 USA dollarit, mitte kauba praegust jooksvat keskmist kulu. Kui müügitellimuse saateleht või arve sisestatakse enne märkimist, sisestatakse COGS jooksva keskmise omahinna juurde.

Enne lao sulgemist saab neid kahte kannet veel üksteisele märkida.

Väljaminekukande saate sissetulekule märkida enne kande sisestamist. Seda märkimist saate teha müügitellimuse real lehel **Müügitellimuse üksikasjad**, valides **kiirkaardil \> Müügitellimuse read** varude **märgistuse**. Avatud sissetulekukandeid saate vaadata lehel **Märkimine**.

Samuti saate pärast kande sisestamist märkida väljastuskande sissetulekule. Väljaminekukande saate märkida või vastendada varude korrigeerimistöölehel sisestatud laokauba avatud sissetulekukandega.

Alloleval joonisel on kuvatud järgmised kanded.

- 1a. Lao füüsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
- 1b. Lao finantsiline sissetulek kogusele 1 hinnaga 10,00 USD tükk.
- 2a. Lao füüsiline sissetulek kogusele 1 hinnaga 20,00 USD tükk.
- 2b. Lao finantsiline sissetulek kogusele 1 hinnaga 22,00 USD tükk.
- 3a. Varude füüsiline väljaminek kogusele 1 omahinnaga USD 16.00 (finantsiliselt konteeritud kannete jooksev keskmine).
- 3b. Varude finantsemissioon kogusele 1 omahinnaga USD 16.00 (finantssisestuskannete jooksev keskmine).
- 3c. 3b varude finantsemissioon on märgitud varude finantsemissiooniks 2b jaoks.
- 4a. Lao füüsiline sissetulek kogusele 1 hinnaga 25,00 USD tükk.
- 5a. Lao füüsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 5b. Lao finantsiline sissetulek kogusele 1 hinnaga 30,00 USD tükk.
- 6a. Varude füüsiline väljaminek kogusele 1 omahinnaga USD 23.00 (finantsiliselt konteeritud kannete jooksev keskmine)
- 7\. Teostatakse lao sulgemine. LIFO meetodit kasutava märgistamispõhimõtte alusel arveldatakse märgitud kanded omavahel. Selles näites tasakaalustatakse 3b 2b vastu ja väärtuse USD 22.00 toomiseks sisestatakse USD 6.00 korrigeerimine 3b-le. Selles näites täiendavaid tasakaalustusi ei tehta, sest sulgemine loob arveldused ainult rahaliselt värskendatud kannete jaoks.

Uus jooksev keskmine omahind kajastab finantsiliselt ja füüsiliselt värskendatud kannete keskmist: 27,50 USA dollarit.

Järgmine illustratsioon näitab LIFO laomudeli mõju sellele kannete seeriale väljaminekute ja sissetulekute vahelise märkimise kasutamisel.

![LIFO märgistusega.](./media/lifo-with-marking.png)

**Diagrammi võti**

- Laokandeid tähistavad vertikaalsed nooled.
- Füüsilisi tehinguid esindavad lühemad helehallid nooled.
- Finantstehinguid esindavad pikemad mustad nooled.
- Varudesse laekumisi esindavad telje kohal olevad vertikaalsed nooled.
- Varudest väljas olevaid väljumisi esindavad telje all olevad vertikaalsed nooled.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Iga diagrammi kuupäev on eraldatud õhukese musta vertikaalse joonega. Kuupäev on märgitud diagrammi allosas.
- Varude sulgemist tähistab punane vertikaalne kriipsjoon.
- Tasakaalustusi ja märgistusi, mida teostab varude sulgemine, esindavad punased diagonaalsed kriipsnooled, mis lähevad kviitungist väljaminekusse.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
