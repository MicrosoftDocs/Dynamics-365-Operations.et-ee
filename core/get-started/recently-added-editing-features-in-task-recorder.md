---
title: Hiljuti lisatud redigeerimisfunktsioonid tegevuse salvestajas
description: "Kui kasutate tegevuse salvestajat tegevusjuhiste loomiseks, saate redigeerida faile tõhusamalt, kasutades selles vikis kirjeldatud funktsioone."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core
ms.custom: 266464
ms.assetid: b4640e67-4b92-4855-8041-1bfc71aadc47
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: c4f9ac515eab6ed8b194fc8985f6d3fae40ced38
ms.lasthandoff: 03/31/2017


---

# <a name="recently-added-editing-features-in-task-recorder"></a>Hiljuti lisatud redigeerimisfunktsioonid tegevuse salvestajas

Kui kasutate tegevuse salvestajat tegevusjuhiste loomiseks, saate redigeerida faile tõhusamalt, kasutades selles vikis kirjeldatud funktsioone.

Need funktsioonid on saadaval menüüs **Sätted &gt; Tegevuse salvestaja &gt; Salvestise redigeerimine**.

-   Etappide lisamine kogu faili uuesti salvestamata.
-   Etappide teisaldamine alamülesande all kogu faili uuesti salvestamata.
-   Salvestise nime ja kirjelduse väljade ahendamine.

## <a name="insert-steps-without-rerecording-the-entire-file"></a>Etappide lisamine kogu faili uuesti salvestamata
Nüüd saab lisada tegevusjuhises kõikjale etapi, ilma kogu faili taasesitamata või uuesti salvestamata.

1.  Valige etapp, mille järele soovite uue etapi lisada. Veenduge, et etapp oleks esile tõstetud.

Selleks, et tegevuse salvestaja etapi lisaks, peab olema lahti õige leht. Õige leht on leht, millel uus etapp toimub. Tegevuse salvestajal on mehhanism, mis määrab aktiivse lehe ja keelab funktsiooni, kui lahti pole õige leht. 

[![tg1](./media/tg1.png)](./media/tg1.png) 


Kui olete õigel lehel, muutub valik **Sisesta etapp** kättesaadavaks.

[![tg2](./media/tg2-231x300.png)](./media/tg2.png)

2. Klõpsake nuppu **Sisesta etapp**.

Nupu **Sisesta etapp** klõpsamisel lülitub tegevuse salvestaja salvestusrežiimi. Nüüd salvestatakse ja lisatakse etappidena mis tahes kasutajaliideses tehtud toiming.

3. Klõpsake käsku **Peata**.

Saate protsessi korrata, lisades või teisaldades vajaliku hulga etappe (vt alamülesandeid altpoolt).

4. Kui olete tegevusjuhise redigeerimise lõpetanud, klõpsake nuppu **Muutmine on lõpetatud** ja tehke siis üks valik tegevusjuhise salvestamiseks või avaldamiseks.

## <a name="move-steps-under-a-subtask-without-rerecording-the-entire-file"></a>Etappide teisaldamine alamülesande all kogu faili uuesti salvestamata
Etappe saab alamülesande all teisaldada, kogu faili taasesitamata või uuesti salvestamata. Samuti võite teisaldada alamülesande etapi või lõpu alamülesande etapi, kui soovite olemasoleva etapiploki grupeerida.

1.  Valige etapp või alamülesande etapp, mida soovite teisaldada. Veenduge, et etapp oleks esile tõstetud.
2.  Klõpsake ellipsit ja seejärel valikut **Teisalda etapp pärast**.

[![tg3](./media/tg3.png)](./media/tg3.png)

3. Valige etapp või alamülesande etapp, mille järele soovite etapi või alamülesande etapi teisaldada. Tegevuse salvestaja teisaldab etapi.

4. Lõpu alamülesande etapi teisaldamiseks valige see, klõpsake ellipsit, klõpsake valikut **Teisalda etapp pärast** ja seejärel valige etapp, mille järele soovite lõpu alamülesande etapi paigutada.

Kui soovite, et tegevusjuhise esimene etapp oleks alamülesande sees, siis looge alamülesande etapp teise etapina ja teisaldage siis esimene etapp selle sisse. Lisada või teisaldada saab nii palju etappe või alamülesandeid, kui vaja.

5. Kui olete tegevusjuhise redigeerimise lõpetanud, klõpsake nuppu **Muutmine on lõpetatud** ja tehke siis üks valik tegevusjuhise salvestamiseks või avaldamiseks.

## <a name="collapse-recording-name-and-description"></a>Salvestise nime ja kirjelduse ahendamine
Välju **Salvestise nimi** ja **Salvestise kirjeldus** saab laiendada ja ahendada. Kui need väljad ahendada, on tegevuse salvestaja redigeerimispaanil näha rohkem etappe. 

[![tg4](./media/tg4-300x252.png)](./media/tg4.png)  

<a name="see-also"></a>Vt ka
--------

[Dokumentide või koolituse loomine tegevuse salvestiste abil](/dynamics365/operations/dev-itpro/user-interface/task-recorder)

[Tegevuse salvestaja kiirviide](/dynamics365/operations/dev-itpro/user-interface/task-recorder-quick-reference)


