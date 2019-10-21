---
title: Käibemaksu tasakaalustusperioodide seadistamine
description: Selles teemas selgitatakse, kuidas seadistada käibemaksu tasakaalustusperioode rakenduses Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cff84f8f6c42fd064258b8ca53e24acc8059977
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175380"
---
# <a name="set-up-sales-tax-settlement-periods"></a>Käibemaksu tasakaalustusperioodide seadistamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles teemas selgitatakse, kuidas seadistada käibemaksu tasumise perioode. Käibemaksu tasakaalustusperioodid sisaldavad teavet perioodivahemike kohta, mille puhul tuleb esitada ja maksta käibemaksu. Tasakaalustusprotsessi saab käitada konkreetse kuupäevavahemiku tasakaalustusperioodi puhul. Kõik tasakaalustusperioodiga seotud maksukoodid tasakaalustatakse. Seotud käibemaksuhalduri seadistamisest olenevalt sisestatakse maksukohustus kas hankija või pearaamatu kontole.

See ülesanne kasutab demoettevõtte USMF andmeid.

1. Minge navigeerimispaneelis **Moodulid > Maks > Kaudsed maksud > Käibemaks > Käibemaksu tasakaalustusperioodid**.
2. Valige suvand **Uus**.
3. Sisestage välja **Tasakaalustusperiood** väärtus.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Valige väljal **Maksuhaldur** käibemaksu haldur, kellele tasakaalustusperioodi puhul loodud aruanded ja maksed saadetakse.
6. Otsige loendist ja valige soovitud kirje.
7. Valige väljas **Maksetingimused** soovitud kirje rippmenüüst. Seotud käibemaksuhalduri saab seadistada kui hankija ja käibemaksu tasakaalustus loob avatud hankija arve. Maksetingimused määratlevad avatud hankija arve maksetähtaja.  
8. Valige tasakaalustusperioodi vahemike tüüp.
9. Sisestage perioodivahemiku ühikute arv perioodi kohta. Näiteks kvartalis on 3 kuud.
10. Märkige või tühjendage ruut **Kasuta käibemaksu tasakaalustamiseks pakktöötlust**. Tasakaalustusperioodi tasakaalustusprotsessi saab töödelda taustal pakett-tööna. See on soovitatav suure hulga maksukannete puhul kuupäevavahemiku jooksul.  
    > [!NOTE]
    > Praegu puudub selle tugi Austrias, Belgias, Hispaanias, Itaalias, Jaapanis ja Hollandis.
11. Märkige või tühjendage märkeruut **Vastasmaksukannete loomise ennetamine**. Süsteem loob tasakaalustusprotsessi ajal vaikimisi vastasmaksukandeid, mis põhjustavad jõudlusprobleeme, kui perioodivahemikul on suur hulk maksukandeid. Märkige see märkeruut, et vältida vastasmaksukannete loomist.
12. Laiendage vahekaarti **Perioodivahemikud**.
13. Valige **Lisa**.
14. Sisestage kuupäev välja **Alguskuupäev** uuele reale.
15. Sisestage kuupäev väljale **Lõppkuupäev**.
16. Valige **Uus perioodivahemik**. Kui esimene perioodivahemik on sisestatud, saab uusi perioode luua automaatselt. Vajaduse korral saate naasta ja uusi perioodivahemikke lisada.  
17. Sulgege leht.

