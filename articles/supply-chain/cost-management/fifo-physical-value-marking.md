---
title: FIFO füüsilise väärtuse ja märkimisega
description: FIFO on laomudel, milles esimesena hangitud sissetulekud väljastatakse esimesena. Finantsiliselt värskendatud väljaminekud laost tasakaalustatakse esimeste finantsiliselt värskendatud lattu minevate sissetulekutega, põhinedes laokannete finantsilisel kuupäeval.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 54682
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5280498a23df26873dda1f380f686796f5e1055f
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092136"
---
# <a name="fifo-with-physical-value-and-marking"></a>FIFO füüsilise väärtuse ja märkimisega

[!include [banner](../includes/banner.md)]


Esimene sisse, esimene välja (FIFO) on varude haldamise ja hindamise meetod, kus kõigepealt müüakse, kasutatakse või kõrvaldatakse kõigepealt esmakordselt toodetud või omandatud varusid. Microsofti Dynamics 365 Supply Chain Management varude sulgemise protsessi käigus loob süsteem tasakaalustused, kus esimene tarne sobitatakse esimese väljaminekuga jne.

Tasakaalustuste ja sobitamise põhimõte põhinevad laokannete finantskuupäevanil. Arvelduste ja kohanduste esialgse hindamise saab teha varude ümberarvutamise protsessi käitamisega.

FIFO-põhimõtte alistamiseks märkige laokanded nii, et konkreetne kaubatarne tasakaalustatakse konkreetse väljaminekuga. Fifo laomudeli kasutamisel arvelduste loomiseks ja väljaminekute väärtuse reguleerimiseks vastavalt FIFO põhimõttele on vaja perioodilist varude sulgemist. Kuni varude sulgemise protsessi käivitamiseni hinnatakse väljaminekkandeid füüsiliste ja finantsvärskenduste ilmnemisel jooksva keskmise juures. Kui te ei kasuta märgistust, arvutatakse jooksev keskmine füüsilise või finantsvärskenduse tegemisel. Järgmised näited näitavad FIFO kasutamise mõju kolmes eri konfiguratsioonis.

- FIFO valikuta **Füüsilise väärtuse kaasamine**
- FIFO valikuga **Füüsilise väärtuse kaasamine**
- FIFO märkimisega

## <a name="fifo-without-the-include-physical-value-option"></a>FIFO valikuta Füüsilise väärtuse kaasamine

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
- 7\. Teostatakse lao sulgemine. FIFO meetodil lahendatakse esimene rahaliselt uuendatud väljaminek esimese rahaliselt uuendatud kviitungi ja nii edasi. Selles näites luuakse üks asula vahemikus 1b kuni 3b. Korrigeeritakse USD -6,00-ni 3b-ni ja sellest tulenev lõplik maksumus USD 10.00.

Uus keskmise hinna käitamine kajastab finantsiliselt värskendatud kannete keskmist. Järgmised illustratsioonid näitavad FIFO laomudeli mõju sellele kannete seeriale, kui valikut **Füüsilise väärtuse kaasamine** ei kasutata.

![FIFO ilma valikuta Kaasa füüsiline väärtus.](./media/fifo-without-include-physical-value.png)

**Diagrammi võti**

- Laokandeid tähistavad vertikaalsed nooled.
- Füüsilisi tehinguid esindavad lühemad helehallid nooled.
- Finantstehinguid esindavad pikemad mustad nooled.
- Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
- Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Iga diagrammi kuupäev on eraldatud õhukese musta vertikaalse joonega. Kuupäev on märgitud diagrammi allosas.
- Varude sulgemist tähistab punane vertikaalne kriipsjoon.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

## <a name="fifo-with-the-include-physical-value-option"></a>FIFO valikuga Füüsilise väärtuse kaasamine

**Kui lehel Kauba mudeligrupp** on kauba **jaoks märgitud märkeruut Kaasa füüsiline väärtus**, kasutab süsteem jooksva keskmise omahinna arvutamiseks nii füüsilisi kui ka finantssissesaamise kandeid. Vajaduse korral kohandab süsteem ka füüsiliselt uuendatud väljalasketehingut. Fifo laomudelit kasutav varude sulgemine teeb tasakaalustused ainult rahaliselt värskendatavatele kannetele. Alloleval joonisel on kuvatud järgmised kanded.

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
- 7\. Teostatakse lao sulgemine. FIFO meetodil lahendatakse esimene rahaliselt uuendatud väljaminek esimese rahaliselt uuendatud kviitungi ja nii edasi. Selles näites luuakse üks asula vahemikus 1b kuni 3b. Korrigeeritakse USD -6,00-ni 3b-ni ja sellest tulenev lõplik maksumus USD 10.00. Lisaks korrigeeritakse kannet 6a kviitungi tehingu maksumusega 2b. Süsteem ei tasakaalusta neid kandeid, kuna sissetulek on värskendatud ainult füüsiliselt ja mitte rahaliselt. Selle asemel sisestatakse füüsilisele emissioonikandele ainult korrigeerimine -1,67 USD ja sellest tulenev korrigeeritud maksumus USD 22.00.

![FIFO koos valikuga Kaasa füüsiline väärtus.](./media/fifo-with-include-physical-value.png)

Pange tähele, et varude sulgemise protsessi käitamise tulemus on sama, olenemata sellest, kas valite **lehel Kauba mudelirühm** suvandi **Kaasa füüsiline väärtus**. Suvand **Kaasa füüsiline väärtus** mõjutab ainult jooksvat keskmist.

**Diagrammi võti**

- Laokandeid tähistavad vertikaalsed nooled.
- Füüsilisi tehinguid esindavad lühemad helehallid nooled.
- Finantstehinguid esindavad pikemad mustad nooled.
- Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
- Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Iga diagrammi kuupäev on eraldatud õhukese musta vertikaalse joonega. Kuupäev on märgitud diagrammi allosas.
- Varude sulgemist tähistab punane vertikaalne kriipsjoon.
- Tasakaalustusi, mida teeb lao sulgemine, tähistatakse punaste diagonaalsete katkendnooltega, mis suunduvad sissetulekust väljaminekuni.

## <a name="fifo-with-marking"></a>FIFO märkimisega

Märkimine on protsess, mis võimaldab teil väljaminekukande siduda või märkida sissetulekukandega. Märkimine võib toimuda nii enne kui pärast kande sisestamist. Saate kasutada märkimist, kui soovite teada laoseisu täpset hinda kande sisestamise või lao sulgemise ajal.

Näiteks võttis teie klienditeenindusosakond oluliselt kliendilt vastu kiirtellimuse. Kuna see tellimus on kiirtellimus, peate selle kauba eest maksma rohkem, et täita oma kliendi taotlust. Peate veenduma, et laokauba maksumus kajastub müügitellimuse arve veeruses või müüdud kauba maksumuses (COGS). Ostutellimuse sisestamisel saadakse laoseis maksumusega 120,00 USD. Kui müügitellimuse dokument on märgitud ostutellimusele enne saatelehe või arve konteerimist, USD 120.00 COGS, mitte kauba praegune jooksev keskmine kulu. Kui müügitellimuse saateleht või arve sisestatakse enne märkimist, sisestatakse COGS jooksva keskmise omahinna juurde. Enne lao sulgemist saab neid kahte kannet veel üksteisele märkida.

Kui tarnekanne on märgitud väljaminekukandele, jäetakse kauba mudeligrupis määratletud hindamismeetod tähelepanuta ja süsteem tasakaalustab need kanded üksteisega. Kande saate käsitsi märkida müügitellimuse reale **lehel Müügitellimuse üksikasjad**, valides **kiirkaardil \> Müügitellimuse read** varude **märgise**. Avatud sissetulekukandeid saate vaadata lehel **Märkimine**. Konteeritud varude korrigeerimise töölehelt saate vastenduskande sobitada või märkida varutud kauba avatud tarnekandega. Alloleval joonisel on kuvatud järgmised kanded.

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
- 7\. Teostatakse lao sulgemine. FIFO meetodit kasutava märgistamispõhimõtte alusel arveldatakse märgitud tehingud omavahel. Selles näites tasakaalustatakse 3b 2b vastu ja väärtuse USD 22.00 toomiseks sisestatakse USD 6.00 korrigeerimine 3b-le. Selles näites täiendavaid tasakaalustusi ei tehta, sest sulgemine loob arveldused ainult rahaliselt värskendatud kannete jaoks.

Järgmine illustratsioon näitab FIFO laomudeli mõju sellele kannete seeriale väljaminekute ja sissetulekute vahelise märkimise kasutamisel.

![FIFO märgistusega.](./media/fifo-with-marking.png)

**Diagrammi võti**

- Laokandeid tähistavad vertikaalsed nooled.
- Füüsilisi tehinguid esindavad lühemad helehallid nooled.
- Finantstehinguid esindavad pikemad mustad nooled.
- Sissetulekuid laovarudesse tähistavad vertikaalsed nooled ajajoone kohal.
- Väljaminekuid laovarudest tähistavad vertikaalsed nooled ajajoone all.
- Iga uus sissetuleku või väljamineku kanne on tähistatud uue sildiga.
- Iga vertikaalne nool on sildistatud jadaidentifikaatoriga, nt *1a*. Identifikaatorid näitavad laokannete sisestuste järjestust ajajoonel.
- Iga diagrammi kuupäev on eraldatud õhukese musta vertikaalse joonega. Kuupäev on märgitud diagrammi allosas.
- Varude sulgemist tähistab punane vertikaalne kriipsjoon.
- Tasakaalustusi ja märgistusi, mida teostab varude sulgemine, esindavad punased diagonaalsed kriipsnooled, mis lähevad kviitungist väljaminekusse.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
